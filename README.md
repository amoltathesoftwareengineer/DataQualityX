# DataQualityX

**A Python toolkit for data validation, quality monitoring, and reliable data processing.**

DataQualityX is a data quality toolkit designed to help developers and data professionals identify common data issues before using datasets for analytics, reporting, or ETL pipelines.

It provides a foundation for validating data, detecting inconsistencies, and generating structured quality reports.

## Features

- **Missing Value Detection:** Identify null and missing values in datasets.
- **Duplicate Detection:** Find duplicate records using configurable rules.
- **Data Type Validation:** Check whether columns contain expected data types.
- **Schema Validation:** Compare dataset columns against a defined schema.
- **Value Range Checks:** Detect values outside acceptable limits.
- **Consistency Checks:** Validate basic relationships between fields.
- **Quality Reports:** Summarize validation results and detected issues.
- **Reusable Validation Rules:** Apply reusable checks to different datasets.
- **ETL Integration:** Support data quality checks within data processing workflows.
- **Automated Testing:** Validate toolkit functionality with Pytest.

## Technology Stack

- Python
- Pandas
- Pytest
- CSV and JSON
- GitHub Actions

## Project Structure

```text
DataQualityX/
├── src/
│   └── dataqualityx/
│       ├── __init__.py
│       ├── validators.py
│       ├── checks.py
│       └── reports.py
├── tests/
│   ├── test_validators.py
│   └── test_checks.py
├── examples/
│   └── sample_data.csv
├── .github/
│   └── workflows/
│       └── ci.yml
├── pyproject.toml
├── requirements-dev.txt
├── .gitignore
├── LICENSE
└── README.md
```

## Requirements

- Python 3.10 or newer
- pip

## Installation

Clone your repository:

```bash
git clone https://github.com/amoltathesoftwareengineer/DataQualityX.git
cd DataQualityX
```

Create a virtual environment on Windows:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

Install the package and development dependencies:

```bash
python -m pip install --upgrade pip
pip install -e .
pip install -r requirements-dev.txt
```

## Usage

The following example illustrates the intended API. The corresponding validation functions must be implemented in the package before this example can run.

```python
import pandas as pd

from dataqualityx.validators import validate_dataset

df = pd.read_csv("examples/sample_data.csv")

report = validate_dataset(
    df,
    required_columns=["customer_id", "email"],
    check_duplicates=True,
)

print(report)
```

## Validation Capabilities

DataQualityX is designed to support checks such as:

| Check | Purpose |
|---|---|
| Missing values | Find incomplete records |
| Duplicate rows | Identify repeated records |
| Required columns | Detect missing fields |
| Data types | Check column type consistency |
| Value ranges | Find invalid numeric values |
| Data consistency | Identify rule violations |

## Running Tests

Run the automated test suite:

```bash
python -m pytest
```

## Example Use Cases

- Validate customer data before loading it into a database.
- Check CSV files before ETL processing.
- Detect duplicate transaction records.
- Verify data completeness before creating Power BI reports.
- Generate data quality summaries for analytics workflows.

## Roadmap

- [ ] Implement reusable validation functions.
- [ ] Add missing-value and duplicate detection.
- [ ] Implement schema and data type validation.
- [ ] Generate JSON and text reports.
- [ ] Add CSV input support.
- [ ] Build automated unit tests.
- [ ] Configure GitHub Actions.
- [ ] Add examples and developer documentation.

## License

Add an appropriate open-source license before distributing the project.

## Author

**Amol Tathe**

GitHub: https://github.com/amoltathesoftwareengineer
