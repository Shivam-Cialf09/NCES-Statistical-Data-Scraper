# NCES-Statistical-Data-Scraper 
This `README.md` file for both the NCES Acceptance Rate Scraper and SAT ACT Test scraper. This README will provide an overview of what each script does, how to set it up, and how to run it.

```markdown
# NCES Statistical Data Scraper

This repository contains two separate Python scripts for extracting statistical data from the National Center for Education Statistics (NCES) website. Each script serves a different purpose: one for scraping acceptance rates, student to faculty ratio and related statistics, and another for retrieving SAT and ACT test score data.

## Installation

Before running the scripts, ensure that you have Python installed on your system along with the following packages:
- pandas
- requests
- beautifulsoup4

You can install the required packages using the following command:
```bash
pip install pandas requests beautifulsoup4
```

## Files

1. **NCES Acceptance Rate Scraper**
   - **Purpose**: Extracts total number of applicants, percent admitted, percent admitted who enrolled, and student-to-faculty ratios.
   - **Input**: Excel file containing a list of universities with their names and NCES IDs.
   - **Output**: Excel file with extracted data for each university.

2. **SAT ACT Test Code Scraper**
   - **Purpose**: Extracts SAT and ACT test scores data including percent of students submitting scores and percentile ranges.
   - **Input**: Excel file containing a list of universities with their names and NCES IDs.
   - **Output**: Excel file with extracted data for each university.

## Usage

### NCES Acceptance Rate Scraper

1. **Modify Input/Output Paths**: Open the script and set the `input_file` and `output_file` paths to your Excel files.
   
   ```python
   input_file = r'/path/to/input.xlsx'
   output_file = r'/path/to/output.xlsx'
   ```

2. **Run the Script**: Execute the script in your terminal or command prompt:

   ```bash
   python nces_acceptance_rate_scraper.py
   ```

### SAT ACT Test Code Scraper

1. **Modify Input/Output Paths**: Open the script and set the `input_file` and `output_file` paths to your Excel files.
   
   ```python
   input_file = r'/path/to/input.xlsx'
   output_file = r'/path/to/output.xlsx'
   ```

2. **Run the Script**: Execute the script in your terminal or command prompt:

   ```bash
   python sat_act_test_code_scraper.py
   ```

## Configuration

Both scripts allow configuration of the range of rows to process from the input Excel file, facilitating partial data extraction for large datasets.

## Note

Ensure that the Excel file used as input contains columns specifically named 'University Name' and 'NCES ID' as these are used by the scripts to construct URLs for data extraction.

## Troubleshooting

- If you encounter any issues with missing data or errors, check the console output for error messages that can help in diagnosing the problem.
- Verify that the NCES website has not changed its structure, as this could affect the script's ability to find and extract data.
