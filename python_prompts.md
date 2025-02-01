# Python Code Generation Prompts

## Prompt 1: API Integration
**Input Prompt:**  
"Generate a Python function to fetch data from a REST API using the `requests` library. Include error handling for HTTP errors and timeouts."

**Example Output:**  
```python
import requests

def fetch_data(url):
    try:
        response = requests.get(url, timeout=10)
        response.raise_for_status()
        return response.json()
    except requests.exceptions.RequestException as e:
        print(f"Error fetching data: {e}")
        return None
## Prompt 2: Data Processing
**Input Prompt:**  
"Write a Python script to read a CSV file, clean the data by removing null values, and save the cleaned data to a new CSV file."

**Example Output:**  
```python
import pandas as pd

def clean_csv(input_file, output_file):
    df = pd.read_csv(input_file)
    df.dropna(inplace=True)
    df.to_csv(output_file, index=False)
