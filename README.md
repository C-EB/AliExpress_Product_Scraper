# AliExpress Product Data Scraper (Selenium-Based)

## 🎯 Project Objective

This project automates the extraction of product information from **AliExpress** using **Selenium** and **undetected ChromeDriver**. It is designed to perform **keyword-based product searches**, navigate through multiple result pages, and extract relevant product details into structured data files. The scraper provides a scalable and reliable solution for **e-commerce analysis**, **competitor monitoring**, and **market research**.

---

## ⚙️ How the Scraper Works

The scraper mimics human browsing behavior to avoid detection and ensure accurate data retrieval from dynamic pages. Its workflow includes:

- **Keyword-Based Search**: Accepts a list of predefined search queries (e.g., "laptop", "smartphone").
- **Popup Management**: Automatically detects and closes popups that block the view or interaction.
- **Human-Like Typing & Scrolling**: Simulates natural user input and scrolling to ensure content is fully loaded.
- **Pagination Handling**: Navigates through multiple result pages for each query (default: 5 pages).
- **Dynamic Content Loading**: Scrolls progressively and waits to allow JavaScript-rendered content to load completely.
- **Error Resilience**: Implements try-except blocks and fallback logic to handle unexpected page structures or missing data.

---

## 📦 Extracted Data

For each product on the search result pages, the scraper collects:

- **📝 Product Name**: Cleaned and structured name text.
- **🔗 Product URL**: Direct link to the product detail page.
- **💰 Current Price**: Parsed and normalized price after discounts (if available).
- **💲 Original Price**: Displayed price before discount (if provided).
- **⭐ Rating**: Average customer rating.
- **📦 Total Orders**: Number of purchases made.
- **🖼️ Thumbnail Image URL**: Product preview image link.
- **📅 Timestamp**: Exact scrape date and time in ISO format.

---

## 📁 Output & Logging

Each query generates a **CSV file** named after the search term (e.g., `laptop_aliexpress_products.csv`), containing all extracted product entries from multiple pages. The structure ensures easy parsing and downstream processing.

Key output characteristics:

- **Structured CSV Format** for compatibility with Excel, Pandas, and databases.
- **Error Logging to Console** for skipped products or failed pages.
- **Per-Query Data Segmentation** for clarity in analysis.

---

## 🧠 Technical Highlights

This scraper demonstrates advanced automation techniques and robustness features:

- **Undetected ChromeDriver**: Bypasses bot-detection mechanisms on AliExpress.
- **CSS Selector Precision**: Targets dynamic DOM elements using stable and specific selectors.
- **Scroll & Wait Strategy**: Mimics real user interaction to trigger lazy-loaded content.
- **Intelligent Retry Logic**: Handles UI elements failing to appear (e.g., pagination buttons or price fields).
- **Modular & Extensible**: Designed with separate functions for typing, scrolling, parsing, and exporting.

---

## 📈 Business & Market Research Applications

This scraper can be a powerful asset for:

- **E-Commerce Competitor Analysis**: Track price changes, promotions, and best-sellers.
- **Product Research**: Identify trending products and analyze customer sentiment via ratings and orders.
- **Market Intelligence**: Collect cross-category data to evaluate niche markets or identify new opportunities.
- **Price Monitoring Tools**: Feed data into dashboards or price alert systems.

The automation is **production-ready**, scalable to more queries or categories, and adaptable to changing site structures with minimal effort.
