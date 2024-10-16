# CSV-Fuzzy-Matcher

# Data Normalization Using Levenshtein Distance

## Project Overview
This project automates the process of matching and normalizing business account names and addresses across two different datasets. Using the Levenshtein distance (via the `rapidfuzz` library), the script identifies matching records even when there are discrepancies (e.g., typos, formatting differences) in account names or addresses.

### Key Features
- **Confident Matches**: High-confidence matches where name and address similarity exceeds specified thresholds.
- **Maybe Matches**: Lower-confidence matches that require manual review.

This project significantly reduces manual effort in cleaning and matching data.

---

## Project Structure
---
. ├── data/ # Folder for input CSV files │ ├── APN and OPS Combined Shop List for Loading.csv │ ├── CRM Shops Normalized Addresses.csv ├── full_data_output/ # Folder for all matches (confident and maybe) │ ├── confident_matches.csv │ ├── maybe_matches.csv ├── final_data_output/ # Folder for final matches (filtered data) │ ├── confident_matches.csv │ ├── maybe_matches.csv ├── data_matching_script.py # Main Python script ├── README.md # Documentation

## Setup Instructions

### Prerequisites
- Python 3.7+
- Required libraries: `pandas`, `rapidfuzz`, `rich`

### Install Dependencies
```bash
pip install pandas rapidfuzz rich


