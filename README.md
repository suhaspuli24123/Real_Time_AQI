# Real_Time_AQI
## Project Overview
This project is analyses Air Quality Index across different cities in India.It aims to provide insights into pollution levels,distribution across regions, identify major pollutants, and observe relationships among key air quality parameters such as PM2.5, PM10, NO₂, CO, SO₂, NH₃, and O₃ by using visualisation techniques.

### Technical implementation
- **Language**: Python  
- **Libraries**: Pandas, Matplotlib, NumPy, Seaborn
- **Plots Used**: Bar, Cluster bar, HeatMap, Box, Scatter
- **Analysis Methods**: Correlation analysis, Outlier detection, Trend analysis
  
## Dataset
The dataset used in this analysis was obtained from the Government of India's Open Data Platform.

**Source**: [data.gov.in](https://www.data.gov.in/resource/covid-19-district-wise-abstract-cases-including-active-cases-discharges-and-deaths-295)

**Dataset**: It provides real-time national Air Quality Index (AQI) values from different monitoring stations across India. 

**Dataset Details**:
- Period: Single-day snapshot( 05-10-2025)
- No.of Pollutants: 7
- Area Covered: 237 Cities across India

## Data Preprocessing: 
1. Rows where all pollutant values were missing (pollutant_min, pollutant_max, pollutant_avg) were identified and dropped.
2. Added new columns for each pollutant to get insights about each pollutant in each location.

## Exploratory Data Analysis
The analysis employed four major visualization techniques:

### **1. Bar plot**:
- Plotted Bar plots to gain insights about top 10 pollluted cities and pollution levels in these cities.
<img width="1000" height="500" alt="barplot_top10_cities_pollution" src="https://github.com/user-attachments/assets/b8fcc929-623d-486c-a4e9-73a621d3c24f" />


**Observations**: 
- Noida, Gurugram and Delhi appear among the top polluted cities, indicating severe air quality issues compared to less industrial cities.

- Plotted Bar plot for each pollutant and top 10 states in which the pollutant level is high.
  <img width="1500" height="2000" alt="barplot_top10_states_foreachpollutant" src="https://github.com/user-attachments/assets/a2fefe8a-3d6d-489a-9853-7c769d7a6ca7" />


 **Observation**s:
 - Each pollutant shows a different set of states at the top, indicating that pollution sources vary geographically.

### **2. Cluster Bar**:
- Plotted Cluster bar to understand every pollutant concentration in top 10 polluted cities.
- <img width="1200" height="600" alt="clusterbar_top10_cities_pollution" src="https://github.com/user-attachments/assets/5ccf8a93-0d80-4f05-9f2e-0c72f9da1364" />


**Observations**:

- This Cluster bar chart tells about contibution of each pollutant to total pollution in top 10 polluted cities of India.

- Most of the cities are effected by PM2.5 and PM10.

### **3. Box Plot**:
- Used box plots to understand concentration of each pollutant across the country.

  <img width="1000" height="600" alt="boxplot_pollutants" src="https://github.com/user-attachments/assets/bbf7d195-e5af-4979-a954-019eecadae94" />

  
**Observations**:

- This Box plot shows the distribution of major air pollutants across the country.

- PM10 and PM2.5 shows the widest spread and highest outliers, indicating reason for severe air quality issues in certain regions.

- SO2 and NH3 have relatively lowest spread.

- Almost all pollutants have skewed distributions with a large number of outliers. This tells that these peaks in certain areas can effect Air Quality of the country.

### **4.Heat Map**:
- Heat map is used to understant the correlation between pollutants.
  
<img width="800" height="600" alt="correlation_pollutants" src="https://github.com/user-attachments/assets/8a9a7f9a-dcda-4a07-bda9-039552ea5fd5" />


**Observations**:
- PM10 and PM2.5 are positively correlated.

- Hence, We can compare these pairs using Scatter plot to get better insights.

### **Scatter plot**:
<img width="700" height="700" alt="scatter_pm10_pm25" src="https://github.com/user-attachments/assets/968bfb74-f6e8-46dd-9c8d-bc248384fe6a" />


**Observations**:

- Most points form a diagonal trend from bottom-left to top-right, showing that PM10 and PM2.5 are directly proportional.

- Dense Cluster is at bottom left, indicating that most observations have low levels of PM2.5 and PM10 i.e, cleaner locations.

- There are no points where PM2.5 is high but PM10 is low i.e, in the bottom right. This aligns with physical reality which says PM2.5 ≤ PM10







