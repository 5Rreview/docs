# Cloudflare Infrastructure

How 5RRRRR leverages Cloudflare's edge network.

## Services Used

| Service | Purpose |
|---------|---------|
| Workers | Edge compute for images, translations, caching |
| R2 | Object storage for media (images, screenshots, avatars) |
| KV | Key-value store for translations, configuration, edge cache |
| DNS | Domain management and routing |
| CDN | Static asset caching and delivery |

## Workers

### Image Worker
- Serves images from R2 with full HTTP semantics
- ETag/If-None-Match for conditional requests
- Range requests for partial content
- Content negotiation (WebP, AVIF detection)
- Multi-bucket routing by hostname
- Open source: [github.com/5Rreview/image-worker](https://github.com/5Rreview/image-worker)

### Translation Worker
- Serves i18n translations from KV at the edge
- Sub-millisecond response times
- 20 locales supported
- Cache API with configurable TTL
- JSONP support for legacy integrations
- Open source: [github.com/5Rreview/translation-worker](https://github.com/5Rreview/translation-worker)

## R2 Storage

Object storage for all platform media:
- User-uploaded review images
- Company logos and brand assets
- Screenshots and verification media
- Served through Image Worker with caching

## KV Store

Edge key-value storage for:
- Translation strings (20 locales, multiple groups)
- Sync manifests for frontend translation loading
- Edge-cached configuration data

## Performance

| Metric | Target |
|--------|--------|
| Image TTFB (cached) | < 50ms globally |
| Translation TTFB | < 20ms globally |
| Cache hit rate | > 95% |
| Availability | 99.9%+ |
