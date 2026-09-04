# Global-Economy-Indicators
Interactive Power BI dashboard analyzing global economic indicators (1970–2021) across 220+ countries. Features custom DAX measures for GDP, per capita wealth, population, trade balance, and industry sector composition (Agriculture, Manufacturing, Services). Includes time-series trends, top-N rankings, and interactive multi-variable filtering.
# 🌍 Global Economy Indicators Analysis & Power BI Dashboard (1970–2021)

An end-to-end interactive Power BI dashboard analyzing global macroeconomic indicators, GDP growth trends, population dynamics, and industry sector breakdowns across 220+ countries over a 50-year period.

![Dashboard Preview](Screenshots/dashboard_overview.png)

---

## 📌 Project Overview
This project cleans, models, and visualizes global economic data from 1970 to 2021. It provides key insights into trade balances, manufacturing shares, GDP per capita growth, and industrial composition.

## 🛠️ Tools & Technologies Used
* **Power BI Desktop:** DAX measures, dynamic slicers, interactive visuals.
* **Power Query:** Data cleaning, custom transformations, and header standardization.
* **Excel / CSV:** Initial data structure validation.

---

## 📊 Key Insights & Features
* **Global Macro Trends:** Tracks total global GDP growth from ~$3.4T in 1970 to ~$95.8T in 2021.
* **Top Economies Ranking:** Dynamic top-N visual showing historical shifts in global economic powerhouses.
* **Sector Composition Analysis:** Detailed breakdown of Agriculture, Manufacturing, and Services (`ISIC G-H`, `ISIC I`, `ISIC J-P`).
* **KPI Ribbon:** Real-time metrics for Total GDP, Population, GDP Per Capita, and Net Trade Balance.

---

## 📐 Key DAX Measures Used
```dax
Total GDP = SUM('Global Economy Indicators'[Gross Domestic Product (GDP)])

GDP Per Capita = DIVIDE([Total GDP], SUM('Global Economy Indicators'[Population]), 0)

Net Exports = SUM('Global Economy Indicators'[Exports of goods and services]) - SUM('Global Economy Indicators'[Imports of goods and services])
