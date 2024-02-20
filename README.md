# SportScrapeR

Adjusting the outline to specify the use of the `rvest` package for scraping sports data from Sports Reference sites enhances clarity on the technical approach for data collection. Here's the revised package structure with `rvest` integration highlighted:

### Package Structure with `rvest` Integration

#### 1. Data Collection with `rvest`

- **Function:** `scrape_sports_data_rvest()`
  - **Purpose:** Utilizes `rvest` to scrape sports data from Sports Reference websites for NFL, NBA, and MLS teams over the past 10 years.
  - **Parameters:** league (NFL/NBA/MLS), years (array of years for data collection)
  - **Returns:** Raw data frames of team data for the specified years and leagues.
  - **File Location:** `R/scrape_sports_data_rvest.R`
  - **Note:** Implement `rvest` selectors to navigate and extract data from HTML pages of Sports Reference websites.

#### 2. Data Cleaning

- **Function:** `clean_sports_data()`
  - **Purpose:** Cleans and preprocesses the raw scraped sports data.
  - **Parameters:** raw_data (data frame of raw scraped data)
  - **Returns:** Cleaned and preprocessed data frame.
  - **File Location:** `R/clean_sports_data.R`

#### 3. Data Transformation

- **Function:** `transform_team_data()`
  - **Purpose:** Transforms cleaned data into a structured format focusing on teams and their performance metrics.
  - **Parameters:** cleaned_data (data frame of cleaned sports data)
  - **Returns:** Transformed data frame with metrics suitable for analysis.
  - **File Location:** `R/transform_team_data.R`

#### 4. Data Storage

- **Function:** `save_team_data()`
  - **Purpose:** Saves the transformed team data in a specified format.
  - **Parameters:** team_data (transformed data frame), file_path (destination path), format (CSV/JSON/etc.)
  - **Returns:** Message indicating successful data storage.
  - **File Location:** `R/save_team_data.R`

#### 5. Utility Functions

- **Function:** `get_teams_last_10_years_rvest()`
  - **Purpose:** Orchestrates the scraping, cleaning, transforming, and saving of team data for the last 10 years using `rvest`.
  - **Parameters:** league (NFL/NBA/MLS), save_path (where to save data), format (data format)
  - **Returns:** Message indicating the completion of data processing and storage.
  - **File Location:** `R/get_teams_last_10_years_rvest.R`

### Additional Components

- **Documentation:** Create documentation for each function in `man/`, detailing how `rvest` is used for scraping.
- **Tests:** Provide unit tests in `tests/testthat/` to ensure the accuracy and functionality of your scraping and data processing with `rvest`.
- **Data:** For sample datasets or examples, use the `data/` directory.

This revised outline emphasizes the use of `rvest` for web scraping, ensuring a clear understanding of the methods and technologies used in the package for collecting sports data.
