# Vapor Pressure Deficit Analysis
## VPD Analysis: Vapor Pressure Deficit and Environmental Health in Six U.S. Cities

## Overview
This project analyzes and forecasts Vapor Pressure Deficit (VPD) trends in six U.S. cities, exploring the link between environmental conditions and health. The study was initiated after observing the impact of humidity on fungal outbreaks and investigating VPD's potential role in student athlete suicides. Our analysis aims to understand VPD fluctuations and their implications on environmental health.

## Introduction 

VPD, a measure of air moisture deficit, is critical in understanding environmental health impacts. We started studying VPD in 2018, driven by a Candida auris outbreak in a New Jersey nursing home, and explored its role in influencing health outcomes.

Key Findings:

VPD varies significantly between months, e.g., in 2019, the VPD in October was lower than in September (Average 1.441 vs. 1.1212, t=5.09, p < .001).
VPD may encourage the growth of fungi and mold, potentially influencing human health.
This study also examines tragic incidents involving student athlete suicides, potentially linked to environmental stressors:

Katie Meyer (Stanford University, March 11, 2022)
Robert Martin (SUNY Binghampton, April 1, 2022)
Jayden Hill (Northern Michigan University, April 3, 2022)
Sarah Shulze (University of Wisconsin, April 13, 2022)
Kelly Catlin (Stanford University, March 7, 2019)
Lauren Bernett (James Madison University, April 26, 2022)
These cases motivated us to investigate VPD patterns in the cities where these events occurred.

##What is VPD?
Vapor Pressure Deficit (VPD) is the difference between the amount of moisture in the air and its saturation point. It helps determine if the environment is too dry or too moist.

##Key Highlights:

Factors: Temperature (directly proportional) and Relative Humidity (inversely proportional).
Formula: (6.1078 * exp((Temp / (234.175 + Temp) * 17.08085)) * (1 - Humidity/100)) / 10
Ideal Range: 0.8 - 1.2 kPa; values below 0.8 indicate high moisture, while values above 1.2 indicate dryness.

##Cities Analyzed
Palo Alto, CA
Johnson City, NY
Marquette, MI
Madison, WI
Weyers Cave, VA
Philadelphia, PA
Data and Methods
Dataset: VPD Actual Dataset

##Analysis Workflow:

Data Extraction: Read data from Excel files, extracting relevant features for VPD calculations.
VPD Calculation: VPD was added as an additional feature using the standard formula.
Data Description: Summary statistics, including mean, median, and standard deviation for VPD scores.
Data Visualization: Line plots, box plots, and heatmaps to display trends and correlations.
Data Analytics: Linear regression models were employed to predict VPD using temperature and humidity.

##Linear Regression Model
Independent Variables: Temperature and Humidity.
Dependent Variable: VPD.
Formula: VPD = m1 * Temperature + m2 * Humidity + c

##Model Verification 

Example:

Given: Temperature = 75, Humidity = 60
Coefficients: m1 = 0.0289, m2 = -0.0169
Calculated VPD: 1.154

##Results
A significant increase in VPD over time in Palo Alto and Philadelphia suggests rising temperatures and decreasing humidity, highlighting the impact of global warming in these cities.
No significant VPD changes were observed in the other cities analyzed.
Learnings and Reflections
This project highlighted the importance of VPD as a factor in environmental health and forecasting climate change trends.
Key takeaways include the need for comprehensive research beyond weather forecasting to examine other factors influencing suicides among athletes.
Despite time constraints, this project demonstrated the relationship between VPD and health outcomes, emphasizing the need for further study.

##Conclusion
While successful in showing VPD trends, the project remains incomplete in correlating other critical factors that influence athlete suicides. Future work would aim to include additional variables to build a more comprehensive model.














