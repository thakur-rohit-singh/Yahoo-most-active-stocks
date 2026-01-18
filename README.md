# Yahoo Most Active Stocks Scraper

This project automates the process of scraping **Most Active Stocks** data from **Yahoo Finance** using **Selenium (Python)**.
It navigates through the website like a real user, extracts stock data across **all pages**, cleans it, and exports the final dataset to an **Excel file**.

---

## Project Overview

Yahoo Finance loads stock data dynamically, which makes simple HTTP-based scraping unreliable.
To handle this, the project uses **Selenium with ActionChains** to:

1. Hover over the **Markets** menu
2. Navigate to **Trending Tickers**
3. Click on **Most Active**
4. Traverse through **all pagination pages**
5. Scrape and clean stock data
6. Save the output as an Excel file

---

## Data Collected

For each stock, the following fields are extracted:

* **Symbol** – Stock ticker symbol
* **Price** – Current market price (USD)
* **Change** – Price change from the previous close
* **Volume** – Total traded volume
* **Market Cap** – Company market capitalization
* **P/E Ratio** – Price-to-Earnings ratio

---

## Technologies Used

* Python
* Selenium
* Chrome WebDriver
* Pandas
* NumPy


---

## Project Flow

1. Launch the browser and maximize the window
2. Load the Yahoo Finance homepage
3. Wait until the page is ready using explicit waits and `document.readyState`
4. Hover over the **Markets** menu using ActionChains
5. Hover over **Stocks** under the Markets menu
6. Click **Trending Tickers → Most Active**
7. Scrape stock data from the table on the page
8. Store each stock’s data in dictionaries
9. Append the dictionaries to a list
10. Click the **Next** button to move to the next page
11. Repeat scraping until all pages are completed
12. Convert the collected data into a Pandas DataFrame
13. Clean and normalize the data (prices, volume, market cap, ratios)
14. Export the final cleaned data to an Excel file

---

## Output

The final cleaned dataset is saved as:

---

Project: *Yahoo Most Active Stocks*





