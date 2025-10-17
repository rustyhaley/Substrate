# U.S. GDP Data Resources

This document provides direct links to data sources, APIs, and tools for accessing U.S. GDP data.

## Primary Data Sources

### FRED (Federal Reserve Economic Data)

**Official Website:**
- Main Portal: https://fred.stlouisfed.org
- About FRED: https://fred.stlouisfed.org/about

**Real GDP Series Pages:**
- **GDPC1** (Quarterly Real GDP): https://fred.stlouisfed.org/series/GDPC1
- **GDPCA** (Annual Real GDP): https://fred.stlouisfed.org/series/GDPCA
- **GDP** (Quarterly Nominal GDP): https://fred.stlouisfed.org/series/GDP

**Direct CSV Downloads:**
```bash
# Quarterly Real GDP (GDPC1) - 1947 to present
curl -L "https://fred.stlouisfed.org/graph/fredgraph.csv?id=GDPC1" -o gdpc1.csv

# Annual Real GDP (GDPCA) - 1929 to present
curl -L "https://fred.stlouisfed.org/graph/fredgraph.csv?id=GDPCA" -o gdpca.csv

# Quarterly Nominal GDP (GDP) - 1947 to present
curl -L "https://fred.stlouisfed.org/graph/fredgraph.csv?id=GDP" -o gdp.csv
```

**FRED API:**
- API Documentation: https://fred.stlouisfed.org/docs/api/fred/
- API Key Signup: https://fredaccount.stlouisfed.org/apikeys
- Free tier available with rate limits
- RESTful API with JSON/XML responses

**FRED API Example:**
```bash
# Get Real GDP data via API (requires API key)
curl "https://api.stlouisfed.org/fred/series/observations?series_id=GDPC1&api_key=YOUR_API_KEY&file_type=json"
```

### Bureau of Economic Analysis (BEA)

**Official Website:**
- BEA Homepage: https://www.bea.gov
- GDP Data Portal: https://www.bea.gov/data/gdp/gross-domestic-product

**Interactive Data Tools:**
- Interactive NIPA Tables: https://apps.bea.gov/itable/
  - Navigate to: National → GDP & Personal Income → Section 1 (Domestic Product and Income)
  - Table 1.1.6: Real Gross Domestic Product, Chained Dollars
- iTable Interface: https://apps.bea.gov/itable/?ReqID=70&step=1

**BEA API:**
- API Home: https://apps.bea.gov/api/signup/
- API Documentation: https://apps.bea.gov/api/bea_web_service_api_user_guide.htm
- API Key Signup: https://apps.bea.gov/api/signup/ (free, instant email delivery)
- Supports JSON and XML output

**BEA API Example:**
```bash
# Get GDP data via BEA API (requires free API key)
curl "https://apps.bea.gov/api/data/?UserID=YOUR_API_KEY&method=GetData&datasetname=NIPA&TableName=T10106&Frequency=Q&Year=X&ResultFormat=json"
```

**Key NIPA Tables:**
- Table 1.1.6: Real GDP (Quarterly and Annual)
- Table 1.1.5: Nominal GDP (Quarterly and Annual)
- Table 1.1.9: Implicit Price Deflators for GDP

**News Releases:**
- GDP News Release: https://www.bea.gov/news/blog/2024-09-26/gross-domestic-product-second-quarter-2024-third-estimate
- Release Schedule: https://www.bea.gov/news/schedule

## Extended Historical Data

### MeasuringWorth (1790-Present)

**Website:** https://www.measuringworth.com/datasets/usgdp/

**Coverage:** U.S. GDP from 1790 to present (links historical estimates to modern BEA data)

**Key Researchers:**
- Louis Johnston (College of Saint Benedict / Saint John's University)
- Samuel H. Williamson (University of Illinois at Chicago - emeritus)

**Methodology:**
- Pre-1929 data based on economic historians' research:
  - Weiss (1799-1829)
  - Gallman (1839-1909 benchmarks)
  - Kendrick (1909-1928)
- Post-1929: Official BEA data

**Download:** Available as CSV from MeasuringWorth website

## Related Federal Reserve Resources

### GDPNow (Real-Time GDP Forecasting)

**Atlanta Fed GDPNow Model:**
- Website: https://www.atlantafed.org/cqer/research/gdpnow
- Purpose: Nowcasting model for current quarter GDP estimates
- Updates: Multiple times weekly as new economic data releases
- Useful for: Tracking economic activity between official BEA releases

## Alternative Data Aggregators

### International Sources

**World Bank:**
- Website: https://data.worldbank.org/indicator/NY.GDP.MKTP.CD?locations=US
- API: https://datahelpdesk.worldbank.org/knowledgebase/articles/889392-about-the-indicators-api-documentation
- Note: Sources U.S. GDP from BEA; use BEA/FRED directly for most accurate data

**IMF (International Monetary Fund):**
- Website: https://www.imf.org/en/Data
- Note: Not recommended as primary GDP source; better for financial variables

**OECD:**
- Website: https://data.oecd.org/gdp/gross-domestic-product-gdp.htm
- Note: Sources from BEA; use BEA/FRED directly for most accurate data

## Data Download Methods Comparison

| Source | Format | Authentication | Historical Coverage | Update Frequency | Best For |
|--------|--------|----------------|---------------------|------------------|----------|
| FRED CSV | CSV | None | 1947 (Q), 1929 (A) | Quarterly | Quick downloads, scripting |
| FRED API | JSON/XML | API Key (free) | 1947 (Q), 1929 (A) | Quarterly | Automated data pipelines |
| BEA iTable | CSV/Excel | None | 1929+ | Quarterly | Interactive exploration |
| BEA API | JSON/XML | API Key (free) | 1929+ | Quarterly | Detailed NIPA table access |
| MeasuringWorth | CSV | None | 1790+ | Annual updates | Long-term historical analysis |

## Update Schedule

### BEA Release Schedule (Three-Stage Process)

Each quarter of GDP data goes through three releases:

1. **Advance Estimate**: ~30 days after quarter end (8:30 AM ET)
2. **Second Estimate**: ~60 days after quarter end (8:30 AM ET)
3. **Third Estimate**: ~90 days after quarter end (8:30 AM ET)

**Annual Comprehensive Update:**
- Released each September
- Revises 5+ years of historical data
- Incorporates methodological improvements

**Example Schedule for Q3 2025:**
- Advance: October 30, 2025
- Second: November 26, 2025
- Third: December 23, 2025

**2025 Release Calendar:**
- Q4 2024 Third: January 30, 2025 ✅
- Q1 2025 Third: June 26, 2025 ✅
- Q2 2025 Third: September 25, 2025 ✅
- Annual Update: September 25, 2025 ✅
- Q3 2025 Advance: October 30, 2025 (upcoming)

## How to Update This Dataset

### Manual Update via FRED

```bash
# Download latest quarterly data
curl -L "https://fred.stlouisfed.org/graph/fredgraph.csv?id=GDPC1" -o Real-GDP-Quarterly-1947-2025.csv

# Download latest annual data
curl -L "https://fred.stlouisfed.org/graph/fredgraph.csv?id=GDPCA" -o Real-GDP-Annual-1929-2024.csv

# Verify download
head -5 Real-GDP-Quarterly-1947-2025.csv
tail -5 Real-GDP-Quarterly-1947-2025.csv
```

### Automated Update Script

```bash
#!/bin/bash
# update-gdp-data.sh

DATA_DIR="./Data/US-GDP"
FRED_BASE="https://fred.stlouisfed.org/graph/fredgraph.csv"

# Download quarterly real GDP
curl -L "${FRED_BASE}?id=GDPC1" -o "${DATA_DIR}/Real-GDP-Quarterly-1947-2025.csv"

# Download annual real GDP
curl -L "${FRED_BASE}?id=GDPCA" -o "${DATA_DIR}/Real-GDP-Annual-1929-2024.csv"

echo "GDP data updated: $(date)"
```

### Best Practices for Updates

1. **Update after BEA's third estimate** (most complete data for the quarter)
2. **Update after September annual revision** (historical data corrections)
3. **Verify data integrity** after download (check first/last rows, row count)
4. **Document updates** in UPDATES.md with date and data range
5. **Note any methodology changes** from BEA annual updates

## Data Verification

### Quick Verification Checklist

```bash
# Check quarterly data
wc -l Real-GDP-Quarterly-1947-2025.csv  # Should be ~315 lines (header + 314 quarters)
head -3 Real-GDP-Quarterly-1947-2025.csv  # Should start with 1947-01-01
tail -3 Real-GDP-Quarterly-1947-2025.csv  # Should end with latest quarter

# Check annual data
wc -l Real-GDP-Annual-1929-2024.csv  # Should be ~97 lines (header + 96 years)
head -3 Real-GDP-Annual-1929-2024.csv  # Should start with 1929-01-01
tail -3 Real-GDP-Annual-1929-2024.csv  # Should end with 2024-01-01
```

### Cross-Validation

- Compare latest values with BEA news releases
- Verify against FRED website display
- Check that growth rates match reported economic news
- Confirm no missing data points in series

## Additional Research Resources

### Economic Analysis

- **NBER Business Cycle Dating**: https://www.nber.org/research/data/us-business-cycle-expansions-and-contractions
- **BEA Methodologies**: https://www.bea.gov/resources/methodologies
- **FRED Blog**: https://fredblog.stlouisfed.org/ (GDP analysis and interpretation)

### Academic Papers

- **BEA GDP Methodology**: https://www.bea.gov/resources/methodologies/nipa-handbook
- **Historical GDP Construction**: Johnston & Williamson papers on MeasuringWorth

### News & Analysis

- **BEA News Releases**: https://www.bea.gov/news/current-releases
- **Federal Reserve Economic Commentary**: District Fed banks publish GDP analysis
- **Economic Calendar**: https://www.bea.gov/news/schedule

## Support & Documentation

### FRED Support
- Email: stlsFRED@stls.frb.org
- FAQ: https://fred.stlouisfed.org/docs/api/fred/

### BEA Support
- Contact Form: https://www.bea.gov/contact
- Phone: (301) 278-9004
- Email: customerservice@bea.gov

---

**Last Updated**: 2025-10-16
**Next Recommended Check**: After Q3 2025 third estimate (late January 2026)
