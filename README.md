# Smart Urban Mobility and Traffic Intelligence Dashboard

## 📌 Project Overview

The **Smart Urban Mobility and Traffic Intelligence Dashboard** is a Power BI-based data analytics project designed to analyse urban mobility patterns, transportation demand, accessibility, reliability, and mobility equity.

The project uses data modelling, DAX calculations, interactive visualizations, demand forecasting, and anomaly detection to help users explore mobility performance and identify patterns that can support data-driven decision-making.

## 🎯 Objectives

- Analyse urban mobility demand and transportation patterns.
- Compare mobility accessibility across different locations and analytical demographic groups.
- Evaluate transportation reliability and travel time.
- Develop a composite Mobility Access Index.
- Explore historical demand patterns and forecast future demand.
- Identify unusual demand observations using anomaly detection.
- Present key insights through interactive Power BI dashboards.

## 🛠️ Tools and Technologies

- **Microsoft Power BI** — Dashboard development and data visualization
- **DAX (Data Analysis Expressions)** — Calculated columns, measures, and analytical indicators
- **Data Modeling** — Fact and dimension tables with relationships
- **Time-Series Forecasting** — Forecasting based on historical mobility demand
- **Data Analytics** — Accessibility, reliability, equity, and anomaly analysis

## 📊 Dashboard Pages

### 1. Executive Intelligence Dashboard

Provides an overview of overall mobility performance through key performance indicators (KPIs):

- Total Demand
- Total Trips
- Mobility Access Index
- Average Reliability
- Average Fare

**Visualizations include:**
- Mobility Demand Trends
- Trips by Transport Mode
- Travel Time by Area
- Demand by Location map
- Average Reliability by Transport Mode

This page helps users understand demand trends, compare transport modes, and explore the geographical distribution of mobility activity.

### 2. Mobility Equity and Access Index

Focuses on comparing accessibility-related conditions across areas and analytical demographic groups.

**Key performance indicators:**
- Mobility Access Index
- Average Reliability
- Average Travel Time
- Total Demand
- Average Fare

**Visualizations include:**
- Mobility Access by Area
- Mobility Access Index by Demographic Group
- Total Trips by Accessibility Status
- Mobility Access Equity Matrix

Interactive filters for area, demographic group, and transport mode allow users to explore specific segments and compare mobility conditions.

### 3. Demand Forecasting and Anomaly Detection

Focuses on historical demand analysis, potential future demand, and unusual observations.

**Features include:**
- Total Demand KPI
- Historical demand forecasting
- Demand categorization into High, Medium, and Low
- Anomaly detection for unusual demand patterns

The forecasting visual uses the date field on the X-axis and Total Demand on the Y-axis. The documented configuration uses a forecast length of 30 periods and a 95% confidence interval.

Forecasting estimates potential future demand from historical observations, while anomaly detection helps identify unusual spikes or drops in demand.

## 🧮 Key Analytical Indicators

### Mobility Access Index

The Mobility Access Index combines three normalized indicators:

1. Accessibility Score
2. Average Reliability
3. Bike Availability

The three components are normalized to a 0–100 scale and averaged to obtain a composite score.

### Accessibility Score

The Accessibility Score is based on the availability of nearby facilities represented in the location data, including:

- Hospitals
- Markets
- Schools

It provides an analytical indication of accessibility based on the available facility indicators.

### Average Reliability

Average Reliability is calculated using average delay relative to maximum delay:

`Average Reliability = (1 - AvgDelay / MaxDelay) × 100`

A zero-maximum-delay safeguard is used to avoid division by zero. Lower average delay results in a higher reliability score under this formula.

### Demand Category

Demand observations are classified into **High**, **Medium**, and **Low** categories based on the distribution of `Passenger_Count`.

### Accessibility and Equity Status

Threshold-based classifications are used to identify accessibility and equity conditions. For example, an accessibility score of 70 or above is classified as Accessible, while lower scores are classified as Underserved.

## 🗂️ Data Modeling

The project uses a star-schema-style data model with `FactMobilityTable` at the center and related dimension tables.

| Table | Purpose |
|---|---|
| `FactMobilityTable` | Stores mobility-related records and measurable values |
| `Dim_Date` | Provides date-related attributes |
| `Dim_Location` | Provides location-related information |
| `Dim_Route` | Provides route-related information |
| `Dim_Vehicle` | Provides vehicle-related information |
| `Dim_Weather` | Provides weather-related information |

The documented dataset contains 300 mobility records. The existing data model is reused for the advanced analytics implemented in Milestone 4.

## 🔄 Project Workflow

1. Integrate and prepare the mobility data.
2. Build and validate the fact-and-dimension data model.
3. Develop measures and calculated columns using DAX.
4. Create the Executive Intelligence Dashboard.
5. Analyse mobility accessibility and equity.
6. Explore demand forecasting and anomaly detection.
7. Validate KPI calculations, filtering behaviour, and dashboard consistency.

## ✨ Key Features

- Interactive KPI cards and visualizations
- Mobility demand and transport-mode comparisons
- Location-based mobility analysis
- Composite accessibility and reliability indicators
- Accessibility and equity comparisons
- Historical demand forecasting
- Anomaly detection
- Interactive filters for exploring mobility segments
- Integrated three-page Power BI dashboard

## ⚠️ Limitations

- Accessibility scores depend on the available nearby-facility indicators.
- Demographic groups are analytical categories rather than direct demographic survey results.
- Accessibility and equity statuses are derived classifications based on defined thresholds.
- Bike availability is represented by a proxy based on the share of motorcycle records; it does not represent real-time bicycle inventory.
- Forecasting and anomaly detection are limited by the available historical dataset and its time coverage.
- Map visualization availability may depend on Power BI's map service configuration.

These limitations should be considered when interpreting the dashboard's results.

## 🚀 How to Use

1. Clone or download this repository.
2. Open the Power BI project file (`.pbix`) included in the repository, if provided.
3. Ensure that the dataset and any required data-source paths are available.
4. Refresh the data if necessary.
5. Navigate through the three dashboard pages.
6. Use the available filters to compare locations, demographic groups, and transport modes.
7. Explore historical demand, forecasting, and anomaly detection results.

**Note:** The Power BI project file and dataset must be included in the repository for the project to be opened and refreshed as described above. Update any local data-source paths if required.

## 🔮 Future Enhancements

- Integrate larger and more recent mobility datasets.
- Incorporate real-time transportation and bike-availability data.
- Improve accessibility analysis with verified facility and demographic data.
- Evaluate forecasting accuracy using additional historical observations.
- Extend anomaly detection with more advanced statistical or machine-learning techniques.
- Add further geographical and temporal comparisons.

## 🏁 Conclusion

The Smart Urban Mobility and Traffic Intelligence Dashboard extends mobility data analysis through executive reporting, accessibility and equity analysis, demand forecasting, and anomaly detection.

By combining Power BI visualizations, DAX-based indicators, and an organized data model, the project provides an interactive way to explore urban mobility patterns and support informed decision-making.

## 👥 Team Project

This project was developed collaboratively as part of an internship project focused on **Smart Urban Mobility and Traffic Intelligence**. Teamwork and collaboration supported the development, analysis, validation, and presentation of the dashboard.

---

**Project Domain:** Data Analytics and Business Intelligence  
**Primary Tool:** Microsoft Power BI  
**Key Concepts:** DAX, Data Modeling, Mobility Analytics, Accessibility Analysis, Forecasting, and Anomaly Detection
