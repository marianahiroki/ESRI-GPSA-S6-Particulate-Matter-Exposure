# ESRI-GPSA-S6-Particulate-Matter-Exposure
This exercise demonstrates the spatial analysis method in ArcGIS to interpolate sample points, generating a continuous surface to predict long-term particulate matter exposure. Its aim is to showcase how GIS can be utilized for interpolation tasks.

## Section 6 ##
**Exercise 1: Making Predictions: Particulate Matter Exposure**
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
  - Begin with a spatial analysis approach by asking:
    - Where are people more exposed to air pollution in California?
    - What data is required for analysis, and how can GIS represent, analyze, and assess it?
  - Identify areas exceeding state regulation values for particulate matter.
  - Determine locations with high particulate matter levels and significant populations aged 65 and above.

1. Exercise Steps
   
   **Data Exploration and Preparation:**
   - Map displays 98 PM2.5 monitoring sites, often in residential areas, with attributes such as location and exposure readings.
   - Populated Places layer shows areas with 200+ residents aged 65 and older, detailing population demographics.
   - Choropleth map design uses grayscale to emphasize PM2.5 values and graduated colours for population density.
     <img width="934" alt="Screenshot 2024-02-28 195545" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/72092cf2-ca7e-4483-bf33-385c5e166b08">

   - Long-term PM2.5 exposure increases age-specific mortality risk, aiding in establishing cardiopulmonary rehabilitation centres.

  **Data Analysis and Modeling:**
   - By selecting PM2.5 monitoring sites in areas with 200+ residents aged 65 years and older the map updates to display monitoring sites in these areas, symbolized with blue circles.
     <img width="935" alt="Screenshot 2024-02-28 195623" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/b47481c0-dd02-493c-8467-d94817da35d3">
     
   - Analysis reveals 81 monitoring sites in populated areas meeting age criteria Meaning that approximately 83% of total monitoring sites are in areas with 200+ elderly residents, ensuring good statewide coverage.
     
   ***Finding the Closest Feature***
   - It is possible to utilize the Find Closest analysis tool to identify the nearest monitoring site to each populated place within a 120-mile range.
   - Analysis results in connecting lines from Populated Places features to the nearest monitoring sites.
   - Nearest Monitoring Sites To Populated Places - Nearest Features layer covers the Annual PM2.5 Monitoring Sites layer, facilitating identification of closest sites.#
     <img width="935" alt="Screenshot 2024-02-28 201158" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/65c276b2-b243-4b62-a559-7263559595ed">
     
  ***Changing the Map Style***
  - Analyzing proximity: Determining air pollution levels at populated places within 120 miles of monitoring sites to assess the relationship between distance and pollution.
  - Visual representation: Modifying line feature styles to reflect particulate matter values, with widths indicating pollution levels.
    <img width="936" alt="Screenshot 2024-02-28 214203" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/d7bef0e1-064e-49fc-a4e5-8c04f5cee1bc">

  ***Filtering***
  - Identifying populated areas where annual PM2.5 values exceed California's ambient air quality standard of 12 micrograms per cubic meter, enabling estimation of the population living in areas with excessive pollution levels.
    <img width="935" alt="Screenshot 2024-02-28 214709" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/e14878b6-9179-4662-92c8-e5c38f67c531">

  ***Calculating Statistics***
  - Calculating statistics to determine the total population potentially exposed to air pollution exceeding state standards in 208 populated places within 120 miles of monitoring sites, revealing 11,423,778 individuals residing in areas with elevated PM2.5 particulate matter levels.
    ![image](https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/a7dd658c-e1f5-463f-8fe4-493e33f13604)

  ***Interpolating Values***
  - Utilizing geostatistical interpolation: Employing the Interpolate Points tool to predict PM2.5 values across California based on monitoring site data, considering factors like wind-blown particulates and proximity to heavily trafficked areas, and interpreting the resulting prediction surface to understand exposure risks.
    <img width="937" alt="Screenshot 2024-02-28 215623" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/8b876cae-7c42-438a-9a49-5a1a11fb872d">

  - Examining the interpolated PM prediction surface to visualize the distribution of PM2.5 levels across the state, with darker shades indicating higher predicted exposure values, and correlating predicted values with actual monitoring site data to validate the interpolation model's accuracy.
    <img width="936" alt="Screenshot 2024-02-28 222109" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/89015f9e-ea46-4864-b2c3-207972d1f9ec">

  ***Viewing Prediction Errors***
  - Analyzing prediction errors to understand the uncertainty associated with PM2.5 value predictions across California, with lighter-coloured areas indicating higher accuracy and red areas indicating greater uncertainty, enabling better interpretation of prediction maps and identification of areas with sparse monitoring data.
    ![image](https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/fae3db5b-0e7f-4b97-9e33-5eb33b9483c6)

 ***Identifying areas of concern***
  - Employing location analysis to pinpoint regions with predicted PM2.5 values surpassing California's state standards of 12 micrograms, facilitating the identification and examination of populated areas potentially exposed to elevated levels of particulate matter pollution.
    <img width="345" alt="Screenshot 2024-02-28 225726" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/29b095f6-9de6-4a53-89fb-d40b50f8661f">
    
    ![image](https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/81229037-0de5-48f3-8cff-e8b77e1ae784)

  - According to your initial analysis, the population living in areas with exposure levels greater than California standards is 11,423,778. The total population in the prediction results layer called Places Over CA Standards (14,289,472) varies from your initial analysis, which is expected. You used two different methods of analysis so you would expect there to be a difference in the results.

  ***Changing the Map Style***
  - The results show the places that are over the state exposure standards, as well as the predicted PM2.5 values across the state.
    <img width="935" alt="Screenshot 2024-02-28 231310" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/4e2ddb46-2802-4327-81a2-087f25673d3b">

  ***Creating a Custom Pop-up**
  - By using Custom Attribute Expressions on Fields List, it is possible to provide additional information to the map features such as the number of population in different ranges of age.
     <img width="937" alt="Screenshot 2024-02-28 233050" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/68e05d90-c418-4662-92dd-0a9487ab810d">

  ***Configuring a Pie Chart***
  - To promote further engagement, I added a pie chart to highlight the population in each populated place, incorporating the expressions you created in the previous step.
    <img width="937" alt="Screenshot 2024-02-28 233545" src="https://github.com/marianahiroki/ESRI-GPSA-S6-Particulate-Matter-Exposure/assets/110165879/7de48805-442b-49f8-9a46-a35fc224b85f">
  
  **Interpret results**
  - Map displays populated areas with predicted PM2.5 exposure exceeding California standards (12 μg/m³).
  - 247 locations exceed state standards, with exposure levels greater than 12 μg/m³.
  - Configured pop-ups showing total population and population aged 65 and older for areas exceeding standards.

  **Repeat or modify**
  - Other factors like proximity to heavily travelled roads and nearby particulate matter sources affect exposure.
  - Used interpolation for predicted PM air pollution surface.
  - Modified analysis using Find Nearest and Interpolate Points tools, showing population variation in results.

  **Present results**
  - Maps show predicted values for each populated place using the nearest monitoring site and interpolated values across the state.

  **Make decisions**
  - Analysis allows comparison with past findings and increases confidence in current interpretation.
  - Grant-funding agencies can assess whether cardiopulmonary rehabilitation programs across California are underused based on analysis results.
