# Localization

5RRRRR supports 20 locales from day one, with per-language calibration for fair scoring.

## Supported Locales

| Code | Language | Script |
|------|----------|--------|
| en | English | Latin |
| ru | Russian | Cyrillic |
| es | Spanish | Latin |
| fr | French | Latin |
| de | German | Latin |
| pt | Portuguese | Latin |
| it | Italian | Latin |
| nl | Dutch | Latin |
| ja | Japanese | CJK |
| ko | Korean | Hangul |
| zh | Chinese | CJK |
| th | Thai | Thai |
| tr | Turkish | Latin |
| hi | Hindi | Devanagari |
| id | Indonesian | Latin |
| vi | Vietnamese | Latin |
| ar | Arabic | Arabic (RTL) |
| pl | Polish | Latin |
| uk | Ukrainian | Cyrillic |
| sv | Swedish | Latin |

## Translation Architecture

Translations are stored in Cloudflare KV and served at the edge via the [Translation Worker](https://github.com/5Rreview/translation-worker).

```
Backend (Laravel)
  │
  │ artisan sync command
  ▼
Cloudflare KV
  │
  │ Translation Worker
  ▼
Frontend (< 20ms globally)
```

### Key Format
- `{locale}:{group}` — e.g., `en:reviews`, `ru:common`
- `_manifest` — sync metadata with available locales and groups

## Per-Language Calibration

The trust scoring system calibrates for language differences:

- **Rating norms** — some cultures rate conservatively (Japanese reviewers tend toward 3-star), others polarize (American reviewers tend toward 1 or 5)
- **Review length** — CJK languages express the same content in fewer characters; German tends to be more verbose
- **Quality scoring** — NLP accuracy varies by language; calibration prevents systematic bias
- **AI detection** — phrase lists are maintained per language, reflecting language-specific AI writing patterns

## RTL Support

Arabic locale uses right-to-left text direction. The frontend and all text processing accounts for RTL layout and word boundary differences.

## Adding New Locales

The system is designed for locale expansion:
1. Add translation strings to all groups
2. Set calibration parameters (rating mean, quality mean, length norms)
3. Create AI phrase list for the new language
4. Deploy via KV sync
