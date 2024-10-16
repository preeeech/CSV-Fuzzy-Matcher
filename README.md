# CSV-Fuzzy-Matcher
Data Normalization Using Levenshtein Distance

## Project Overview
This project is designed to automate the process of matching and normalizing business account names and addresses across two different datasets. By using the Levenshtein distance (implemented via the `rapidfuzz` library), the script identifies matching records even when there are small discrepancies (e.g., typos or different formatting) in account names or addresses. The output of this process includes two sets of matches:
- **Confident matches**: High-confidence matches where the name and address similarity exceeds specified thresholds.
- **Maybe matches**: Lower-confidence matches that still have a reasonable chance of being correct but require manual review.

This solution significantly reduces manual labor in cleaning and matching data

### Setup Instructions
Prerequisites: To run this project, ensure that you have the following installed:
-**Python 3.7+**
-**Required Python libraries**

Required Libraries
-**You can install the necessary libraries by running**
```pip install pandas rapidfuzz rich```


## Key Concepts in the Script

### Data Normalization
The script normalizes the account names and addresses by converting everything to lowercase and replacing common address terms (like "Street" with "St.") to ensure consistent matching.

### Matching Process
The script uses Levenshtein distance to calculate the similarity ratio between account names and addresses in two datasets:

- **Name Ratio**: Measures the similarity between account names.
- **Address Ratio**: Measures the similarity between addresses.
- **Weighted Ratio**: Combines name and address similarity with weights (60% for address, 40% for name).

### Matching Criteria
- **Confident Matches**: Records are considered a confident match if the weighted similarity exceeds a threshold or if the name or address matches almost exactly.
- **Maybe Matches**: Records with lower, but still significant, similarity scores are categorized as maybe matches.

### Example Output
In the `final_data_output/` folder, you'll find two CSV files:

- **confident_matches.csv**: Contains high-confidence matches, where both name and address are likely correct.
- **maybe_matches.csv**: Contains lower-confidence matches, which may need manual review.

### Customization
You can adjust the matching thresholds, weights, or normalization rules to fit your specific dataset or use case. This can be done in the following sections of the code:

- **Thresholds for confident and maybe matches**: Modify in the `Confident` and `Maybe` classes.
- **Normalization rules**: Add more rules to the `normalization_replacement` dictionary if you encounter additional address abbreviations.
