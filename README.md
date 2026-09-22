# Pennsylvania Severe Weather Atlas

A reproducible analysis of NOAA Storm Events records across Pennsylvania from 2011 through 2025, with a focused local view of the Lehigh Valley.

This project examines reported Thunderstorm Wind, Hail, and Tornado events through data preparation, quality checks, temporal analysis, county mapping, event magnitudes, reported impacts, and damage estimates.

## Study Snapshot

Pennsylvania:
- 15,399 reported event records
- 12,630 Thunderstorm Wind records
- 2,441 Hail records
- 328 Tornado records
- 67 counties represented

Lehigh Valley:
- 564 reported event records
- 464 Thunderstorm Wind records
- 93 Hail records
- 7 Tornado records
- Lehigh and Northampton counties

## Main Findings

- July had the most pooled event records statewide and in the Lehigh Valley.
- Summer accounted for 60.67% of Pennsylvania records and 69.33% of Lehigh Valley records.
- Pennsylvania’s highest annual total was 1,571 records in 2019.
- The Lehigh Valley’s highest annual total was 98 records in 2020.
- Allegheny County had the most statewide records, with 1,063.
- Lehigh County had more local records than Northampton County, with 313 compared with 251.
- EF0 and EF1 tornadoes represented 87.50% of Pennsylvania tornado records.
- Most wind records were classified as estimated gusts.

## Reported Impacts

Pennsylvania records contained:

- 205 direct injuries
- 10 indirect injuries
- 18 direct fatalities
- 5 indirect fatalities

Available damage estimates totaled:

- $203,508,160 in property damage
- $2,156,000 in crop damage

Lehigh Valley records contained:

- 2 direct injuries
- 0 reported fatalities
- $1,691,000 in available property damage estimates
- No positive crop-damage estimates

Missing damage estimates remain unknown and were not converted to zero.

## Project Structure

- data/processed — Prepared datasets and audit outputs
- notebooks — Six analysis notebooks
- reports/figures — Charts and visual summaries
- reports/tables — Summary tables and data manifests
- outputs/maps — County maps and geographic exports

## Selected Outputs

- Pennsylvania annual patterns
- Pennsylvania monthly reporting heatmap
- Lehigh Valley annual patterns
- County total-records map
- County event-type maps
- Hail-size distributions
- Wind-magnitude distributions
- Tornado-rating comparison
- Reported injuries and fatalities
- Reported property and crop damage

## Reproducing the Project

The project was developed with Python 3.13.

Create the environment with:

py -3.13 -m venv .venv

Install the project packages with:

.\.venv\Scripts\python.exe -m pip install ipykernel pandas numpy matplotlib seaborn requests geopandas

Register the notebook kernel with:

.\.venv\Scripts\python.exe -m ipykernel install --user --name pa-weather-atlas --display-name "Python (PA Weather Atlas)"

Run the notebooks in numerical order:

1. Project setup and data inventory
2. Study scope and historical data preparation
3. Annual and seasonal patterns
4. County patterns and mapping
5. Event magnitudes and reported impacts
6. Atlas summary and final review

Notebook 2 downloads the selected NOAA Storm Events files. Notebook 4 downloads the Census county boundary reference file.

Raw downloads, external archives, and the virtual environment are excluded from this repository. Download manifests and processing notebooks document how those inputs were obtained and used.

## Data Sources

- NOAA Storm Events Database
- NOAA Storm Events bulk CSV files
- U.S. Census Cartographic Boundary Files

## Interpretation Limits

These are reported event records, not a complete count of independent storms. NOAA records may be revised over time.

The analysis describes reported historical records and should not be treated as a direct measure of hazard risk, causation, or future trends. Damage estimates are incomplete and are not inflation-adjusted. County maps use the 2025 Census boundary reference layer for the study period.

## License

The MIT License applies to original code and documentation in this repository. NOAA and U.S. Census data remain attributed to their respective providers.
