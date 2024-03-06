# ESRI-GPSA-S6-Particulate-Matter-Exposure
This exercise demonstrates the spatial analysis method in ArcGIS to interpolate sample points, generating a continuous surface to predict long-term particulate matter exposure. Its aim is to showcase how GIS can be utilized for interpolation tasks.

## Section 5 ##
**Exercise 1: Quantifying Patterns: Missed Trash and Recycling Collection**
- Scenario Overview
  - Grant-funding agency aims to identify high air pollution exposure areas in California, particularly for PM2.5 particulates.
  - PM2.5 particulates pose health risks including lung disease and cancer.
  - Elevated levels near major roads due to vehicle emissions, other sources include industry, non-smokeless fuels, and wildfires.
  - PM2.5 particulates are light, remain airborne for long periods, and can travel long distances.
  - Certain populations, like those aged 65+, are more vulnerable to harm from fine particulate matter.
    
- Objectives
  - Conduct environmental analysis to identify areas exceeding California's ambient air quality standards.
  - Produce a map displaying high particulate matter exposure areas and populations aged 65+.
    
- Approach
  - Begin with spatial analysis approach by asking:
    - Where are people more exposed to air pollution in California?
    - What data is required for analysis, and how can GIS represent, analyze, and assess it?
  - Identify areas exceeding state regulation values for particulate matter.
  - Determine locations with high particulate matter levels and significant populations aged 65 and above.

1. Exercise Steps
   
   **Data Exploration and Preparation:**
   - Map displays 98 PM2.5 monitoring sites, often in residential areas, with attributes such as location and exposure readings.
   - Populated Places layer shows areas with 200+ residents aged 65 and older, detailing population demographics.
   - Choropleth map design uses grayscale to emphasize PM2.5 values and graduated colors for population density.
     <img width="934" alt="Screenshot 2024-02-28 195545" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/72092cf2-ca7e-4483-bf33-385c5e166b08">

   - Long-term PM2.5 exposure increases age-specific mortality risk, aiding in establishing cardiopulmonary rehabilitation centers.

  **Data Analysis and Modeling:**
   - By selecting PM2.5 monitoring sites in areas with 200+ residents aged 65 years and older the map updates to display monitoring sites in these areas, symbolized with blue circles.
     <img width="935" alt="Screenshot 2024-02-28 195623" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/b47481c0-dd02-493c-8467-d94817da35d3">

   - Analysis reveals 81 monitoring sites in populated areas meeting age criteria.
   - Approximately 83% of total monitoring sites are in areas with 200+ elderly residents, ensuring good statewide coverage.
   - It is possible to utilize Find Closest analysis tool to identify nearest monitoring site to each populated place within a 120-mile range.
   - Analysis results in connecting lines from Populated Places features to nearest monitoring sites.
   - Nearest Monitoring Sites To Populated Places - Nearest Features layer covers Annual PM2.5 Monitoring Sites layer, facilitating identification of closest sites.#
     <img width="935" alt="Screenshot 2024-02-28 201158" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/65c276b2-b243-4b62-a559-7263559595ed">
     
   - 


    
  **Interpret results**
  - Map displays populated areas with predicted PM2.5 exposure exceeding California standards (12 μg/m³).
  - 247 locations exceed state standards, with exposure levels greater than 12 μg/m³.
  - Configured pop-ups showing total population and population aged 65 and older for areas exceeding standards.

  **Repeat or modify**
  - Other factors like proximity to heavily traveled roads and nearby particulate matter sources affect exposure.
  - Used interpolation for predicted PM air pollution surface.
  - Modified analysis using Find Nearest and Interpolate Points tools, showing population variation in results.

  **Present results**
  - Maps show predicted values for each populated place using nearest monitoring site and interpolated values across the state.

  **Make decisions**
  - Analysis allows comparison with past findings and increases confidence in current interpretation.
  - Grant-funding agency can assess whether cardiopulmonary rehabilitation programs across California are underused based on analysis results.
