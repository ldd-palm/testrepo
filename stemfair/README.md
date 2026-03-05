# Sprint vs. Marathon, Nevada’s Warming Race

## What this project is about
Have you ever felt like **summers are getting hotter** and **winters are getting warmer**?
I live in Nevada, and I wondered:

- Is Nevada really getting warmer?
- Is Elko changing a lot?
- How do Elko, Reno, and Las Vegas compare?
- If it’s warmer, does that change how much we need heating or cooling?

So I used real climate data to find out.

---

## Event info (ECSD STEM Fair 2026)
From the ECSD STEM Fair website:
- **Where:** Elko Convention Center
- **When:** **March 9–12**
- Website: https://sites.google.com/ecsdnv.net/2026-ecsd-stem-fair/home

---

## My research questions (RQs)
**RQ1:** Are the annual average temperatures in **Elko, Reno, and Las Vegas** increasing over the past ~50 years?

**RQ2:** Which city is warming the fastest: **Elko, Reno, or Las Vegas**? (That’s the “Sprint vs. Marathon” part.)

**RQ3:** How do temperature changes affect **heating and cooling demand** in Elko?

---

## Data source (official climate data)
All the weather data in this folder comes from **NOAA** (National Oceanic and Atmospheric Administration), using **NOAA Climate Data Online (CDO)**.

I used long-term airport weather stations:
- **Elko Regional Airport:** USW00024121
- **Reno Airport:** USW00023185
- **Las Vegas (McCarran/Harry Reid):** USW00023169

---

## How I did it (simple method)
### 1) Annual average temperature (for RQ1)
- I used monthly averages to make a yearly average temperature for each city.

### 2) Anomaly + trend (for RQ2)
- Cities have different normal temperatures (Las Vegas is always hotter than Elko).
- To compare fairly, I used **temperature anomaly**:
  - Anomaly = (year’s temperature) − (that city’s average from **1975–2000**)
- Then I used a **linear trend line** to compare warming speed (°F per decade).

### 3) Heating and cooling (for RQ3)
To connect climate to real life, I used:
- **HDD65 (Heating Degree Days):** bigger HDD means a colder year (more heating needed)
- **Hot days (TMAX ≥ 90°F):** more hot days means more cooling stress

---

## What I found (short version)
- All three cities show warming over time.
- The warming rate is not exactly the same in each city.
- In Elko, warming can mean **less heating needed** (lower HDD) and **more hot days**.

---

## What is inside this GitHub folder?

### `stemfair/final/`
- `stemfair_final_poster.pdf` — my final poster
- `COMMENT.txt` — a short note saved with the poster

### `stemfair/data_sources/`
- `poster_source_annual_avg_temp_3cities_1975-2025.csv`
  - The table I used to calculate annual average temperature and make the temperature chart in the poster.

### Base daily downloads (NOAA CDO exports)
These are the big daily data files downloaded from NOAA:
- `stemfair/elko_1975-2026.csv`
- `stemfair/reno_1975-2026.csv`
- `stemfair/lasvegas_1975-2026.csv`

### Charts
- `stemfair/svt_charts/` — the SVG charts I selected (poster-ready)
  - Start with `stemfair/svt_charts/README_svt_charts.md`

---

## Extra notes
- Climate scientists often use **30-year climate normals** because 30 years is long enough to smooth out year-to-year weather changes, but still shows what the climate is like now.
