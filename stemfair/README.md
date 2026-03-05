# Sprint vs. Marathon, Nevada's Warming Race

This folder contains the data and figures used for the STEM fair poster **“Sprint vs. Marathon, Nevada's warming race”**.

## Event Information (ECSD STEM Fair 2026)
Source: Elko County School District STEM Fair website
- **Venue:** Elko Convention Center (Elko County, Nevada)
- **District STEM Fair dates:** **March 9–12**
- **Eligibility note (from the event website):** Students must contact their school STEM Fair Representative; participants must live within the physical boundaries of ECSD.
- **Advancement (from the event website):** Top projects may qualify for **Regeneron ISEF**.

Event link: https://sites.google.com/ecsdnv.net/2026-ecsd-stem-fair/home

## Project Summary
Many people in Elko feel that summers have become hotter and winters have become warmer. This project tests that idea using **official NOAA climate data**.

### Objectives / Research Questions
**RQ1:** Are annual average temperatures in **Elko, Reno, and Las Vegas** increasing over the past ~50 years?

**RQ2:** Which city has the highest warming rate: **Elko, Reno, or Las Vegas**? (Sprint vs. Marathon)

**RQ3:** How do temperature changes affect **heating and cooling demand** in daily life in **Elko**?

## Data Sources
All climate data used here are from **NOAA NCEI** (via **NOAA Climate Data Online (CDO)**), using airport stations for long-term records.

Key stations (GHCND IDs used in downloads):
- Elko Regional Airport: **USW00024121**
- Reno Airport: **USW00023185**
- Las Vegas (McCarran/Harry Reid): **USW00023169**

## Methods (High-level)
### 1) Annual mean temperature (3-city comparison)
- Compute each city’s annual mean temperature from monthly means (equal month-weighting).

### 2) Warming-rate comparison (anomaly + linear regression)
- Convert each city’s temperatures to **anomalies** relative to a shared baseline period (**1975–2000**).
- Fit a **linear trend** to the anomaly time series for each city.
- Report slope in **°F per decade**.

### 3) Energy-demand indicators for Elko (Goal 2)
- **Heating Degree Days (HDD65):** computed from daily temperatures using base **65°F**.
- **Cooling indicator:** hot days where **TMAX ≥ 90°F**.
- Compare 2001–2025 to the 1975–2000 baseline using **percent change**.

### Data quality rules
- When using year/month completeness, exclude partial years (e.g., 2026 has incomplete months).

## Key Results (Poster-level)
- **All three cities show warming** over the long term.
- **Warming rates differ by city** (trend slopes make the comparison clear).
- In Elko, warming implies **reduced heating demand (lower HDD)** and **increased heat exposure (more hot days)**.

## What’s in this GitHub directory and how to use it
This GitHub repository stores:

### `stemfair/` (this folder)
- `README.md` — this file
- `final/`
  - `stemfair_final_poster.pdf` — the final poster PDF submitted for the fair
  - `COMMENT.txt` — a short note saved with the final PDF
- `data_sources/`
  - `poster_source_annual_avg_temp_3cities_1975-2025.csv` — the table used to calculate annual average temperatures and generate the annual-temperature chart in the poster
  - `elko_1975-2026.csv`, `reno_1975-2026.csv`, `lasvegas_1975-2026.csv` — base daily station downloads (NOAA CDO export)

### Reproducing charts
- You can reproduce charts in **Google Sheets** by importing the CSV files above.
- Suggested workflow:
  1. Import the CSV.
  2. Filter incomplete years.
  3. Compute anomalies (baseline 1975–2000) and/or HDD/Hot-day metrics.
  4. Create line charts and bar charts; add trendlines where appropriate.

## Notes
- Climate is often summarized using **30-year climate normals** to reduce year-to-year “weather noise” while still representing modern conditions.
