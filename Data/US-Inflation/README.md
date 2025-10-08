# U.S. Inflation Dataset - Consumer Price Index (CPI)

## Overview

This directory contains authoritative U.S. inflation data from the Federal Reserve Economic Data (FRED) system, sourced from the Bureau of Labor Statistics (BLS). The Consumer Price Index for All Urban Consumers (CPI-U) is the gold standard measure of inflation in the United States, tracking price changes for a market basket of consumer goods and services.

## What's Inside

- **CPI-US-Monthly-1947-2025.csv** - Main dataset (945 monthly data points)
- **US-Inflation-CPI-1947-2025.md** - Detailed metadata and research documentation
- **README.md** - This file
- **UPDATES.md** - Change log for data updates
- **RESOURCES.md** - Data sources and access information

## Data Source Research

### How This Source Was Identified

I conducted comprehensive research to identify the most authoritative and accessible source for U.S. inflation data:

1. **Research Process**:
   - Evaluated Bureau of Labor Statistics (BLS) official data
   - Compared FRED (Federal Reserve Economic Data) accessibility
   - Tested DataHub.io and other aggregators
   - Verified data authenticity, update frequency, and download accessibility

2. **Primary Source Selected**: **FRED (Federal Reserve Economic Data)**
   - **URL**: https://fred.stlouisfed.org/series/CPIAUCSL
   - **Direct CSV**: https://fred.stlouisfed.org/graph/fredgraph.csv?id=CPIAUCSL&cosd=1947-01-01
   - **Series**: CPIAUCSL (CPI for All Urban Consumers, Seasonally Adjusted)

3. **Why FRED vs. BLS Direct**:
   - **FRED**: Easy CSV downloads, no API complexity, well-maintained
   - **BLS**: Official source but bot-protection makes automated downloads difficult
   - **Data Authenticity**: FRED sources directly from BLS - same authoritative data

## Why This Source Is Reputable

### Authority & Credibility

1. **Ultimate Authority**
   - Data originated by U.S. Bureau of Labor Statistics (BLS)
   - BLS is the principal federal agency for measuring labor market activity, working conditions, and price changes
   - CPI-U is the official inflation measure used by Federal Reserve for monetary policy

2. **FRED as Trusted Aggregator**
   - Maintained by Federal Reserve Bank of St. Louis
   - Official Federal Reserve System resource
   - Used by economists, policymakers, and researchers worldwide
   - Direct pipeline from BLS - no data manipulation

3. **Scientific Rigor**
   - Based on ~80,000 price quotes collected monthly
   - Covers 93% of U.S. population (all urban consumers)
   - Uses Laspeyres price index methodology
   - Basket weights updated every 2 years from Consumer Expenditure Survey
   - Peer-reviewed methodology documented in BLS Handbook of Methods

4. **Transparency**
   - Public domain data (U.S. government)
   - Complete methodology documentation available
   - Monthly updates follow strict release schedule
   - Historical revisions are minimal and documented

5. **Reliability Indicators**
   - **Temporal Consistency**: Continuous monthly data since 1947 (78 years)
   - **Update Discipline**: Released mid-month every month at 8:30 AM ET
   - **Cross-Validation**: Widely cited and validated across economic research
   - **Policy Usage**: Used by Federal Reserve, Treasury, Social Security Administration

## Dataset Specifications

### Coverage
- **Geographic**: United States (75 urban areas)
- **Population**: All Urban Consumers (~93% of U.S. population)
- **Temporal**: January 1947 - August 2025 (ongoing)
- **Frequency**: Monthly updates

### Metrics
- **Primary Measurement**: Consumer Price Index (1982-1984 = 100 baseline)
- **Format**: Index values (not percentage rates)
- **Adjustment**: Seasonally adjusted
- **Precision**: 3 decimal places

### Data Quality
- **Completeness**: 945/945 months (100% coverage since 1947)
- **Reliability**: Highest (official government economic statistic)
- **Timeliness**: Released ~2 weeks after month end
- **Accessibility**: Direct CSV download, no authentication required

## Current Status (as of 2025-10-07)

- **Latest Reading**: 323.364 (August 2025)
- **Year-over-Year Inflation**: ~2.5% (based on 12-month change)
- **Trend**: Moderating from 2022-2023 peaks, stabilizing near Fed target
- **Historical Context**:
  - 1947 baseline: 21.480
  - 2025 current: 323.364
  - Total increase: 1,404% over 78 years

## Key Inflation Periods in Dataset

### Major Episodes
- **1970s-1980s Stagflation**: Peak 14.8% annual inflation (1980)
- **Great Moderation** (1990s-2000s): Stable 2-3% inflation
- **Great Recession** (2008-2009): Brief deflation
- **COVID-19 Response** (2021-2023): Rapid surge to 9.1% (June 2022)
- **Current Normalization** (2024-2025): Returning to ~2% Federal Reserve target

## Use Cases

This dataset supports:

- **Economic Research**: Historical inflation analysis, forecasting, and modeling
- **Policy Analysis**: Federal Reserve monetary policy evaluation
- **Financial Planning**: Real return calculations, retirement planning, investment analysis
- **Academic Studies**: Macroeconomic research and teaching
- **Real Value Adjustments**: Converting nominal dollars to inflation-adjusted values
- **Substrate Integration**: Supporting Claims, Arguments, Economic Models with authoritative data

## Data Interpretation Notes

1. **Index vs. Rate**:
   - CPI value is an index number (current: ~323)
   - Inflation rate = percentage change in CPI over time
   - Year-over-year inflation = ((CPI_now - CPI_12mo_ago) / CPI_12mo_ago) × 100

2. **Purchasing Power**:
   - $100 in 1984 (base period) ≈ $323 in 2025
   - Inverse relationship: Higher CPI = lower dollar purchasing power

3. **Compounding**:
   - Small annual inflation rates compound significantly over decades
   - Example: 3% annual inflation reduces purchasing power by ~50% in 24 years

4. **Real vs. Nominal Values**:
   - Use CPI to convert nominal (current) dollars to real (constant) dollars
   - Formula: Real_value = Nominal_value × (CPI_base / CPI_current)

## Maintenance

See **UPDATES.md** for detailed change log of data refreshes and updates.

Monthly update recommended: Check mid-month for latest CPI release from FRED.

---

**Last Updated**: 2025-10-07
**Maintained By**: Substrate Data Curation
**Update Frequency**: Monthly (download fresh data mid-month following BLS release)
