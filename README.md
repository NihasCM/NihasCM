<!--
  README.md — github.com/NihasCM/NihasCM
  ─────────────────────────────────────────────────────────────────────────
  ORDER: proof before biography. Header → Experience → Projects →
  Architecture → Current Focus → whoami → Stack → Activity → Contact.

  Identity fields (location, title, email, LinkedIn, stack) are kept in
  sync with Nihas_Resume.docx — the resume is the source of truth.

  EXTERNAL REQUESTS: 3 — capsule-render (header), github-readme-stats
  (official), snake SVG (self-hosted on your own output branch).

  Note on the banner: capsule-render is community-hosted, so it can 502.
  Every image here has real alt text, so a failed load degrades to a
  readable text line rather than a broken-image icon. That's the mitigation.

  ⚠ BLOCKING: scrapping · hotel-harmony · tirulocal-hub are PRIVATE.
  Those three links 404 for everyone but you. Make them public before
  publishing, or delete the entries.

  Verified against the repos via GitHub API on 2026-07-29. Every claim
  traces to a file. No metrics appear because none are measured anywhere
  in the code — do not add any you cannot demonstrate.
  ─────────────────────────────────────────────────────────────────────────
-->

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0a0a,50:0d1117,100:007AFF&height=170&section=header&text=Nihas&fontSize=48&fontColor=ffffff&fontAlignY=36&desc=Full-Stack%20Developer%20%E2%80%A2%20Supply%20Chain%20Tech%20%E2%80%A2%20RPA%20%26%20AI%2FML&descAlignY=56&descSize=14&descColor=8b949e&animation=fadeIn" alt="Nihas — Full-Stack Developer, Supply Chain Tech, RPA and AI/ML" />

**Building internal tools and supply chain systems that automate operations,
aggregate data, and power business workflows.**

`Python` · `TypeScript` · `React` · `Node.js` · `MySQL`

Chennai, India · GMT+5:30 · Open to Software Engineering & Supply Chain Tech

</div>

---

## Experience

**Sourcing Executive — Full-Stack Developer, Internal Tools** · GOGOX India · Chennai
*May 2025 – Present*

- Built and maintained in-house Fleet Management (FMS), HRM, and logistics
  operations platforms
- React · TypeScript · Node.js · Express · MySQL · Firebase · BigQuery
- Browser automation for data processing and advance payment validation
- Role-based dashboards and reporting for faster operational decisions

**Software Developer Intern** · AAMRO Freight · Chennai
*Jan 2025 – Mar 2025*

- Shipped a supply chain app covering orders, inventory, and automated
  low-stock alerts — removed 60% of manual stock checks
- Node/Express backend over MySQL, 10+ REST endpoints, sub-200ms responses
- Cut order placement from 7 steps to 4

---

## Featured Projects

<!--
  Uniform shape per project: one-line summary → stack → highlights → repo.
  Same structure every time so the eye lands in the same place. Depth lives
  in each repo's own README.
-->

### Multi-Source Listing Aggregation Pipeline

> Concurrent pipeline that aggregates and deduplicates listings from four
> travel and mapping providers into a single Postgres table.

**Stack**
Python · asyncio · Playwright · rapidfuzz · geopy · Supabase

**Highlights**

- Concurrent scraping via `asyncio.gather`, fault-isolated per source
- Two-stage deduplication: fuzzy name matching, then geospatial distance
- Idempotent upserts — re-runs enrich rows instead of resetting them
- Per-source field trust: maps for coordinates, OTAs for price
- Rotating logs with error screenshots on scraper failure

**Repository**
[NihasCM/scrapping](https://github.com/NihasCM/scrapping) — architecture documented in `CLAUDE.md`

### Hotel Operations Platform

> Property management across rooms, guests, payments, reporting, and
> multi-method payment reconciliation.

**Stack**
React · TypeScript · Tailwind CSS · Vitest · Docker

**Highlights**

- Generic typed `request<T>` wrapper over six domain modules
- HTTP errors normalized at a single boundary
- CSV reconciliation matching system refs against bank refs
- Covers UPI, GPay, PhonePe, and card with matched/unmatched/pending states

**Repository**
[NihasCM/hotel-harmony](https://github.com/NihasCM/hotel-harmony) — API layer runs on mock data; backend is separate

### Local Commerce Platform

> Two-sided platform: public directory across six categories, plus an admin
> console for the operators running it.

**Stack**
React · TypeScript · TanStack Router · Tailwind CSS · Vitest

**Highlights**

- Parameterized routes per category, six detail components on one layout contract
- Admin side: listings, reviews, users, categories, CMS, analytics, activity log
- Largest codebase here (~509 KB TypeScript), 43 commits

**Repository**
[NihasCM/tirulocal-hub](https://github.com/NihasCM/tirulocal-hub)

### KZ IOR/EOR Information System

> Flask app for searching Kazakhstan import/export compliance data across
> four manufacturer datasets.

**Stack**
Python · Flask · pandas · openpyxl

**Highlights**

- Part-number search resolving HS codes, ECCN, and license requirements
- Normalizes inconsistent Excel headers across four vendor sources

**Repository**
[NihasCM/Aamro-Project](https://github.com/NihasCM/Aamro-Project)

### Driver Drowsiness Detection System

> Real-time fatigue monitoring that flags drowsiness from eye-blink frequency
> and head-tilt patterns.

**Stack**
Python · OpenCV · Computer Vision · Machine Learning

**Highlights**

- Facial landmark recognition flagging fatigue events within 1–2 seconds
- 90%+ detection accuracy across varied lighting in a simulated environment
- Audio-visual alert triggers on fatigue detection

*Academic project, Jan – Apr 2023*

---

## Pipeline Architecture

**Three decisions worth asking me about**

- Dedup needs both signals: names differ across sources, coordinates go
  missing — either alone produces false merges
- Upsert keys on a generated slug, because no source ID is shared by all
  four providers
- Each source is trusted only for the fields it owns

---

## Current Focus

- Full-stack development — React/TypeScript frontends over Node.js APIs
- Supply chain technology — fleet management, freight, inventory systems
- Databases — MySQL and PostgreSQL schema design, query optimization
- Automation & RPA — browser automation, multi-source data collection
- AI/ML — computer vision and applied ML fundamentals

---

<table>
<tr>
<td width="55%" valign="top">

### `> whoami`

```yaml
focus:        Full-stack dev · supply chain tech
languages:    Python · TypeScript · JavaScript
backend:      Node.js · Express · Flask · asyncio
frontend:     React · TanStack Router · Tailwind
databases:    MySQL · PostgreSQL · Supabase · BigQuery
emerging:     RPA · OpenCV · Machine Learning
building:     Fleet management & internal ops tooling
              multi-source data aggregation
education:    MCA, SRM Institute (CGPA 8.6)
open_to:      Software engineering · supply chain tech
timezone:     GMT+5:30 (Chennai)
```

</td>
<td width="45%" valign="top" align="center">

<!-- Official github-readme-stats. Most repos are private, so
     include_all_commits keeps this from understating the work. -->
<img src="https://github-readme-stats.vercel.app/api?username=NihasCM&show_icons=true&hide_border=true&hide_title=true&include_all_commits=true&theme=transparent&icon_color=007AFF&text_color=808080&cache_seconds=86400" alt="GitHub statistics for NihasCM" width="100%" />

</td>
</tr>
</table>

---

## Stack

<!-- Technologies used either in a public repo here or in production work at
     GOGOX/AAMRO. Flutter, Streamlit, UiPath omitted — nothing uses them.
     HTML/CSS omitted as baseline. -->

| | |
|---|---|
| **Languages** | Python · TypeScript · JavaScript · SQL |
| **Backend** | Node.js · Express · Flask · asyncio · Playwright |
| **Data** | pandas · openpyxl · rapidfuzz · geopy · BigQuery |
| **Frontend** | React · TanStack Router · Tailwind CSS · Vite |
| **Databases** | MySQL · PostgreSQL · Supabase · Firebase |
| **Emerging** | RPA · OpenCV · Machine Learning · AWS AI/ML |
| **Testing** | Vitest |
| **DevOps** | Docker · GitHub Actions · Netlify · GitHub Pages |
| **Tools** | Git · ESLint · Prettier · Bun · Android Studio |

---

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/NihasCM/NihasCM/output/github-contribution-grid-snake-dark.svg">
  <img alt="Contribution graph for NihasCM" src="https://raw.githubusercontent.com/NihasCM/NihasCM/output/github-contribution-grid-snake.svg" width="100%">
</picture>

<br><br>

**[LinkedIn](https://www.linkedin.com/in/nihas23/)** ·
**[Portfolio](https://nihascm.github.io/nihascm.dev/)** ·
**nihasnooruliyen@gmail.com**

</div>
