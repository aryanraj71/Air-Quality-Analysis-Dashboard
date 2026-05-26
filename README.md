# Air Quality Analysis & Interpretation Dashboard 🌬️📊

A comprehensive **Power BI Dashboard** project analyzing urban air quality, pollutant dynamics, and seasonal trends across major cities. This project integrates Exploratory Data Analysis (EDA), Statistical Analysis, Unsupervised Machine Learning (K-Means Clustering), and interactive visualization to deliver actionable environmental insights.

Developed by: **Aryan Raj**  
*B.Tech CSE Data Science | University of Petroleum and Energy Studies (UPES), Dehradun*

---

## 📌 Project Overview
Urban air pollution is a critical public health and environmental crisis. This dashboard provides a holistic view of pollution levels, seasonal trends, and pollutant behavior. By visualizing clusters, correlations, and comparisons, it enables stakeholders to identify high-risk zones, dominant pollutants, and temporal patterns to support data-driven policy decisions.

### Key Tools & Technologies:
*   **BI Platform**: Power BI Desktop
*   **Data Prep & Processing**: Power Query, DAX (Data Analysis Expressions)
*   **Machine Learning**: Python integration in Power BI (K-Means Clustering)
*   **Dataset**: `city_day.csv` (containing daily city-level air quality parameters like AQI, PM2.5, PM10, NO2, SO2, CO, etc.)

---

## 🖥️ Dashboard Architecture & Pages

The dashboard is structured into three primary pages:

### Page 1: Exploratory Data Analysis (EDA) Insights
Explore pollutant variations, distribution patterns, and relationships between key air quality indicators.
*   **Seasonal Pollutant Variation (Heatmap)**: Analyzes how weather dynamics drive pollutant concentrations (e.g., PM2.5 and PM10 showing peak average values in monsoon and summer).
*   **PM2.5 Distribution**: A right-skewed histogram indicating that while most days are moderately polluted, periodic extreme pollution spikes occur due to episodic events.
*   **Pollutant Relationships (Scatter Plot)**: A scatter plot of PM10 vs PM2.5 showing a strong positive correlation, indicating shared emission origins (traffic, combustion, and dust). Delhi displays the highest risk exposure.
*   **Seasonal Fluulations (Boxplot)**: Shows seasonal meteorological behaviors driving fluctuations, with summer and monsoon showing higher median values.
*   **Yearly Trends**: Displays fluctuating improvement and worsening patterns from 2015 to 2024, showing a sharp rise in 2020 followed by gradual declines, emphasizing the need for persistent urban policies.

🖼️ *Visualizations from the EDA section:*
![EDA Heatmap](assets/eda_heatmap.png)
![EDA PM2.5 Distribution](assets/eda_pm25_distribution.png)
![EDA PM10 vs PM2.5 Scatter](assets/eda_pm10_vs_pm25.png)
![EDA Seasonal Boxplot](assets/eda_seasonal_boxplot.png)
![EDA Yearly Trend](assets/eda_pm25_yearly_trend.png)

---

### Page 2: Statistical Analysis & K-Means Clustering Insights
Combining inferential statistics with unsupervised machine learning to group cities based on pollution severity.
*   **Seasonal Differences**: Statistically confirms that season strongly impacts air quality, with Summer (~254 µg/m³) and Monsoon (~261 µg/m³) showing significantly higher average PM2.5 compared to Winter (~248 µg/m³).
*   **City Segmentation (K-Means)**: Segments cities into three distinct clusters:
    *   🟢 **Cluster 1 (Low Pollution)**: Residential or strictly regulated zones with cleaner profiles.
    *   🟡 **Cluster 2 (Moderate Pollution)**: Transitional cities experiencing mixed industrial and urban activity.
    *   🔴 **Cluster 3 (High Pollution)**: Highly industrial, traffic-dense cities with elevated health risks.
*   **Particulate Corelation**: Confirms that rising fine particulate matter (PM2.5) corresponds directly to rising dust pollution (PM10), indicating shared emission origins.

🖼️ *Clustering Visuals:*
![K-Means Clustering](assets/clustering_kmeans.png)
![Clustering Details](assets/clustering_details.png)

---

### Page 3: Filter-Interactive Dashboard
A dynamic, customizable reporting view allowing users to slice and dice the data for customized insights.
*   **Interactive Slicers**: Filter by **City, Year, Season, and Month** to perform localized root-cause analysis.
*   **AQI & Particulate Tracker**: Monitor how average AQI levels remain consistently high (typically in the 250-260 range), indicating a universally polluted urban environment.
*   **Pollutant-wise Breakdown**: Tracks specific pollutant levels over time, revealing that while SO2 and NO2 remain low, PM10 remains significantly higher and remains the critical driver of poor AQI.

🖼️ *Interactive Views:*
![Interactive Filter Dashboard Overview](assets/dashboard_overview.png)
![Interactive Dashboard Details](assets/dashboard_details.png)

---

## 📈 Key Insights & Recommendations
1.  **Particulate Matter Dominance**: PM10 and PM2.5 are the primary pollutants. Emission controls must focus heavily on vehicular emissions, construction dust, and industrial combustion.
2.  **Regional Policy Approach**: Since major cities share similar pollution shares (18-20% contribution each), isolated city-level policies are insufficient. Regional airshed management is essential.
3.  **Seasonal Interventions**: Stricter emission caps should be enforced dynamically during summer and monsoon seasons when meteorological factors exacerbate pollution accumulation.

---

## 📂 Repository Structure
```directory
.
├── assets/                          # High-resolution dashboard screenshots (PNG)
│   ├── dashboard_overview.png       # Interactive dashboard overview
│   ├── dashboard_details.png        # Interactive dashboard charts
│   ├── eda_heatmap.png              # Seasonal variation heatmap
│   ├── eda_pm25_distribution.png    # Histogram distribution
│   ├── eda_pm10_vs_pm25.png         # Scatter correlation plot
│   ├── eda_seasonal_boxplot.png     # Boxplot
│   ├── eda_pm25_yearly_trend.png    # Line chart trend
│   ├── clustering_kmeans.png        # K-Means clustering graph
│   └── clustering_details.png       # Clustering statistics
├── AirQuality_Analysis_Report.pdf   # Detailed PDF Project Report
├── city_day.csv                     # Raw air quality dataset
├── AirQuality_Analysis.pbix         # Power BI Desktop source file (3 Pages)
└── README.md                        # Project documentation (this file)
```

---

## 🚀 How to Run the Project
1.  **Clone the repository**:
    ```bash
    git clone https://github.com/aryanraj71/Air-Quality-Analysis-Dashboard.git
    cd Air-Quality-Analysis-Dashboard
    ```
2.  **Open in Power BI**:
    *   Make sure you have [Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed.
    *   Double-click `AirQuality_Analysis.pbix` to launch the dashboard.
3.  **Verify Python Script Integration (Optional)**:
    *   For K-Means clustering visual execution, ensure Python is installed and configured in Power BI: `Options and settings > Options > Python scripting`.
    *   Required libraries: `pandas`, `scikit-learn`, `matplotlib`.
