# COVID-19 Wastewater Surveillance - SF Bay Area

## Metadata

**Data Source**: California Department of Public Health (CDPH) / CDC NWSS
**Primary URL**: https://data.chhs.ca.gov/dataset/covid-19-wastewater-surveillance
**Direct CSV**: https://data.chhs.ca.gov/dataset/1184f641-313f-47ee-b126-9e8c42699be5/resource/726752d3-afe6-4733-99bd-ffb9f400348c/download/wastewater.csv
**CDC NWSS Dashboard**: https://www.cdc.gov/nwss/
**Update Frequency**: Weekly (typically updated Fridays)
**Last Updated**: 2025-10-07
**Coverage**: San Francisco Bay Area, July 2023 - Present
**License**: Public domain (U.S. government data)

## Geographic Coverage

**Bay Area Counties Monitored:**
- San Francisco
- Alameda (East Bay Municipal Utility District - EBMUD)
- Santa Clara
- Contra Costa
- Marin (6 sites including Central Marin Sanitation Agency, Novato)
- San Mateo

**Major Treatment Plants:**
- EBMUD (East Bay)
- Central Marin Sanitation Agency
- Novato Sanitary District
- Plus 12+ representative plants across the region

## Data Description

### Primary Metrics

**SARS-CoV-2 Concentration**: Viral gene copies measured via qPCR and ddPCR methods
- **Unit**: Log10 transformed concentration values (copies/mL)
- **Normalization**: Flow-adjusted, PMMoV-normalized options available
- **Seasonality**: Data organized by epidemic season (e.g., 2024/2025, 2023/2024)

### Data Format

The California statewide dataset provides:
- `season`: Epidemic season identifier
- `weekending`: Week ending date (MM/DD/YYYY format)
- `sars_conc`: Log10 SARS-CoV-2 concentration (copies/mL)

### Detection Methods
- **qPCR** (quantitative polymerase chain reaction)
- **ddPCR** (droplet digital PCR)
- Methods detect viral RNA fragments in wastewater

## Key Insights from Data

### Current Status (October 2025)
- **Latest Reading (08/02/2025)**: 5.60 log10 copies/mL
- **Trend**: Elevated levels, increasing from summer lows
- **Context**: HIGH wastewater activity across California

### Historical Peaks
- **Highest Peak**: 17.73 log10 copies/mL (Week ending 01/06/2024)
- **Summer 2024 Peak**: 15.25 log10 copies/mL (Week ending 08/03/2024)
- **Recent Low**: 1.60 log10 copies/mL (Week ending 03/15/2025)

### Wastewater as Leading Indicator
- Wastewater surveillance typically shows trends **4-7 days before** clinical testing
- Population-level surveillance (not individual detection)
- Captures symptomatic, asymptomatic, and unreported cases

## Data Sources & Alternative Access

### Primary Sources
1. **California CHHS Open Data Portal**: https://data.chhs.ca.gov/
2. **CDC NWSS Public Dataset**: https://data.cdc.gov/Public-Health-Surveillance/NWSS-Public-SARS-CoV-2-Wastewater-Metric-Data/2ew6-ywp6
3. **WastewaterSCAN** (Historical): https://data.wastewaterscan.org/ (Note: Scaled back Bay Area sampling mid-2024)

### API Access
- **Socrata API**: Available via data.cdc.gov and data.chhs.ca.gov
- **Format**: JSON, CSV, XML
- **Query Language**: SoQL (Socrata Query Language)

## Usage Notes

### Data Quality
- **Sampling Frequency**: 1-3 times per week per site
- **Reporting**: Weekly aggregated data
- **Completeness**: Some gaps during equipment maintenance or sampling issues
- **Reliability**: High - multiple redundant sites across region

### Interpretation Guidelines
1. **Trend Over Absolute Value**: Focus on directional changes, not single readings
2. **Compare Within Dataset**: Log scale means multiplicative changes
3. **Seasonal Context**: Consider flu season and holiday patterns
4. **Population Normalized**: Data adjusted for wastewater flow and served population

## Related Substrate Components

**Claims Supported:**
- Wastewater surveillance as early warning system for disease outbreaks
- Population-level health monitoring effectiveness

**Problems Addressed:**
- Real-time disease surveillance challenges
- Underreporting in clinical testing systems

**Solutions Enabled:**
- Public health decision-making based on ground-truth data
- Trend analysis for resource allocation

## Data Processing Notes

The accompanying CSV file (`COVID-Wastewater-SF-Bay-Area-2023-2025.csv`) contains:
- California statewide aggregated data from CDPH
- Weekly readings from July 2023 through August 2025
- Log10 transformed viral concentration values
- ISO date format conversion for compatibility

## References

1. CDPH COVID-19 Wastewater Surveillance: https://www.cdph.ca.gov/Programs/CID/DCDC/Pages/COVID-19/CalSuWers-Dashboard.aspx
2. CDC NWSS: https://www.cdc.gov/nwss/
3. WastewaterSCAN: https://www.wastewaterscan.org/
4. Marin County Wastewater Monitoring: https://www.marinhhs.org/covid-19-wastewater

---

**Dataset Purpose**: Provide ground-truth, authoritative COVID-19 surveillance data for the San Francisco Bay Area to support public health analysis, trend monitoring, and informed decision-making.
