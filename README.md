# Aviation Accident Risk Analysis (1962 -2023)
## Project Overview

This project analyzes six decades of civil aviation accidents using data from the National Transportation Safety Board (NTSB). As the company prepares to enter the aviation industry, this analysis identifies the lowest-risk aircraft models and the conditions associated with fatal outcomes. The insights will guide aircraft acquisition and safety strategies for the new aviation division.

## Business Understanding

 **Stakeholder:** Head of the Aviation Division
 **Objective:** Support strategic aircraft acquisition by identifying historically safer aircraft and high-risk flight conditions
 **Value:** Reduce operational risk, lower insurance liability, and improve safety outcomes in early operations

## Data Understanding

 **Source:** [NTSB Aviation Accident Database](https://www.ntsb.gov/_layouts/ntsb.aviation/AviationQuery.aspx)
 **Scope:** 80,000+ records from 1962 to 2023
 **Key Features:**  
  - Aircraft Make and Model  
  - Injury Severity (fatal, serious, minor, uninjured)  
  - Flight Phase  
  - Weather Conditions  
  - Purpose of Flight  
  - Engine Count  

### Limitations
- Some columns (e.g., `Aircraft.Category`) had over 60% missing values
- Many fields contained coded abbreviations that were decoded for clarity
- Narrative text fields were excluded due to unstructured format

## Data Preparation
- Removed irrelevant or sparse columns (e.g., location coordinates, registration numbers)
- Decoded categorical fields such as `Weather.Condition`, `Injury.Severity`, and `Purpose.of.flight`
- Standardized case for text fields (e.g., "BOEING" → "Boeing")
- Imputed injury counts with 0 and filled missing categorical fields with `"Unknown"` or `"No"`
- Created new `Event.Year` feature from date

All data cleaning and transformations are fully documented in the Jupyter Notebook.

## Key Findings

### 1. **Aircraft Make**
- Boeing and Cessna recorded the highest fatal injury totals
- May reflect higher flight volume — needs further context before acquisition

### 2. **Phase of Flight**
- Approach and landing had the highest fatality counts
- These phases are risk hotspots needing focused training and safety procedures

### 3. **Weather & Purpose**
- Flights in Instrument Meteorological Conditions (IMC) had significantly higher fatality rates
- Personal flights were riskier than commercial or instructional use cases

### 4. **Trend Over Time**
- Fatal injuries have declined since the 1990s, suggesting progress in aviation safety

##  Recommendations

1. Avoid acquiring aircraft models with historically high fatality rates unless justified by volume or modernization
2. Prioritize safety interventions during approach and landing
3. Avoid IMC operations unless fully certified
4. Focus early operations on commercial or instructional flights

##  Key Links

[Jupyter Notebook][aviation_accident_analysis- luciana.ipynb](https://github.com/Lndanu/aviation-accidents-analysis/blob/main/aviation_accident_analysis-%20luciana.ipynb)
[Business Slide Deck](./aviation_data_insights_presentation.pdf)
[NTSB Dataset Source](https://www.ntsb.gov/_layouts/ntsb.aviation/AviationQuery.aspx)
Interactive Dashboard: https://public.tableau.com/authoring/AviationAccidentRiskInsights19622023/AviationSafetyAnalysisDashboard#1
https://public.tableau.com/app/profile/luciana5648/viz/AviationAccidentRiskInsights19622023/AviationSafetyAnalysisDashboard


## Author

**Luciana Ndanu**  
Location: Nairobi, Kenya  
Email: lucianandabu9@gmail.com
LinkedIn:https://www.linkedin.com/in/luciana-ndanu-24a71bb6/]
