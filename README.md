# README

## World Population Scraping Script

This repository contains a Python script for scraping world population data from the website [Worldometers](https://www.worldometers.info/). The script collects various population metrics for different countries and saves the data into a CSV file.

### Prerequisites

To run this script, you'll need the following Python packages:
- `requests`
- `beautifulsoup4`
- `pandas`

You can install these packages using pip:

```bash
pip install requests beautifulsoup4 pandas
```

### Script Overview

The script performs the following tasks:

1. **Send a GET request to the Worldometers population page**:
   - Retrieves the HTML content of the main population page.

2. **Parse the HTML content**:
   - Uses BeautifulSoup to parse the HTML content and find all country links.

3. **Filter and clean country links**:
   - Removes irrelevant links from the initial list of country links.

4. **Scrape data for each country**:
   - Iterates through each country link, sending GET requests to the respective country population pages.
   - Extracts relevant data from the population tables.

5. **Store the data in a dictionary**:
   - Organizes the extracted data into a dictionary with the following keys:
     - Country
     - Year
     - Population
     - Yearly % Change
     - Yearly Change
     - Migrants (net)
     - Median Age
     - Fertility Rate
     - Density (P/Km²)
     - Urban Pop %
     - Urban Population
     - Country's Share of World Pop
     - World Population
     - Global Rank

6. **Save the data to a CSV file**:
   - Converts the dictionary to a Pandas DataFrame and saves it as `world_population.csv`.

### How to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/world_population_scraping.git
   cd world_population_scraping
   ```

2. **Run the script**:
   ```bash
   python world_population_scrapping.ipynb
   ```

3. **Output**:
   - The script will create a CSV file named `world_population.csv` in the current directory containing the scraped population data.

### Notes

- Ensure you have a stable internet connection as the script sends multiple GET requests to the Worldometers website.
- The script skips the "Channel Islands" as its data structure differs from other countries on the website.

### Contributing

If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.

### License

This project is licensed under the MIT License.

---
