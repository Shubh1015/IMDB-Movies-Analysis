# 🎬 IMDb Movies Analytics Dashboard

[![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white)](https://www.tableau.com/)
[![Domain](https://img.shields.io/badge/Domain-Entertainment_Analytics-purple?style=flat-square)]()
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)]()

> A Tableau-powered visual analytics dashboard that decodes IMDb's movie database — surfacing patterns in genre popularity, audience ratings, directorial performance, and box office trends across decades of cinema.

---

## 📌 Problem Statement

The entertainment industry generates enormous volumes of audience and revenue data, yet most stakeholders — producers, distributors, content platforms — lack a consolidated analytical view of what has historically resonated with audiences. Sifting through IMDb's raw data to answer questions like *"Which genres consistently earn the highest ratings?"* or *"How has average movie runtime changed over the last 30 years?"* requires hours of manual analysis.

This dashboard compresses that analysis into seconds.

---

## 💡 Solution Overview

The IMDb Movies Dashboard provides an interactive exploration of movie metadata — including titles, genres, release years, IMDb ratings, vote counts, runtime, and directorial credits. It is designed for:

- **Content strategists** identifying high-performing genres for investment
- **Film enthusiasts** exploring patterns in cinema history
- **Data analysts** learning visual storytelling with entertainment data

---

## ✨ Features

- **Genre Performance Analysis** — Average IMDb rating and vote count by genre; identifies consistently well-received categories
- **Decade-wise Trend Analysis** — How audience preferences, ratings, and movie output have shifted across decades
- **Top Rated Films Leaderboard** — Ranked list of highest-rated movies filterable by genre and era
- **Director Performance View** — Aggregated ratings and movie count by director for top filmmakers
- **Runtime Distribution** — Histogram showing runtime patterns across genres (action vs. drama vs. animation)
- **Rating Distribution** — Frequency distribution of IMDb scores; reveals the true shape of audience judgment
- **Interactive Filters** — Genre, Year Range, Minimum Vote Count (to filter out low-sample outliers)

---

## 🏗️ Dashboard Architecture

```
IMDb Dataset (CSV)
     │
     ▼
Tableau Data Layer
├── Data Cleaning: Null handling (missing ratings, runtime, genre)
├── Calculated Fields:
│   ├── Decade (FLOOR([Year]/10)*10)
│   ├── Rating Bucket (for distribution bins)
│   └── Vote-Weighted Average Rating
├── Parameters: Year Range Slider, Genre Multi-select
└── Data Types: Genre parsed from pipe-delimited string
     │
     ▼
Dashboard Sheets
├── Sheet 1: Genre Avg Rating Bar Chart
├── Sheet 2: Movies Per Decade Area Chart
├── Sheet 3: Top 20 Movies Table (sorted by rating, min 10K votes)
├── Sheet 4: Director Scatter (movies count vs. avg rating)
├── Sheet 5: Runtime Box Plot by Genre
└── Sheet 6: Rating Distribution Histogram
     │
     ▼
Published Tableau Workbook (.twb)
```

---

## 🧰 Tech Stack

| Tool | Purpose |
|---|---|
| **Tableau Desktop** | Primary visualization and dashboard engine |
| **IMDb Public Dataset** | Source data (movies, ratings, crew metadata) |
| **Calculated Fields** | Decade bucketing, vote-weighted ratings, genre parsing |
| **Tableau Filters & Actions** | Interactive cross-filtering between views |

---

## 🚀 Getting Started

### Prerequisites

- [Tableau Desktop](https://www.tableau.com/products/desktop) (2020.1+) or [Tableau Public](https://public.tableau.com/)

### Setup

```bash
git clone https://github.com/Shubh1015/IMBD-Project.git
cd IMBD-Project
```

Open `IMBD Project.twb` in Tableau Desktop or Tableau Public.

> **Note:** If the data connection is broken, re-point the data source to the IMDb dataset (title.basics + title.ratings from [datasets.imdbws.com](https://datasets.imdbws.com/)).

---

## 📸 Dashboard Preview

```
[ Screenshot: IMDb_Dashboard.png ]
```

---

## 📊 Key Analytical Findings

*(Inferred from standard IMDb dataset analysis patterns)*

- **Documentary** and **Biography** genres consistently earn higher average IMDb ratings than mainstream genres like Action and Comedy
- Average ratings have trended slightly downward post-2000, likely reflecting the massive increase in total titles produced
- Movies with runtime between **90–120 minutes** receive the highest average audience ratings
- A small cluster of directors (Nolan, Spielberg, Kubrick) appear as outliers — high movie count AND high average rating

---

## 🔮 Future Enhancements

- [ ] Integrate box office gross data (from Box Office Mojo) to correlate ratings with commercial success
- [ ] Add language/country dimension for international cinema analysis
- [ ] Build a "similar movies" recommendation logic using genre + rating proximity
- [ ] Publish interactive version to Tableau Public with embedded URL

---

## 🤝 Contributing

Pull requests and analytical improvements are welcome. Please open an issue describing the enhancement before submitting a PR.

---

## 📄 License

MIT License. IMDb data is sourced from IMDb's publicly available non-commercial datasets and is used here for educational purposes only.

---

## 🏷️ Topics

tableau  imdb  movie-analytics  entertainment-analytics  data-visualization  film-industry  data-analysis
