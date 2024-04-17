# Fetch Clinical Trials Studies Script (Jupyter Notebook)

## Introduction
This Jupyter Notebook fetches studies from the ClinicalTrials.gov API and saves them to Parquet files. It allows filtering studies based on the last update date and provides options for setting page size and the number of pages per Parquet file.

## Dependencies
- `requests`: Library for making HTTP requests
- `pandas`: Library for data manipulation and analysis
- `tqdm`: Library for displaying progress bars

## Instructions
1. Clone or download the Jupyter Notebook to your local machine.
2. Ensure you have Python installed along with the required dependencies.
3. Open the Jupyter Notebook in your preferred environment.
4. Run each cell sequentially to define the functions and main logic.
5. Execute the cell containing the main function `fetch_studies()` with the desired parameters.
6. Monitor the execution progress within the notebook.
7. Once the execution completes, you can find the saved Parquet files in the `output_parquet` folder, located in the directory where your Jupyter Notebook is located when you run the script.

## Parameters
- `from_date` (optional): Specifies the date in YYYY-MM-DD format from which to fetch studies. If provided, the function will pull only studies that have been updated on or after this date. Defaults to `None`.
- `pageSize` (optional): Number of studies to fetch per page. Defaults to `100`.
- `pagePerParquet` (optional): Number of pages to save per Parquet file. Defaults to `50`.

## Log File
The script generates a log file named `fetch_studies.log`, which logs information about the execution, including any errors encountered during the process. It will be located in the directory where your Jupyter Notebook is located when you run the script.

## Example Usage
To fetch studies updated since April 10, 2024, and save every 100 pages to 1 Parquet file, while fetching 200 studies per page, execute the following code within the notebook:

```python
fetch_studies(from_date='2024-04-10', pageSize=200, pagePerParquet=100)