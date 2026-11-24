# Data folder

All files in `raw/` are csv exports of the study spreadsheets. Volunteers are 
identified only by study number

## Study design

About 140 overweight volunteers consumed a maqui–citrus beverage daily for two 
months. The beverage was sweetened with one of three sweeteners (between-subject 
factor), and plasma and urine were sampled at baseline and at the end of the 
intervention (within-subject factor). Metabolites were quantified by 
UHPLC-ESI-QqQ-MS/MS.

| Sweetener letter | Code | Sweetener | Study ID range |
|---|---|---|---|
| A | ST | Stevia | 1–46 |
| B | SU | Sucralose | 51–96 |
| C | SA | Sucrose (*sacarosa*) | 101–146 |

## Files

| File | Used for | Contents |
|---|---|---|
| `chronicPlasmAnt.csv` | plasma paper | Anthocyanin-derived (poly)phenol metabolites in plasma |
| `chronicPlasmFlav.csv` | plasma paper | Flavanone metabolites in plasma |
| `chronicUrineAnt.csv` | urine paper | Anthocyanin-derived (poly)phenol metabolites in urine|
| `chronicUrineFlav.csv` | urine paper | Flavanone metabolites in urine|
| `chronicSexVolunteers.csv` | both | `numVol` (study number for volunteer), `Sex` (`HOMBRE`/`MUJER`; 80 men, 58 women) |

### Sample codes (`grouping` column)

`"<n> <sweet><time>"`, for example `"12 B0"` or `"7 AF"`. `n` is the volunteer's number within
the group (1–46), `sweet` is A/B/C (type of sweetener, table above), and `time` is `0` (baseline) or `F` (after
two months). The study-wide ID is `n` + 0 / 50 / 100 for sweeteners A / B / C.
