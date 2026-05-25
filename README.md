# nandini_
placement dashboard
# PlaceIQ — Student Placement Analytics Dashboard

A single-file, AI-powered analytics dashboard for exploring and predicting student placement outcomes across a 10,000-student dataset.

## Features

- **Dashboard** — KPI cards, chart story arcs, and data-backed recommendations covering CGPA, aptitude, internships, projects, training, and extracurricular impact
- **Students** — Searchable, filterable, paginated table of student records with an AI cohort analyser for instant segment insights
- **Analysis** — Correlation charts, feature importance bars, monthly trend line, and a Claude-powered chat that answers any question about the dataset with full conversation memory
- **Predictions** — Heuristic placement probability calculator with a gauge, personalised tips, and an AI interpretation of any student profile
- **Reports** — Six pre-built report types (Executive Summary, Feature Correlation, At-Risk, Top Performers, Training Impact, Trend Analysis) with an AI summariser panel
- **Settings** — Display, notification, model, and data preferences with a Claude AI configuration advisor

## Tech Stack

| Layer | Details |
|---|---|
| Frontend | Vanilla HTML / CSS / JavaScript — zero build step |
| Charts | Chart.js 4.4 |
| Fonts | Poppins, Inter, Space Grotesk (Google Fonts) |
| AI | Anthropic Claude API (`claude-sonnet-4-20250514`) via `fetch` |

## Getting Started

1. Open `placement_dashboard.html` in any modern browser.
2. All AI features call `https://api.anthropic.com/v1/messages` directly from the browser — no backend required.
3. To use AI features in production, proxy the API call through your own server to keep your Anthropic API key secret.

## Dataset

- 10,000 synthetic student records
- 11 features: CGPA, Aptitude Score, Soft Skills Rating, Internships, Projects, Placement Training, Extracurricular Activities, SSC Marks, HSC Marks, Placement Status, Predicted Score
- Overall placement rate: **41.97%**

## Key Findings

- Aptitude Score is the strongest predictor (Pearson r = 0.522)
- Placement Training produces a **3.3× placement uplift** (51.6% vs 15.6%)
- Extracurricular Activities produce a **4.5× uplift** (62.0% vs 13.7%)
- The second internship is disproportionately valuable: 0→1 internship barely moves the needle; 1→2 jumps from 32.6% to 69.7%
- CGPA crossing 8.0 nearly doubles placement probability
