# ☁️ Cloudflare Infrastructure

How 5⭐⭐⭐⭐⭐ leverages Cloudflare's edge network for global performance.

## Services Used

| Service | Purpose |
|---------|---------|
| ⚡ Workers | Edge compute for media delivery and translations |
| 💾 R2 | Object storage for all platform media |
| 🔑 KV | Edge key-value store for translations and configuration |
| 🌐 DNS | Domain management and routing |
| 🚀 CDN | Static asset caching and delivery |

## 🔧 Open-Source Workers

| Worker | Description | Repo |
|--------|-------------|------|
| 🖼️ Image Worker | Media delivery from R2 with caching and content negotiation | [image-worker](https://github.com/5Rreview/image-worker) |
| 🌍 Translation Worker | i18n translations served at the edge for 20 locales | [translation-worker](https://github.com/5Rreview/translation-worker) |

## 📈 Performance Targets

| Metric | Target |
|--------|--------|
| Image TTFB (cached) | < 50ms globally |
| Translation TTFB | < 20ms globally |
| Cache hit rate | > 95% |
| Availability | 99.9%+ |
