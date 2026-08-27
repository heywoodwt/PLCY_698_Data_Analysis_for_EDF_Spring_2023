# EDF Disaster Relief Data Pipeline

Cleaning and merging of North Carolina disaster relief datasets for the Environmental
Defense Fund, Spring 2023.

Takes EDF's source database plus Golden LEAF Foundation funding records — spread across
Excel and CSV exports in inconsistent shapes — and produces a single analysis-ready
table keyed on county FIPS.

## Pipeline

| Notebook | Stage |
|----------|-------|
| `xlsx_2_file.ipynb` | Converts the source Excel workbooks to CSV |
| `new_clean_data.ipynb` | Normalizes column names, types, and county naming |
| `merge_csv_files.ipynb` | Joins the EDF, Golden LEAF, and FIPS location tables |
| `wrangling_data.ipynb` | Reshaping and derived fields |
| `eda_work_1.ipynb` | Exploratory analysis of the merged result |
| `import_data.py` | Loader helpers |

`final_data_with_golden_leaf.csv` is the output that feeds
[Flood_Analysis_PLCY_698](https://github.com/heywoodwt/Flood_Analysis_PLCY_698).

## Running it

```bash
pip install pandas openpyxl jupyter
jupyter lab
```

Run the notebooks in the order listed above.

