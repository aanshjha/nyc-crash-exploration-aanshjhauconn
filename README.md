# NYC Crash Data Exploration

This repository explores New York City motor-vehicle crash records from June 30 through July 6, 2024, including missing-data tests, hourly patterns, a location map, severity comparisons, and a validated ZIP-code merge.

## Repository layout

- `homework5.qmd` - source analysis
- `homework5.pdf` - rendered report
- `data/nyc_crashes_2024-06-30_to_2024-07-06.csv` - crash records
- `data/nyc_modified_zip_codes.csv` - ZIP-code lookup
- `data/nyc_borough_boundaries.geojson` - offline map boundary layer

Files created under `data/derived/` are reproducible outputs and are ignored by Git.

## Run locally

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
quarto render homework5.qmd
```

Quarto and a PDF engine such as Tectonic must be installed separately.

## Data sources

The files were downloaded on September 23, 2026 from official NYC Open Data datasets:

- [Motor Vehicle Collisions - Crashes](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)
- [Modified ZIP Code Tabulation Areas](https://data.cityofnewyork.us/Health/Modified-Zip-Code-Tabulation-Areas-MODZCTA-/pri4-ifjk)
- [Borough Boundaries](https://data.cityofnewyork.us/City-Government/Borough-Boundaries/gthc-hcne)

The crash dataset is revised over time, so row counts can differ from older rendered reports.

