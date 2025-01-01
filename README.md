# Country-GDP-Data-ETL-processing
•	Key Features
•	Extracts data from a web page using BeautifulSoup.
•	Transforms data by converting currencies using exchange rates.
•	Loads the transformed data into both a CSV file and an SQLite database.
•	Logs progress for each ETL step for traceability.
•	Executes a query to validate the database load.

Execution Flow

Initialization:
Logs the start of the ETL process.
Specifies URLs, table attributes, file paths, and database configurations.

Extraction:
Calls the extract function to scrape data from the Wikipedia page.
Logs completion of data extraction.

Transformation:
Reads exchange rates from exchange_rate.csv.
Converts the MC_USD_Billion column into multiple currencies using exchange rates.
Logs completion of data transformation.

Loading:
Saves the transformed data to a CSV file using load_to_csv.
Loads the data into an SQLite database table using load_to_db.
Logs completion of data loading.

Validation:
Runs a query to fetch the names of the top 5 banks from the SQLite database.
Displays the results as part of the validation step.

Completion:
Logs the end of the ETL process.
Closes the database connection.

Web Page URL:
[Source: Wikipedia List of Largest Banks (Archived)](https://web.archive.org/web/20230908091635/https://en.wikipedia.org/wiki/List_of_largest_banks)
