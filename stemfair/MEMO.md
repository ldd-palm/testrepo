# Sprint vs. Marathon, Nevada’s Warming Race

**Finished:** March 5, 2026

I live in Nevada, and in the past few years I’ve felt like summers are getting hotter and winters are getting warmer in Elko. I wanted to know if that feeling matches real data. I also wondered how Elko compares with Reno and Las Vegas, and what warming could mean for daily life.

This project uses official NOAA climate data to answer three questions:
(1) Are annual average temperatures in Elko, Reno, and Las Vegas increasing over the last ~50 years?
(2) Which city is warming the fastest (the “sprint vs. marathon” idea)?
(3) In Elko, does warming affect heating and cooling demand?

The data in this folder comes from NOAA Climate Data Online (CDO). I used long-term airport weather stations because they have consistent records over many decades: Elko Regional Airport (USW00024121), Reno Airport (USW00023185), and Las Vegas (McCarran/Harry Reid) (USW00023169).

To compare warming fairly, I used **temperature anomalies** instead of raw temperatures. Las Vegas is naturally hotter than Elko, so raw temperatures don’t show which city is warming faster. An anomaly is the year’s temperature minus that city’s average during a baseline period. For this project, the baseline is **1975–2000**. Then I used a simple **linear trend** to summarize warming rate in **°F per decade**.

To connect climate to real life in Elko, I used **Heating Degree Days (HDD)**. HDD estimates how much heating is needed by adding up how far the daily average temperature is below a base temperature (often 65°F). Colder days add more HDD; warm days add zero. Lower HDD usually means less heating is needed.

Overall, the results show that all three cities have warmed over time, and the warming rates are not identical. In Elko, warming can mean less heating demand and more hot-day exposure.

## What I learned (why 30 years?)

Before this project, I thought climate was just “average weather.” Now I understand why scientists often use **30-year climate normals**. Weather changes a lot from year to year, so a 30-year average helps smooth out the ups and downs while still representing today’s climate.

## Event information

This project was prepared for the ECSD STEM Fair 2026. According to the ECSD STEM Fair website, the fair is held at the Elko Convention Center and the district fair dates are March 9–12.  
Website: https://sites.google.com/ecsdnv.net/2026-ecsd-stem-fair/home

## Folder guide (what each file is for)

The final poster is in `stemfair/final/` as `stemfair_final_poster.pdf`.

A table used to calculate annual average temperatures and generate the annual temperature chart in the poster is in `stemfair/data_sources/` as `poster_source_annual_avg_temp_3cities_1975-2025.csv`.

The large daily data downloads from NOAA CDO are stored as:
- `stemfair/elko_1975-2026.csv`
- `stemfair/reno_1975-2026.csv`
- `stemfair/lasvegas_1975-2026.csv`

The selected, poster-ready SVG charts are in `stemfair/svt_charts/` (see `stemfair/svt_charts/README_svt_charts.md`).
