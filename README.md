# Netflix Titles – Data Cleaning

This repository contains a data cleaning script for `netflix_titles.csv`.

## Tasks Performed
1. **Identify and handle missing values**  
   - Used `df.isnull().sum()` to detect missing values.  
   - Filled missing values in `director`, `cast`, `country`, and `rating` with `"Unknown"`.  

2. **Remove duplicates**  
   - Used `df.drop_duplicates()` to remove duplicate rows.  

3. **Standardize text values**  
   - Trimmed whitespace in all text columns.  
   - Standardized `country` names to Title Case (e.g., `"united states, india"` → `"United States, India"`).  
   - Standardized `type` (e.g., `"Movie"` / `"Tv Show"`) and made `rating` uppercase.  

4. **Convert date formats**  
   - Converted `date_added` column to `datetime`.  
   - Created a new column `date_added_standard` in `dd-mm-yyyy` format.  

5. **Rename column headers**  
   - All column names are lowercase with underscores (e.g., `"Date Added"` → `"date_added"`).  

6. **Check and fix data types**  
   - `release_year` → integer (`Int64`).  
   - `date_added` → datetime.  

## Files
- `cleaning_script.py` → Python script with all steps.  
- `netflix_titles_cleaned.csv` → Output file after cleaning (generated when you run the script).  

## How to Run
1. Place `netflix_titles.csv` and `cleaning_script.py` in the same folder.  
2. Run the script:  
   ```bash
   python cleaning_script.py
