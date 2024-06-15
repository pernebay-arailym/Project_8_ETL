
## Build ETL with Python

### Overview

This Python project implements an ETL (Extract, Transform, Load) process to gather data from an API listing universities in the United States, filter and structure it, and finally load it into a SQLite database.

### Notes

- **Extract:** Uses the `requests` library to fetch data from the API endpoint listing universities in the United States.

- **Transform:** Filters the dataset to include only universities located in California, converts lists of domains and web pages into comma-separated strings, and selects specific columns (`domains`, `country`, `web_pages`, `name`) for further processing.

- **Load:** Utilizes `pandas` and `SQLAlchemy` to load the transformed data into a SQLite database named `my_lite_store.db`, specifically into a table named `cal_uni`. If the table already exists, it replaces it with the new data.

- **Customization:** Modify the transformation logic (`transform` function) to suit different filtering criteria or additional data manipulation requirements.

- **Expansion:** Extend functionality by integrating with different databases (e.g., MySQL, PostgreSQL) or enhancing error handling and logging mechanisms for production environments.

