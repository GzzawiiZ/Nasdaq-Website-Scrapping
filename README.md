
---

# Nasdaq Website Scraping Project

## Project Overview
This project is designed to scrape financial data from the Nasdaq website. It aims to gather stock prices, trading volumes, and other relevant market data for analysis and monitoring purposes. This tool can be used by investors, analysts, and financial enthusiasts to obtain up-to-date information directly from Nasdaq.

## Technologies Used
This project leverages a range of technologies and libraries to facilitate web scraping, data manipulation, and visualization:
- **Python 3.8+**: The core programming language used for all scripting and automation.
- **Selenium**: A powerful tool to automate web browsers, allowing us to interact with web pages programmatically.
- **WebDriver Manager**: Simplifies the management of binary drivers for different browsers.
- **Pandas**: Used for data manipulation and analysis; crucial for handling and organizing data in tabular form.
- **Matplotlib**: A plotting library for creating static, interactive, and animated visualizations in Python.
- **Requests**: Allows sending HTTP requests in Python, essential for web scraping tasks where API calls are needed.
- **Beautiful Soup 4 (bs4)**: A Python library for pulling data out of HTML and XML files, ideal for parsing web pages.
- **Pillow (PIL)**: The Python Imaging Library adds image processing capabilities to your Python interpreter.
- **Random**: Provides functionalities to generate random numbers, crucial for implementing delays and mimicking human interaction patterns to avoid detection while scraping.
- **Time**: Used to handle various time-related tasks, especially adding delays between web page interactions to prevent overloading the server.
- **os**: Provides a way of using operating system dependent functionality to interact with the file system.
- **RE**: A module that provides support for regular expressions in Python. It is used for searching, matching, or splitting strings based on specific patterns. This is particularly useful in extracting information from structured text like HTML/XML content.
- **Laambda **:Anonymous functions defined by the `lambda` keyword in Python. These functions are small, contain no name, and are limited to a single expression. They are extensively used in the project for inline operations like sorting, filtering, or mapping data, providing a concise and functional approach to handling data transformations.

## Features
- Scrape real-time stock prices.
- Extract historical data for any specific ticker.
- Generate and save data reports in CSV format.

## Setup Instructions
1. **Clone the Repository**
   ```bash
   git clone https://github.com/GzzawiiZ/Nasdaq-Website-Scrapping.git
   cd Nasdaq-Website-Scrapping
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Usage
This project includes several functions to scrape and process data from the Nasdaq website. Here’s how to use each function:
To start scraping data from the Nasdaq website:
Just run the first cell in `Main.ipynb`
1. **Scraping Stock Data**
   - **Function**: `get_stock(S_table)`
   - **Description**: This function scrapes data based on the specified table type from the Nasdaq website. The `S_table` parameter can be one of the following: `nextFiscalQ`, `nextFiscalY`, `currentQ`, `currentY`.
   - **Example**:
     ```python
     print(get_stock("nextFiscalQ"))
     ```

2. **Fetching Dividend History**
   - **Function**: `get_log(company_symbol)`
   - **Description**: Retrieves the dividend history for a given stock symbol.
   - **Example**:
     ```python
     print(get_log("AAPL"))
     ```

3. **Retrieving Analyst Recommendations**
   - **Function**: `get_recommendation(company_symbol)`
   - **Description**: Fetches the latest analyst recommendations for a specific stock symbol.
   - **Example**:
     ```python
     get_recommendation("GOOGL"))
     ```

4. **Generating Analyst Target Price Graph**
   - **Function**: `get_graph(company_symbol)`
   - **Description**: Downloads and displays a graph of analyst target prices for a specified stock symbol.
   - **Example**:
     ```python
     get_graph("MSFT")
     ```

5. **Downloading Images from Nasdaq Events Page**
   - **Function**: `get_photos()`
   - **Description**: Downloads and saves the first ten images from the Nasdaq events page.
   - **Example**:
     ```python
      get_photos()'
     ```

Each function is designed to be executed within the Python environment. Ensure you have the necessary libraries installed and the browser driver set up correctly as per the project's setup instructions. This modular approach allows users to execute specific parts of the script based on their data needs.


## Output

Data retrieved by the functions is stored in pandas DataFrame. If you wish to save this data as a CSV file, you can use the following Python code snippet for each function's DataFrame output:

```python
# Assuming 'df' is the DataFrame variable name holding your data
df.to_csv('filename.csv', index=False)
```

This line of code will save the DataFrame `df` to a CSV file named `filename.csv` in the current directory. The `index=False` parameter is used to prevent pandas from writing row numbers (indices) into the CSV file.

For example, if you have fetched stock data using the `get_stock` function and want to save it to a CSV file, you could modify the function call as follows:

```python

df = get_stock("nextFiscalQ")
df.to_csv('nextFiscalQ_data.csv', index=False)
```

Repeat this pattern for any data you retrieve using the other functions (`get_log`, `get_recommendation`, etc.) to persist that data to CSV files. This enables easy access to and sharing of the scraped data.


## Legal Disclaimer
This tool is intended for personal and educational purposes only. Please ensure you comply with Nasdaq’s terms of service regarding data scraping. Use this tool responsibly and ethically.

## Contributing
Contributions are welcome! Please feel free to submit pull requests, improve the documentation, or suggest new features.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Contact
For any queries, you can reach out to Gzzawiiz@gmail.com or m.ayuob@student.uw.edu.pl .

---
