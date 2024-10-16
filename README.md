# CSV-Fuzzy-Matcher

# Data Normalization Using Levenshtein Distance

## Project Overview
This project is designed to automate the process of matching and normalizing business account names and addresses across two different datasets. By using the Levenshtein distance (implemented via the `rapidfuzz` library), the script identifies matching records even when there are small discrepancies (e.g., typos or different formatting) in account names or addresses. The output of this process includes two sets of matches:
- **Confident matches**: High-confidence matches where the name and address similarity exceeds specified thresholds.
- **Maybe matches**: Lower-confidence matches that still have a reasonable chance of being correct but require manual review.

This solution significantly reduces manual labor in cleaning and matching data, saving up to 20 hours of work per month.

## Project Structure
```bash
.
├── data/                       # Folder for input CSV files
│   ├── APN and OPS Combined Shop List for Loading.csv
│   ├── CRM Shops Normalized Addresses.csv
├── full_data_output/            # Folder for all matches (confident and maybe)
│   ├── confident_matches.csv
│   ├── maybe_matches.csv
├── final_data_output/           # Folder for final matches (filtered data)
│   ├── confident_matches.csv
│   ├── maybe_matches.csv
├── data_matching_script.py      # Main Python script
├── README.md                    # Documentation


