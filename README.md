# Journal_Finder

# Springer Journal Scraper

This project is focused on scraping journal data from the Springer website and storing it in an SQLite database. It also updates journal details such as publishing models, impact factors, submission times, and download statistics. Below are the main functions included in the project.

## Key Functions

### 1. `build_search_url(keywords)`
- Dynamically builds the search URL using keywords to query the Springer website.
  
### 2. `create_empty_table(db_name, table_name)`
- Creates a new SQLite table to store journal information, including fields such as `journal_name`, `journal_link`, `paper_title`, `publication_date`, and other metrics like impact factors and downloads.

### 3. `scrape_springer_journals(search_url, num_pages, db_name, table_name)`
- Scrapes journal and article details (e.g., journal name, paper title, publication date) from the Springer website and stores them in the SQLite database.
- Skips duplicate entries based on journal name and link to avoid redundant data.

### 4. `scrape_journal_details(db_name, table_name, row_limit=None)`
- Retrieves journal details that are missing important metrics (e.g., impact factor, publishing model) from the database and updates them by scraping the Springer website.
- Allows processing of all rows, or just a limited number if `row_limit` is set.

### 5. `update_frequency(db_name, table_name)`
- Updates the frequency of duplicate journal entries based on journal name and link, ensuring only one unique entry exists for each journal while counting repeated occurrences.

## How It Works

1. **Search and Scrape**: The `scrape_springer_journals` function scrapes journal data based on a dynamic URL built from keywords and stores the results in the database.
2. **Update Details**: The `scrape_journal_details` function updates journal information such as publishing models, impact factors, and downloads by fetching them from the Springer website.
3. **Manage Duplicates**: The `update_frequency` function manages repeated journal entries, updating their frequency and ensuring each journal has a unique entry.

