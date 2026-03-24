<p align="center">
  <a href="https://5rrrrr.com">
    <img src="assets/banner.svg" alt="5★★★★★.com — Reviews You Can Trust" width="100%">
  </a>
</p>

<p align="center">
  <a href="https://5rrrrr.com"><img src="https://img.shields.io/badge/🌐_5rrrrr.com-live-F7A610?style=for-the-badge&labelColor=141416" alt="Website"></a>
  <a href="https://github.com/5Rreview/open-trust-methodology"><img src="https://img.shields.io/badge/methodology-open_source-10B981?style=for-the-badge&labelColor=141416" alt="Open Methodology"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-CC_BY_4.0-71717A?style=for-the-badge&labelColor=141416" alt="License"></a>
</p>

<p align="center">
  <sub>Public documentation for <a href="https://5rrrrr.com">5rrrrr.com</a> — the open trust platform</sub>
</p>

---

## 📋 Contents

<table>
<tr>
<td width="50%" valign="top">

### 🔭 Vision & Strategy
- [Project Overview](vision/project-overview.md) — what 5R★ is and why it exists
- [Trust Philosophy](vision/trust-philosophy.md) — core beliefs about trust

### 🏗️ Architecture
- [Platform Architecture](architecture/platform-overview.md) — high-level technical overview
- [Cloudflare Infrastructure](architecture/cloudflare-infrastructure.md) — edge workers
- [Localization](architecture/localization.md) — 20-locale i18n system

</td>
<td width="50%" valign="top">

### 🏢 For Companies
- [How 5R★ Trust Score Works](for-companies/trust-scores.md) — what affects your score
- [Responding to Reviews](for-companies/responding.md) — best practices
- [Claiming Your Profile](for-companies/claiming.md) — how to get started

### 👩‍💻 For Developers
- [API Overview](api/overview.md) — public API <sup>coming soon</sup>
- [Open Trust Methodology](https://github.com/5Rreview/open-trust-methodology) — scoring methodology

</td>
</tr>
</table>

---

## ⭐ 5R★ Core Components

> [!NOTE]
> All five components work together to produce a single **5R★ Trust Score** (0–100) for every company on the platform.

| &nbsp; | Component | Description |
|:---:|-----------|-------------|
| 🛡️ | **5R★ Trust Score** | Composite reputation score (0–100) with confidence grades |
| 🤖 | **5R★ AI Risk Flags** | AI-detected fraud and risk patterns |
| 📰 | **5R★ Business Events** | Chronological company timeline |
| 🔍 | **5R★ Trust Signals** | Raw domain intelligence data |
| ✍️ | **5R★ Reviews** | User reviews with quality scoring and fake detection |

---

## 🔗 Related Repositories

| Repo | Description | Status |
|------|-------------|:------:|
| [`open-trust-methodology`](https://github.com/5Rreview/open-trust-methodology) | 5R★ Trust scoring methodology | ![Public](https://img.shields.io/badge/-public-10B981?style=flat-square) |
| [`image-worker`](https://github.com/5Rreview/image-worker) | Cloudflare R2 image service | ![Public](https://img.shields.io/badge/-public-10B981?style=flat-square) |
| [`translation-worker`](https://github.com/5Rreview/translation-worker) | Cloudflare KV translation service | ![Public](https://img.shields.io/badge/-public-10B981?style=flat-square) |

---

<details>
<summary><strong>🌍 Supported Languages (20)</strong></summary>

<br>

| &nbsp; | Language | Code | &nbsp; | Language | Code |
|:---:|----------|:----:|:---:|----------|:----:|
| 🇬🇧 | English | `en` | 🇯🇵 | Japanese | `ja` |
| 🇷🇺 | Russian | `ru` | 🇰🇷 | Korean | `ko` |
| 🇪🇸 | Spanish | `es` | 🇨🇳 | Chinese | `zh` |
| 🇫🇷 | French | `fr` | 🇹🇭 | Thai | `th` |
| 🇩🇪 | German | `de` | 🇹🇷 | Turkish | `tr` |
| 🇵🇹 | Portuguese | `pt` | 🇮🇳 | Hindi | `hi` |
| 🇮🇹 | Italian | `it` | 🇮🇩 | Indonesian | `id` |
| 🇳🇱 | Dutch | `nl` | 🇻🇳 | Vietnamese | `vi` |
| 🇸🇦 | Arabic | `ar` | 🇵🇱 | Polish | `pl` |
| 🇺🇦 | Ukrainian | `uk` | 🇸🇪 | Swedish | `sv` |

</details>

---

<p align="center">
  <sub>Made with ⭐ by the <a href="https://5rrrrr.com">5R★</a> team · <a href="LICENSE">CC BY 4.0</a></sub>
</p>
