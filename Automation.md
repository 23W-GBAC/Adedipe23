# Week 1: Data Collection and Preprocessing
we will focus on gathering relevant data for my AI blog post and preprocessing it for analysis.
## Python Script:
# Week 1 - Data Collection and Preprocessing

# Import necessary libraries
import requests
import pandas as pd

# Step 1: Collect data from a web source (e.g., an API)
url = "https://api.example.com/data"
response = requests.get(url)
data = response.json()

# Step 2: Convert data to a DataFrame for easier manipulation
df = pd.DataFrame(data)

# Step 3: Handle missing values or outliers
df = df.dropna()  # Example: Removing rows with missing values

# Step 4: Save the preprocessed data for future use
df.to_csv("preprocessed_data.csv", index=False)

## Errors and Solutions:

Error: Connection issues while fetching data.
Solution: Add error handling using try-except blocks.
Error: Inconsistent data format from the API.
Solution: Check the API documentation and modify the script to handle different data formats.
Error: Unanticipated missing values.
Solution: Implement more robust methods for handling missing values, such as imputation.
