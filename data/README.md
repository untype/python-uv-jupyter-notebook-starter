# Data Directory

This directory contains all datasets used in the project.

## Structure

- **`raw/`** - Original, immutable datasets (never modify these files)
  - Place your original CSV, Excel, JSON, or other data files here
  - Example: `data/raw/sales_data.csv`

- **`processed/`** - Cleaned and transformed datasets
  - Store intermediate data after cleaning, merging, or feature engineering
  - Example: `data/processed/sales_data_cleaned.csv`

- **`external/`** - External data from third-party sources
  - Reference data, lookup tables, or data from APIs
  - Example: `data/external/country_codes.json`

## Best Practices

1. **Never modify raw data** - Keep original files untouched for reproducibility
2. **Document your data** - Add a brief description of each dataset
3. **Use relative paths** - In notebooks, use `data/raw/filename.csv`
4. **Version control** - Large files (>100MB) should use Git LFS or be excluded from git
5. **Add metadata** - Consider including a data dictionary or schema documentation

## Usage in Notebooks

```python
import pandas as pd

# Load raw data
df = pd.read_csv('data/raw/your_dataset.csv')

# After processing, save to processed/
df.to_csv('data/processed/your_dataset_cleaned.csv', index=False)
```
