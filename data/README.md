# Dataset Description

## Overview
- File: `combined_data.zip`
- Format: CSV (when unzipped)
- Total samples: 148,088
- Features: 24
- Target classes: 14
- Preprocessed samples: 89,014 (after duplicate removal)

## Class Distribution
```
[17384  5479  6320  1617  4549  2143 14734 13046  4054  6275  1136  1574  1565  9138]
```

## Setup Instructions
1. Unzip the data file:
```bash
cd data
unzip combined_data.csv.zip
```

2. Verify the CSV file is present:
```bash
ls -l combined_data.csv
```

The pipeline will automatically read `combined_data.csv` when running.

## Data Privacy
Note: This dataset is included in the .gitignore file to prevent committing large data files to the repository.