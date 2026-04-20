# Jugla v404.02

Junction 2025 hackathon submission — Fortum's "Watt's next? Forecasting energy consumption with AI" challenge.

## What we built

Two models, two time horizons:

- **SARIMAX** (statistical) and **DeepAR-style RNN** (deep learning) trained on Fortum's customer consumption data
- Forecast windows: **48 hours** and **12 months**

External features explored: electricity prices, hourly temperature (open-meteo), heating demand (open-meteo), Finnish industrial productivity and construction output (Eurostat). SARIMAX settled on electricity prices + heating demand; the RNN used the full feature set.

Validation via MAPE — 12-month model trained on 2 years and forecasted year 3; 48-hour model trained on 14 days and forecasted the next 2.

## Team

- **Ernests Pētersons** — modeling, notebook implementation
- **Mārtiņš Vīksna** — modeling, notebook implementation
- **Rihards Putāns** — data sourcing and feature selection, presentation

## Contents

- [`Methodology_document.pdf`](Methodology_document.pdf) — full approach
- [`Notebooks/`](Notebooks) — SARIMAX and DeepAR, 48h and 12mo variants
- [`Results_csv/`](Results_csv) — forecast outputs
