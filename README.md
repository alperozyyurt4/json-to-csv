# JSON to CSV Converter

This Python script helps you transform a JSON file into a CSV file by removing unnecessary fields and flattening nested data. It's a practical solution for cleaning and preparing JSON data for analysis or reporting.

## Key Features

- Removes specified fields from both the main JSON structure and nested `details` elements.
- Flattens nested `details` into top-level CSV columns with a `details_` prefix.
- Automatically generates CSV headers based on the cleaned data.

## Quick Start

### Prerequisites
- Python 3.x installed on your system.

### Steps to Run
1. Clone this repository to your local machine:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd <repository-directory>
   ```
3. Place your JSON file in the same directory and name it `test.json`.
4. Run the script:
   ```bash
   python json_to_csv_clean.py
   ```
5. The cleaned CSV will be saved as `test.csv` in the same directory.

## Customization

### Modify Fields to Remove
You can change the fields to be excluded by editing the script:

- **Top-level fields:** Update the `removed_tags` list.
- **Nested `details` fields:** Update the `removed_details_tags` list.

Example:
```python
removed_tags = ['unwanted_field1', 'unwanted_field2']
removed_details_tags = ['nested_field1', 'nested_field2']
```

## Example Input and Output

### Input JSON (`test.json`):
```json
[
    {
        "id": 1,
        "unwanted_field": "value",
        "details": [
            {"nested_field": "value", "useful_field": "data"}
        ]
    }
]
```

### Output CSV (`test.csv`):
```
id,details_useful_field
1,data
```

## Contribution
We welcome contributions! Feel free to fork the repository and submit pull requests to improve the script or add new features.

## License
This project is licensed under the MIT License.

## Support
For any questions or feedback, please open an issue in the repository.

