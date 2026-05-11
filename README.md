# Female Tertiary Graduates by Field — Interactive Dashboard

An interactive data dashboard built on the [World Bank Gender Statistics](https://data.worldbank.org/indicator/SE.TER.GRAD.FE.ZS) dataset (**WB_GS_SE_TER_GRAD_FE_ZS**), visualising the share of female tertiary graduates by field of study across 170 countries from 1998 to 2019.

## Live Dashboard

**[View Dashboard →](https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/)**

## Data

| Attribute | Value |
|---|---|
| Source | World Bank Open Data |
| Indicator | `SE.TER.GRAD.FE.ZS` |
| Coverage | 170 countries |
| Period | 1998–2019 |
| Observations | 11,901 non-null data points |
| Fields of Study | 10 (incl. STEM aggregate) |

## Features

- **Global trend lines** — female graduate share over time for each field of study
- **Country rankings** — top 15 countries per field with inline bar visualisation
- **Field comparison bar chart** — cross-field average comparison
- **Country spotlight** — per-country time series for any field and country
- **KPI strip** — at-a-glance summary statistics
- **Fully offline** — all data embedded in `index.html`; no server needed

## How to Host on GitHub Pages

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Under *Source*, select `Deploy from a branch` → `main` → `/ (root)`
4. Save — your dashboard will be live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/` within ~1 minute

Or use the included GitHub Actions workflow (`.github/workflows/pages.yml`) which deploys automatically on every push to `main`.

## Local Development

No build step required. Just open `index.html` in any browser:

```bash
open index.html   # macOS
start index.html  # Windows
xdg-open index.html  # Linux
```

## Tech Stack

- **Chart.js 4.4** — line, bar, and horizontal bar charts
- **Vanilla JS** — no framework overhead
- **CSS custom properties** — theming and dark mode
- **Google Fonts** — Playfair Display + DM Sans + DM Mono

## Data Notes

- Only `OBS_STATUS = 'A'` (actual) records are used; missing values are excluded
- Country-level data uses ISO 3-character codes; World Bank regional aggregates are excluded from country-level views but included in global trend averages
- All values represent the **percentage of graduates in a given field who are female**
