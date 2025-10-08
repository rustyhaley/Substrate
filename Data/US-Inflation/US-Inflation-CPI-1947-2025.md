# U.S. Consumer Price Index (CPI) - Inflation Data

## Metadata

**Data Source**: Federal Reserve Economic Data (FRED) / U.S. Bureau of Labor Statistics (BLS)
**Primary URL**: https://fred.stlouisfed.org/series/CPIAUCSL
**Direct CSV**: https://fred.stlouisfed.org/graph/fredgraph.csv?id=CPIAUCSL&cosd=1947-01-01
**BLS Series**: CPIAUCSL (Consumer Price Index for All Urban Consumers: All Items in U.S. City Average)
**Update Frequency**: Monthly (released mid-month following data month at 8:30 AM ET)
**Last Updated**: 2025-10-07
**Coverage**: United States, January 1947 - Present
**License**: Public domain (U.S. government data)

## Data Description

### Primary Metrics

**Consumer Price Index (CPI-U)**: Measures changes in the price level of a weighted average market basket of consumer goods and services purchased by households
- **Unit**: Index value (1982-1984 = 100 baseline)
- **Population Coverage**: All Urban Consumers (approximately 93% of U.S. population)
- **Seasonally Adjusted**: Yes
- **Base Period**: 1982-1984 = 100

### Data Format

The FRED dataset provides:
- `observation_date`: Month identifier (YYYY-MM-DD format, first day of month)
- `CPIAUCSL`: CPI-U index value (seasonally adjusted)

### Calculation Methodology

- **Index Calculation**: Laspeyres price index formula
- **Basket Composition**: ~80,000 items across 8 major categories:
  - Food and beverages
  - Housing
  - Apparel
  - Transportation
  - Medical care
  - Recreation
  - Education and communication
  - Other goods and services
- **Weight Updates**: Basket weights updated every 2 years based on Consumer Expenditure Survey
- **Geographic Coverage**: 75 urban areas across the United States

## Key Insights from Data

### Current Status (August 2025)
- **Latest Reading**: 323.364 (August 2025)
- **Year-over-Year Inflation**: Approximately 2.5% (based on 12-month change)
- **Trend**: Moderating from 2022-2023 peaks, stabilizing near Federal Reserve target

### Historical Context
- **Post-WWII Low**: 21.480 (January 1947)
- **2022-2023 Peak**: 317.603 (December 2024)
- **Total Increase**: 1,404% from 1947 to 2025 (78-year period)
- **Average Annual Inflation**: ~3.5% over full period

### Major Inflation Episodes
- **1970s Stagflation**: Double-digit inflation (peak 14.8% in 1980)
- **Great Moderation** (1990s-2000s): Stable ~2-3% annual inflation
- **Great Recession** (2008-2009): Brief deflationary period
- **COVID-19 Response** (2021-2023): Rapid inflation surge to 9.1% (June 2022)
- **Current Period** (2024-2025): Gradual return to ~2% target

### Inflation Rate Calculation

To calculate year-over-year inflation rate:
```
Inflation Rate = ((CPI_current - CPI_12months_ago) / CPI_12months_ago) × 100
```

Example (August 2025):
- Current: 323.364
- One year ago (Aug 2024): ~315.5
- Inflation: ((323.364 - 315.5) / 315.5) × 100 ≈ 2.5%

## Data Sources & Alternative Access

### Primary Sources
1. **FRED (Federal Reserve Economic Data)**: https://fred.stlouisfed.org/series/CPIAUCSL
2. **BLS Official CPI Page**: https://www.bls.gov/cpi/
3. **BLS Data Tools**: https://data.bls.gov/timeseries/CPIAUCSL

### Related CPI Series
- **CPILFESL**: CPI for All Urban Consumers: All Items Less Food & Energy (Core CPI)
- **CPIAUCNS**: CPI-U Not Seasonally Adjusted
- **CPIENGSL**: CPI for Energy
- **CPIFABSL**: CPI for Food and Beverages

### API Access
- **FRED API**: https://fred.stlouisfed.org/docs/api/fred/
  - Requires free API key
  - JSON and XML formats
  - Comprehensive time series access
- **BLS Public Data API**: https://www.bls.gov/developers/
  - Free tier: 500 queries/day
  - JSON format
  - Multiple series access

## Usage Notes

### Data Quality
- **Reliability**: Gold standard for U.S. inflation measurement
- **Frequency**: Monthly updates (mid-month release)
- **Timeliness**: Published ~2 weeks after month end
- **Revisions**: Minimal - typically only seasonal adjustment factors revised
- **Completeness**: 945 monthly observations (1947-2025)

### Interpretation Guidelines
1. **Index vs. Rate**: CPI is an index; inflation rate is the percentage change
2. **Compounding Effects**: Small annual rates compound significantly over decades
3. **Purchasing Power**: CPI of 100 in 1984 requires ~323 today for equivalent purchasing power
4. **Real vs. Nominal**: Use CPI to adjust nominal dollars to real (inflation-adjusted) values
5. **Base Period**: 1982-1984 average = 100 baseline

### Limitations
- **Substitution Bias**: Fixed basket doesn't capture consumer substitution behavior
- **Quality Changes**: Difficult to adjust for product quality improvements
- **New Products**: Slow to incorporate new goods and services
- **Geographic Variation**: National average masks regional differences
- **Population Coverage**: Excludes rural households (~7% of population)

## Related Substrate Components

**Claims Supported:**
- CPI as authoritative measure of inflation and purchasing power
- Federal Reserve monetary policy effectiveness
- Impact of fiscal/monetary policy on price levels

**Problems Addressed:**
- Economic planning and policy-making requiring accurate inflation data
- Wage and benefit adjustments (COLAs)
- Real return calculations for investments

**Solutions Enabled:**
- Inflation-adjusted economic analysis
- Cost of living comparisons across time periods
- Monetary policy decision-making

## Data Processing Notes

The accompanying CSV file (`CPI-US-Monthly-1947-2025.csv`) contains:
- FRED series CPIAUCSL (CPI-U seasonally adjusted)
- Monthly observations from January 1947 through August 2025
- Index values with 3 decimal place precision
- ISO 8601 date format (YYYY-MM-DD)

## Use Cases

This dataset supports:
- **Economic Research**: Historical inflation analysis and forecasting
- **Policy Analysis**: Federal Reserve and Treasury decision-making evaluation
- **Financial Planning**: Real return calculations, retirement planning
- **Wage Negotiations**: COLA adjustments based on CPI changes
- **Academic Research**: Macroeconomic studies and modeling
- **Substrate Integration**: Supporting Claims, Arguments, and economic Models with authoritative data

## References

1. BLS CPI Overview: https://www.bls.gov/cpi/overview.htm
2. BLS CPI FAQ: https://www.bls.gov/cpi/questions-and-answers.htm
3. FRED CPIAUCSL Series: https://fred.stlouisfed.org/series/CPIAUCSL
4. BLS Handbook of Methods (Chapter 17 - CPI): https://www.bls.gov/opub/hom/cpi/
5. Federal Reserve Inflation Targeting: https://www.federalreserve.gov/faqs/economy_14400.htm

---

**Dataset Purpose**: Provide authoritative, comprehensive U.S. inflation data to support economic analysis, policy evaluation, and real-value calculations within the Substrate knowledge system.
