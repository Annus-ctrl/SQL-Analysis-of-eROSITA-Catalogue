## Project Overview

This project explores Galactic X-ray transients detected by the eROSITA telescope.  
Data from the VizieR catalogue was extracted, cleaned, and imported into a MySQL database.  
Various SQL queries were executed to analyze properties like luminosity, spectral classification, temperature, and population distributions of 738 X-ray transients.

## Key Features / Skills

- Data extraction and cleaning from VizieR catalogues  
- Structured ASCII table creation for database import  
- MySQL database design and optimization  
- SQL analysis: filtering, aggregation, joins, subqueries  
- Population statistics and astrophysical insights

- ## Dataset

- Source: [VizieR Catalogue J/MNRAS/544/885 – Galactic X-ray Transients in eROSITA](https://vizier.u-strasbg.fr)  
- Number of sources: 738  
- Key columns:
  - `IAUName`: Official source name
  - `RA_ICRS`, `DE_ICRS`: Coordinates
  - `FeRASS1`, `F2RXS`: X-ray fluxes
  - `Lum_W1e7`: Luminosity
  - `Temperature_K`: Effective temperature
  - `SourceClass`: Source classification
 
  - ## Project Structure

- `Galactic_Xray_Transients_Project.pdf` – Full LaTeX report  
- `data/` – CSV/ASCII files extracted from VizieR  
- `sql_queries/` – Example SQL scripts used for analysis  
- `README.md` – Project overview and instructions

- ## How to Run

1. Install MySQL and create a database `m2`.
2. Import the data using the `LOAD DATA` command:

```sql
LOAD DATA LOCAL INFILE '/path/to/AHtransients.dat'
INTO TABLE AHtransients
FIELDS TERMINATED BY '|'
LINES TERMINATED BY '\n';
```


## Key Findings

- Hottest populations: CVs, IBs, WRs, XRBs (>5000 K)  
- Most sources: SS_IB (418) and IB (110)  
- Top 5 X-ray sources identified with luminosities > 10^32 erg/s  
- Nearby bright stars (<20 pc) show measurable X-ray activity  
- Rare extreme luminosity outliers detected, e.g., 1eRASS J121314.8-645231
-
## Conclusion: This project demonstrates how MySQL can be used to explore astronomical datasets.  
The analysis reveals population trends, extreme sources, and selection biases in the eROSITA Galactic X-ray transient catalogue.

## References

- Maan et al. 2025, MNRAS 544, 885 – Galactic X-ray Transients in eROSITA
- VizieR Catalogue Service: https://vizier.u-strasbg.fr
