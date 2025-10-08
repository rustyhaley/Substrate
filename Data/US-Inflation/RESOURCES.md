# U.S. Inflation Data Resources

## Primary Data Source

**FRED Series CPIAUCSL**: https://fred.stlouisfed.org/series/CPIAUCSL
- CPI for All Urban Consumers: All Items in U.S. City Average
- Seasonally Adjusted
- Monthly updates (mid-month release)
- Direct CSV download available

**Direct CSV Download**: https://fred.stlouisfed.org/graph/fredgraph.csv?id=CPIAUCSL&cosd=1947-01-01
- No authentication required
- Clean CSV format
- Historical data from 1947 to present

## Official Government Sources

**Bureau of Labor Statistics (BLS)**: https://www.bls.gov/cpi/
- Official source of CPI data
- Comprehensive documentation and methodology
- Interactive data tools

**BLS CPI Data Page**: https://data.bls.gov/timeseries/CPIAUCSL
- Official BLS data viewer
- Multiple download formats
- Historical archives

**BLS API**: https://www.bls.gov/developers/
- Free tier: 500 queries/day
- JSON format
- Multiple series access

## Interactive Dashboards

**BLS CPI Dashboard**: https://www.bls.gov/charts/consumer-price-index/consumer-price-index-overview.htm
- Visual charts and graphs
- Latest release information
- Interactive exploration

**FRED CPIAUCSL Graph**: https://fred.stlouisfed.org/graph/?g=1qGKs
- Customizable time series charts
- Add comparison series
- Export graphs and data

## Related CPI Series

**Core CPI (Excluding Food & Energy)**: https://fred.stlouisfed.org/series/CPILFESL
- Better indicator of underlying inflation trends
- Used by Federal Reserve for policy decisions

**CPI Not Seasonally Adjusted**: https://fred.stlouisfed.org/series/CPIAUCNS
- Raw data without seasonal adjustment

**CPI Components**:
- Food: https://fred.stlouisfed.org/series/CPIFABSL
- Energy: https://fred.stlouisfed.org/series/CPIENGSL
- Housing: https://fred.stlouisfed.org/series/CPIHOSSL
- Medical Care: https://fred.stlouisfed.org/series/CPIMEDSL

## Documentation & Methodology

**BLS Handbook of Methods**: https://www.bls.gov/opub/hom/cpi/
- Complete methodology documentation
- Data collection procedures
- Calculation formulas

**BLS CPI FAQ**: https://www.bls.gov/cpi/questions-and-answers.htm
- Common questions answered
- Interpretation guidance

**Federal Reserve Inflation Info**: https://www.federalreserve.gov/faqs/economy_14400.htm
- Fed's 2% inflation target explanation
- PCE vs CPI comparison

## Alternative Inflation Measures

**PCE Price Index**: https://fred.stlouisfed.org/series/PCEPI
- Federal Reserve's preferred inflation measure
- Personal Consumption Expenditures price index

**Producer Price Index (PPI)**: https://www.bls.gov/ppi/
- Wholesale/producer price inflation
- Leading indicator for CPI

**Employment Cost Index**: https://www.bls.gov/ncs/ect/
- Labor cost inflation
- Wages and benefits

## API Access

**FRED API Documentation**: https://fred.stlouisfed.org/docs/api/fred/
- Free API key registration
- Comprehensive time series access
- JSON and XML formats

**Example API Call**:
```
https://api.stlouisfed.org/fred/series/observations?series_id=CPIAUCSL&api_key=YOUR_KEY&file_type=json
```

## Research & Analysis Tools

**Inflation Calculator**: https://www.bls.gov/data/inflation_calculator.htm
- Convert dollars across time periods
- Based on CPI-U data

**FRED Economic Research**: https://research.stlouisfed.org/
- Academic papers using FRED data
- Economic analysis and commentary

---

**Last Updated**: 2025-10-07
