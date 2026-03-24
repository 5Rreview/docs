# 🌍 Localization

5⭐⭐⭐⭐⭐ supports 20 locales from day one, with per-language calibration for fair scoring.

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

## ⚖️ Per-Language Calibration

The 5R★ Trust Score system calibrates for language and cultural differences:

- **Rating norms** — some cultures rate conservatively (Japanese reviewers tend toward 3-star), others polarize (American reviewers tend toward 1 or 5)
- **Review length** — CJK languages express the same content in fewer characters; German tends to be more verbose
- **Quality scoring** — NLP accuracy varies by language; calibration prevents systematic bias
- **AI detection** — 5R★ AI Risk Flags use per-language patterns to detect AI-generated content

## 🔄 RTL Support

Arabic locale uses right-to-left text direction. The platform fully supports RTL layout and text processing.

## Edge Translations

Translations are served globally at the edge via the open-source [Translation Worker](https://github.com/5Rreview/translation-worker).
