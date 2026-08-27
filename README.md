# FIFA World Cup 2026 — Data Analysis & Power BI Dashboard
--------------------------------------------------------------------
An end-to-end data project covering the 2026 FIFA World Cup (USA, Canada & Mexico): web scraping, data cleaning, and an interactive, stadium-themed Power BI dashboard built with custom HTML visuals.
<img width="1358" height="766" alt="Screenshot 2026-08-28 013824" src="https://github.com/user-attachments/assets/3b981d46-5370-46a6-a914-da7505d9e153" />
---------------------------------------------------------------------------------------------------------

## 📌 Overview

This project explores the 2026 FIFA World Cup — the first edition hosted by three countries (USA, Canada, Mexico) and the first to feature 48 teams. It walks through the full pipeline:

1. **Web Scraping** — collecting raw World Cup data with Python.
2. **Data Cleaning** — structuring and cleaning the scraped data with Python (Pandas).
3. **Dashboard Design** — building an interactive, visually immersive dashboard in Power BI, enhanced with custom HTML/CSS visuals for a stadium-night theme.

---

## 🗂️ Datasets

All cleaned datasets are provided as CSV files, ready to plug into Power BI, Excel, or any BI/analysis tool.

| File | Description | Rows |
|---|---|---|
| `world_cup_2026_full_dataset.csv` | Full match-by-match dataset: date, time, stage, teams, score, stadium, city, attendance, referee, scorers, penalty shootouts | 104 |
| `world_cup_2026_group_standings.csv` | Group stage standings for all 12 groups (played, won, drawn, lost, GF, GA, GD, points, qualification status) | 48 |
| `world_cup_2026_all_goals.csv` | Every individual goal scored in the tournament, with match number, scorer, team, minute, and own-goal flag | 308 |
| `world_cup_2026_scorers.csv` | Full list of goal scorers with team and goal count | 182 |
| `top_10_scorers.csv` | Top 10 scorers with Arabic/English names, teams, and player image links | 10 |
| `world_cup_2026_stadiums.csv` | All 16 host stadiums with city, matches hosted, and seating capacity | 16 |

**Data notes:**
- Text fields are bilingual-friendly (Arabic team/player/city names) to support an Arabic-first dashboard.
- Dates, scores, and numeric fields were cleaned and standardized during the Python cleaning stage (e.g., consistent date formats, numeric attendance/capacity fields, unified team names across files).

---

## 🐍 Web Scraping & Cleaning

- **Language:** Python
- **Libraries:** `requests`, `BeautifulSoup4`, `pandas`
- **Process:**
  1. Scraped raw World Cup 2026 data (teams, fixtures, results, stadiums, scorers) from web sources.
  2. Parsed and extracted the relevant fields using BeautifulSoup.
  3. Cleaned the data with Pandas — handling missing values, unifying naming conventions, fixing data types, and splitting/merging columns where needed.
  4. Exported clean, analysis-ready CSV files (listed above).

A sample scraper (for reference/methodology) is included in [`wikipedia_scraper.py`](./wikipedia_scraper.py), demonstrating the scraping approach used to pull structured content (headings, tables, paragraphs, references) from Wikipedia pages with BeautifulSoup.

---

## 📊 Power BI Dashboard

The dashboard is built in **Power BI Desktop**, combining native visuals with **custom HTML content visuals** to create a stadium-at-night theme (glassmorphism cards, stadium background, gold/blue color palette).

### Pages

| Page | Highlights |
|---|---|
| **Home** | Hero banner, tournament summary (48 teams, 104 matches, one champion), scrollable card carousel of all 48 qualified teams with FIFA rank & World Cup history |
| **Teams** | Groups overview, qualified vs. eliminated teams, Round of 32 qualification donut chart, full scorers table |
| **World Cup** | Tournament-wide KPIs (total goals, matches, stadiums), full group standings table with sorting |
| **Matches** | Match-by-match table with date, time, stage, teams, score, stadium, referee, and attendance; KPIs for matches played, goals conceded, and average goals per match |
| **Performance** | Stadium-level performance: matches hosted, capacity, and total/declining attendance trend by stadium (line chart) |
| **Top Players** | Interactive top-scorer explorer — click a player avatar to reveal their profile, team, world ranking, and goal tally |

### Tech used for the visuals

- **Power BI** native visuals (tables, cards, donut chart, line chart)
- **HTML/CSS** content visuals for the stadium background, glass-effect cards, hero section, and the interactive player-selector wheel

---

## 🛠️ Tools & Tech Stack

- **Python** — scraping & data cleaning (`requests`, `BeautifulSoup4`, `pandas`)
- **Power BI Desktop** — data modeling & dashboard
- **HTML/CSS** — custom visual styling inside Power BI
- **Excel/CSV** — data storage format

---



## 📄 License

This project is for educational and portfolio purposes. Data is aggregated from publicly available sources.
