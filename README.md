# Weather Pattern Analysis & Forecasting
### Interactive Data Visualization | CSCE 5320 — University of North Texas

[![Live Webpage](https://img.shields.io/badge/Live%20Webpage-GitHub%20Pages-02C39A?style=for-the-badge)](https://karthik0987.github.io/Data-Visulaization-Final-Project/)
[![Tableau](https://img.shields.io/badge/Tableau-Public-1C7293?style=for-the-badge)](https://public.tableau.com/app/profile/karthik/viz/Project1_17760345128990/Dashboard1)
[![Python](https://img.shields.io/badge/Python-3.10+-0A2342?style=for-the-badge)](https://www.python.org/)

---

## 🌐 Live Interactive Webpage
**[https://karthik0987.github.io/Data-Visulaization-Final-Project/](https://karthik0987.github.io/Data-Visulaization-Final-Project/)**

The webpage contains:
- 9 interactive Plotly charts with hover, zoom, and legend toggle
- Tableau dashboard embedded from Tableau Public
- Power BI report embedded publicly
- Responsive layout with Stage 1 and Stage 2 storytelling sections

---

## 📋 Project Overview

This project analyzes **1.6 million rows** of hourly weather data across **36 cities** in North America and Israel, spanning **5 years (2012–2017)**. The goal was to build interactive visualizations that uncover seasonal patterns, geographic differences, and correlations between weather variables including temperature, humidity, atmospheric pressure, and wind speed.

---

## 📊 Visualizations

| # | Title | Tool | Stage |
|---|---|---|---|
| V1 | Monthly Average Temperature by City | Tableau | Stage 1 |
| V2 | Seasonal Temperature Heatmap | Tableau | Stage 1 |
| V3 | Temperature vs. Humidity Scatter Plot | Tableau | Stage 1 |
| V4 | Temperature vs. Humidity by Season | Tableau | Stage 2 |
| V5 | Seasonal Humidity by City | Tableau | Stage 2 |
| V6 | Average Wind Speed by City | Tableau | Stage 1 |
| V7 | Monthly Atmospheric Pressure Trends | Tableau | Stage 2 |
| V8 | Top 10 Weather Conditions | Tableau | Stage 1 |
| V9 | Yearly Average Temperature Trend | Tableau | Stage 2 |
| PBI-1 | City-Level Temperature — Geographic Map | Power BI | Stage 1 |
| PBI-2 | Wind Speed Distribution | Power BI | Stage 1 |
| PBI-3 | Average Humidity by Season and Country | Power BI | Stage 2 |
| PBI-4 | Average Pressure by City | Power BI | Stage 2 |

---

## 🗂️ Dataset

**Source:** [Kaggle — Global Historical Weather Dataset](https://www.kaggle.com/)

| File | Type | Records |
|---|---|---|
| temperature.csv | Numeric | 45,253 rows |
| humidity.csv | Numeric | 45,253 rows |
| pressure.csv | Numeric | 45,253 rows |
| wind_speed.csv | Numeric | 45,253 rows |
| wind_direction.csv | Numeric | 45,253 rows |
| weather_description.csv | Categorical | 45,253 rows |
| city_attributes.csv | Structured | 36 cities |

After merging: **1,629,108 rows × 15 columns**

---

## 🔧 Data Pipeline

```python
# Key transformation steps
1. Load 7 raw CSVs from Kaggle
2. Linear interpolation for missing numeric values (~1.8%)
3. Forward/backward fill for categorical weather descriptions
4. Convert temperature from Kelvin to Celsius (subtract 273.15)
5. Melt wide format → long format (45,253 × 36 cities = 1.6M rows)
6. Merge all files on datetime + City
7. Add City attributes (Country, Latitude, Longitude)
8. Engineer time features: Year, Month, Hour, Season
```

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Python + Pandas | Data cleaning, merging, feature engineering |
| Plotly | 9 interactive charts embedded on webpage |
| Tableau | 9 visualizations + published dashboard |
| Power BI | 4 interactive report pages |
| HTML/CSS/JavaScript | Interactive webpage |
| GitHub Pages | Free public hosting |

---

## 🚀 How to Run

**1. Clone the repository**
```bash
git clone https://github.com/karthik0987/Final-Project-Data-Vis.git
cd Final-Project-Data-Vis
```

**2. Install dependencies**
```bash
pip install pandas numpy plotly
```

**3. Download the dataset from Kaggle**
Place the 7 CSV files in a `Datasets/` folder.

**4. Run data preprocessing**
```bash
python "Data preprocessing code.py"
```
This generates `weather_master_cleaned.csv`

**5. Generate Plotly charts**
```bash
python make_viz.py
```

**6. Open the webpage**
Open `index.html` in VS Code with Live Server, or visit the live link above.

---

## 📁 Repository Structure

```
Final-Project-Data-Vis/
├── index.html                    # Interactive webpage (all charts embedded)
├── Data preprocessing code.py   # Data cleaning & merging pipeline
├── make_viz.py                   # Plotly chart generation
├── Datasets/                     # Raw CSV files from Kaggle
└── Vis Screenshots/              # Screenshots of all visualizations
```

---

## 🔑 Key Findings

- **Miami** is the warmest city in every season, peaking at **28.15°C** in Summer
- **Toronto** drops to **−2.76°C** in Winter — the coldest value in the dataset
- **Negative correlation** between temperature and humidity — Winter is coolest and most humid, Summer is hottest and driest
- **Houston** shows dramatic atmospheric pressure drops in 2013 and 2017 corresponding to major hurricane events
- **Toronto and Chicago** record the highest average wind speeds due to flat terrain adjacent to large lakes
- Nearly all 10 cities show an **upward warming trend** from 2012 to 2017

---

## 👤 Author

**Etukuri Karthik Choudhary**
MS Computer Science — University of North Texas
[GitHub](https://github.com/karthik0987)

---

## 📚 Course

**CSCE 5320 — Scientific Data Visualization**
University of North Texas | Spring 2026
