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

## Setup Instructions

### Prerequisites
- Python 3.7+
- Required libraries: `pandas`, `rapidfuzz`, `rich`

### Install Dependencies
```bash
pip install pandas rapidfuzz rich


