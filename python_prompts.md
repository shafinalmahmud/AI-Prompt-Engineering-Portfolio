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
