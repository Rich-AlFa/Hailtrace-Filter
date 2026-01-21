# Hailtrace Filter

**Clean and filter raw Hailtrace lead exports into high-quality, targeted lists ready for calling in seconds.**

This Jupyter-based automation takes messy raw CSV exports from Hailtrace ( addresses, home values, property types, etc.), applies smart filters for targeted housing types and home value ranges, cleans inconsistent data, and outputs a polished, ready-to-use lead file.

**Main benefit**: What used to take 1–2 hours of manual Excel filtering, sorting, removing junk addresses, and reformatting now happens in just a few clicks — saving time every storm season.

## ✨ Features

- Filters leads by housing type (e.g. single-family homes only, exclude apartments/mobile homes)
- Optional filter to target specific zip code or city list.
- Applies home value thresholds (e.g. keep only properties above $X to focus on higher-value targets)
- Cleans addresses, removes duplicates/invalids, standardizes formatting
- Handles Hailtrace-specific columns (phone number, address, home value, zipcodes, etc.)
- Produces clean output CSV files named and organized inside a folder created by the script: `Filter Output.csv` (or custom naming)
- Reproducible with Jupyter Notebooks – easy to tweak filters
- Splits Cellphones, Landlines and also stores records without home value for later processing into a sepparate file.

## 📊 Before vs After

| Task                          | Manual Process (Excel)   | With This Automation     |
|-------------------------------|---------------------------|---------------------------|
| Time to prepare lead list     | 1–2 hours                | ~2–10 minutes            |
| Filtering housing & value     | Tedious manual selection | One-time code adjustment |
| Cleaning bad/invalid data     | Error-prone              | Automated & consistent   |
| Daily/weekly repetition       | Frustrating              | Run notebook & done      |
| Output quality                | Varies person-to-person  | Always clean & targeted  |

## 🛠️ Technologies Used

- **Language**: Python 3
- **Core library**: pandas (data filtering, cleaning & CSV I/O)
- **Environment**: Jupyter Notebook
- **No external APIs** or heavy dependencies

## 📁 Project Structure

```text
Hailtrace-Filter/
├── HAILTRACE_FILTER_2.1.ipynb     ← Main/updated notebook for filtering leads
├── FILTER UPDATED.ipynb           ← Alternative/earlier version (if needed)
├── README.md
└── (Input file --raw_hailtrace_export.xlsx-- [not included for privacy] – add your data here)
    ├── filtered_leads_output-cell.csv (cellphone list)   ← Output file (Mobile numbers) created and stored in the "Filter Output" folder created in the process.
    └── filtered_leads_output-land.csv (landline list)    ← Output file (Landline numbers) created and stored in the "Filter Output" folder created in the process.
```
## 🚀 Quick Start / Usage

1. Clone the repository
```
Bashgit clone https://github.com/Rich-AlFa/Hailtrace-Filter.git
cd Hailtrace-Filter
```
2. Install dependencies
```
Bashpip install pandas jupyter
```
3. Prepare your data
```
- Export your leads from Hailtrace as CSV (download residential list from the swath or shape selected) into the same folder containing this jupyter file
- Name the file accordingly and place it in a dedicated folder (since the script takes all excel files in the folder and concatenates them)
```

4. Run the notebook
Launch Jupyter:
```
- Bashjupyter notebook
- Open HAILTRACE_FILTER_2.3.ipynb (or the most recent one)
- Adjust filters if needed (zip codes requested, cities requested, min_home_value, etc. – look for the variables near the top)
- Run all cells (Shift+Enter or "Run All")
- Output folder and files appears: Filter output > filename-cell.csv / filename-land.csv / filename-missing_homevalue.csv
```
Use the filtered CSV directly in your CRM, dialing tool, or print lists.

Done! 🎯
