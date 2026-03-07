# proj
ETL Automation Script

This Python script automates the ETL (Extract, Transform, Load) process for structured data files, supporting both CSV and JSON formats. It extracts data from a specified directory, cleans and transforms it, and outputs a consolidated CSV file ready for analysis.

Features

Data Extraction: Automatically loads all .csv and .json files from a target folder.

Data Cleaning:

Converts date columns to datetime objects.

Capitalizes product names for consistency.

Removes rows with null prices.

Fills missing quantities with 0.

Removes duplicate entries.

Data Transformation: Calculates a new column Total Cost as quantity * price.

Output: Generates a single consolidated CSV file in a dedicated output folder.

Logging: Tracks key steps, warnings, and errors in a project_log.txt file for auditability.

Error Handling: Gracefully handles missing files or invalid data formats.

Usage

Place your .csv and .json files in the project folder:
C:\Users\Admin\Desktop\Project\

Run the script:

python etl_script.py

The processed dataset will be saved to:
C:\Users\Admin\Desktop\Project\output_data\ready_data.csv

Check project_log.txt for detailed logs of the ETL process.

Dependencies

Python 3.x

pandas

glob

os

logging

Install missing dependencies with:

pip install pandas
Example Output
Files found successfully: 5
Loading CSV file: sales_january.csv
Loading JSON file: sales_february.json
Data Extracted Successfully!
Data cleaning starting up...
Successfully dropped 2 null price values!
Data transformation was completed successfully!
Data was loaded successfully! ✅
Notes

Ensure all files have consistent column names (date, product, price, quantity).

The script is easily extendable to handle additional file types or transformations.
