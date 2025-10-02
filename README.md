# Bike Sharing Demand — Mini EDA

Mini exploratory analysis of bike rental demand using the UCI Bike Sharing (hourly) dataset.  
We keep it simple: **pandas + matplotlib** (no seaborn). The goal is to answer **when** demand peaks:
- Hourly profile (0–23)
- Weekday × Hour heatmap (7 × 24)
- Monthly seasonality (1–12)

> Script: `bike_demand_mini.py`  
> Figures are saved under `figs/`.

---

## Dataset

This project expects a UCI Bike Sharing–style `hour.csv` (or similar) with at least:
- `date` or `dteday` (daily date)
- `hour` (0..23)
- `weekday` (0=Mon .. 6=Sun)
- `mnth` or `month` (1..12)
- `cnt` (total rentals that hour)

If your columns use slightly different names (e.g., `dteday`, `hr`, `mnth`), the script maps common variants automatically.

**Note:** The dataset is **not** included in the repo. Place your CSV next to the script or update `CSV_PATH` inside `bike_demand_mini.py`.

---

## What’s inside

- **Hourly profile** — 24-point line plot of average rentals by hour  
- **Weekday × Hour heatmap** — 7×24 grid showing average rentals  
- **Monthly seasonality** — bar chart of average rentals by month  
- Console readouts:
  - Top/lowest hours (by average `cnt`)
  - Top/lowest months (by average `cnt`)
  - Heatmap max/min cell values
  - A short “Quick Findings” stub you can edit

---

## Quick start

```bash
# 1) Create and activate a virtual env (optional but recommended)
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

# 2) Install dependencies
pip install -r requirements.txt

# 3) Put your hour.csv next to the script (or edit CSV_PATH in the script)

# 4) Run
python bike_demand_mini.py
