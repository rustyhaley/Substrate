# Dataset Update Log

This file tracks all updates to the U.S. Inflation (CPI) dataset.

## Update Format

Each entry should include:
- **Date**: When the update was made
- **Data Period**: Which time period the new data covers
- **Source**: URL or reference to the data source
- **Changes**: What was added, modified, or corrected
- **Latest Value**: Most recent data point added

---

## 2025-10-07 - Initial Dataset Creation

**Data Period**: 1947-01-01 to 2025-08-01
**Source**: FRED (Federal Reserve Economic Data) - BLS Series CPIAUCSL
**URL**: https://fred.stlouisfed.org/graph/fredgraph.csv?id=CPIAUCSL&cosd=1947-01-01

### Changes
- Created initial dataset with 945 monthly data points
- Downloaded FRED series CPIAUCSL (CPI for All Urban Consumers, Seasonally Adjusted)
- Data includes:
  - Observation dates in ISO 8601 format (YYYY-MM-DD)
  - CPI index values with 3 decimal place precision
  - Coverage from January 1947 through August 2025

### Latest Value
- **Month**: August 2025
- **CPI Index**: 323.364
- **Year-over-Year Change**: ~2.5% (from August 2024)
- **Trend**: Moderating inflation, stabilizing near Federal Reserve 2% target

### Coverage
- **Start Date**: 1947-01-01 (earliest available in FRED series)
- **End Date**: 2025-08-01 (most recent data)
- **Total Records**: 945 monthly measurements
- **Completeness**: 100% (no gaps in monthly series)

### Files Created
- `CPI-US-Monthly-1947-2025.csv` (main dataset)
- `US-Inflation-CPI-1947-2025.md` (metadata documentation)
- `README.md` (dataset documentation)
- `RESOURCES.md` (data sources)
- `UPDATES.md` (this file)

### Data Quality Notes
- All 945 months have complete data
- No missing values or gaps in time series
- Seasonally adjusted values from BLS
- Index baseline: 1982-1984 = 100
- Historical low: 21.480 (January 1947)
- Current value: 323.364 (August 2025)
- Total increase: 1,404% over 78-year period

### Notable Context
- Dataset captures major inflation episodes:
  - 1970s-1980s stagflation (peak ~14.8% annual)
  - Great Moderation (1990s-2000s stable ~2-3%)
  - Great Recession (2008-2009)
  - COVID-19 inflation surge (2021-2023, peak 9.1%)
  - Current normalization period (2024-2025)

---

## Future Updates

New updates will be added above this line in reverse chronological order (newest first).

### Update Schedule

**Recommended Update Frequency**: Monthly

**When to Update**:
- BLS releases CPI data mid-month (typically 12th-15th)
- FRED updates same day as BLS release
- Check around the 15th of each month for new data

**How to Update**:
```bash
cd Data/US-Inflation
curl -s "https://fred.stlouisfed.org/graph/fredgraph.csv?id=CPIAUCSL&cosd=1947-01-01" -o CPI-US-Monthly-1947-2025.csv
```

**Update Checklist**:
1. Download fresh CSV from FRED
2. Verify row count increased by 1 (one new month)
3. Check latest value is reasonable (typically 0.1-0.5% monthly change)
4. Update this file with new entry
5. Update "Last Updated" date in README.md and metadata file
