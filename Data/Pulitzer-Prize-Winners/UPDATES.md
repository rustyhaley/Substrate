# Dataset Update Log

This file tracks all updates to the Pulitzer Prize Winners dataset.

## Update Format

Each entry should include:
- **Date**: When the update was made
- **Data Period**: Which time period the new data covers
- **Source**: URL or reference to the data source
- **Changes**: What was added, modified, or corrected
- **Records**: Number of records in dataset

---

## 2025-10-07 - Initial Arts & Letters Dataset Creation

**Data Period**: 1918 to 2024
**Source**: Wikidata SPARQL Query
**URL**: https://query.wikidata.org/
**Scope**: Arts & Letters Categories (Poetry, Drama, General/Special awards)

### Changes
- Created curated dataset with 249 unique Pulitzer Prize winners in Arts & Letters categories
- Fetched data via SPARQL query against Wikidata knowledge base
- Focused on categories with high Wikidata coverage for data quality
- Processed data:
  - Converted date formats to YYYY
  - Simplified category names (removed "Pulitzer Prize for" prefix)
  - Deduplicated entries
  - Removed work titles appearing as winner names
  - Added data_source column
  - Sorted by year (descending) and category
- Created category-specific CSV files:
  - category-poetry.csv (105 winners)
  - category-drama.csv (109 winners)
  - category-general.csv (35 winners)

### Records
- **Total Winners**: 249 unique records
- **Year Range**: 1918-2024 (107 years)
- **Categories**: Poetry (105), Drama (109), General/Special (35)
- **Completeness**: High for included categories (~95%+ coverage of Poetry and Drama)

### Data Quality Notes
- High-quality, curated dataset focusing on Arts & Letters categories
- Poetry and Drama have excellent coverage across all years (1918-2024)
- Journalism categories intentionally excluded (low Wikidata coverage)
- Fiction, History, Biography, Music excluded (incomplete Wikidata coverage)
- Some entries lack work titles (when not available in Wikidata)
- Winners are primarily individuals (authors, playwrights, poets)

### Files Created
- `Pulitzer-Prize-Winners-Arts-Letters-1918-2024.csv` (combined dataset - all categories)
- `category-poetry.csv` (Poetry winners only)
- `category-drama.csv` (Drama winners only)
- `category-general.csv` (General/Special awards only)
- `README.md` (dataset documentation with research methodology)
- `RESOURCES.md` (data sources)
- `UPDATES.md` (this file)

### SPARQL Query Used
```sparql
SELECT ?winner ?winnerLabel ?awardDate ?category ?categoryLabel ?work ?workLabel
WHERE {
  ?winner p:P166 ?awardStatement .
  ?awardStatement ps:P166 ?category .
  ?category (wdt:P279|wdt:P31)* wd:Q46525 .
  OPTIONAL { ?awardStatement pq:P585 ?awardDate . }
  OPTIONAL { ?awardStatement pq:P1686 ?work . }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en" }
}
ORDER BY DESC(?awardDate)
```

### Known Limitations
- Not comprehensive (Wikidata does not have all Pulitzer winners)
- Category names simplified for consistency
- Work titles missing for some entries
- Does not distinguish between individual/team/organizational winners
- No finalist data included

### Future Expansion Opportunities
- Add Fiction, History, Biography categories (requires enhanced scraping)
- Add Music category (completes Arts & Letters collection)
- Add Journalism categories (requires pulitzer.org scraping, ~1,400+ winners)
- Add finalist information (available from 1980 onwards)
- Combine with demographic data for representation analysis

---

## Future Updates

New updates will be added above this line in reverse chronological order (newest first).
