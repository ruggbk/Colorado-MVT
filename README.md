# Colorado Motor Vehicle Theft Analysis
Brandon Rugg | July 2023

This project analyzes the sharp increase in motor vehicle theft (MVT) rates in Colorado beginning around 2014. It uses county-level crime and socioeconomic data to examine potential relationships with economic conditions, crime patterns, and policy changes. 

A Tableau Data Story summarizing key results is available here:
[Colorado Motor Vehicle Theft Analysis (Tableau Public)](https://public.tableau.com/app/profile/brandon.rugg/viz/ColoradoMotorVehicleTheft/ColoradosMotorVehicleTheftEpidemic)

## Data Sources
Data were integrated from multiple public sources:
- FBI Crime Data API (county-level crime statistics)
- US Census Bureau (population, income, poverty, labor statistics)
- Colorado Department of Revenue (marijuana sales data)
- Bureau of Labor Statistics (economic indicators)

## Data Processing
- County-level crime and economic datasets were merged into a unified panel (`main_df`)
- All crime measures were converted to per-capita rates
- Additional engineered features include:
  - Clearance rates
  - Average stolen vehicle value
  - A proxy “inequality” metric combining income and poverty measures

## Analysis
- Exploratory correlation analysis across crime and economic variables
- Linear regression models using standardized features
- Comparative analysis:
  - Full dataset (2000–2021, counties > 5,000 population)
  - Focused subset (top 20 MVT counties, 2008–2021)
- State-level comparisons with other recreational marijuana legalization states

## Key Findings
- MVT rates are strongly correlated with other property crimes (robbery, burglary, larceny), though this is likely a function of population density.
- Recreational marijuana sales consistently show a positive association with MVT rates across multiple model specifications.
- Traditional economic indicators (unemployment, poverty rate) show weak or inconsistent relationships with MVT. For the latter, this is likely due to limitations in how poverty rates are defined.
- Evidence does not support the hypothesis that changes in 2014 sentencing legislation were a primary driver of the increase (no corresponding structural break in clearance rates or stolen vehicle value trends).
- Results differ meaningfully between statewide and high-MVT county analyses, particularly in the Denver metro area.

## Interpretation
The results suggest that the 2014 MVT spike is associated with broader structural changes concentrated in urban counties rather than purely economic distress. Marijuana legalization and related economic shifts coincide with the timing and geographic concentration of the increase, though causality is not established.

## Repository Structure
- `Colorado MVT Analysis.ipynb` — main analysis and visualization
- `FBI Crime Data API.ipynb` — crime data ingestion pipeline
- `US Census Bureau API & General Economic Info.ipynb` — socioeconomic data ingestion
- `state rates/` — comparison data for states that also legalized marijuana early
- Cached datasets (`.pkl`, `.csv`) used for reproducibility