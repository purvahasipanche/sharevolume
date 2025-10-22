# Company Shares Outstanding Dashboard

This is a single-file, responsive HTML application designed to fetch and display common stock shares outstanding data for a specified company from the SEC EDGAR API.

## Features

*   **Dynamic Data Fetching**: Retrieves `EntityCommonStockSharesOutstanding` data from the SEC EDGAR API.
*   **Filtering**: Processes data to include only entries with a fiscal year (`fy`) greater than 2020 and a valid numeric value (`val`).
*   **Max/Min Display**: Clearly shows the highest and lowest shares outstanding values along with their respective fiscal years.
*   **Company Name Display**: Dynamically updates the page title, main heading, and entity name based on the fetched data.
*   **Responsive Design**: Uses Tailwind CSS for a clean and responsive user interface.
*   **Dynamic CIK Loading**: Supports loading data for any 10-digit CIK by appending it as a URL parameter (e.g., `index.html?CIK=0001018724`).

## How to Run

1.  **Save the file**: Save the `index.html` content provided as `index.html` in a local directory.
2.  **Open in Browser**: Open `index.html` in any modern web browser.

### Viewing Data for Specific Companies

By default, the application loads data for **CenterPoint Energy (CIK: 0001130310)**.

To view data for a different company, append a `?CIK=` parameter to the URL in your browser's address bar. For example:

*   For **Apple Inc. (CIK: 0001018724)**: `index.html?CIK=0001018724`
*   For **Microsoft Corp (CIK: 0000789019)**: `index.html?CIK=0000789019`

## Data Source

All financial data is sourced from the [SEC EDGAR API](https://www.sec.gov/edgar/sec-api-documentation).

**Note on User-Agent**: The SEC requests a descriptive User-Agent for API access. In this client-side application, the User-Agent is managed by the browser. For server-side applications or proxy interactions, a custom User-Agent would be explicitly set (e.g., `'YourCompanyName - Data Fetcher / your_email@example.com'`).

## Included Files

*   `index.html`: The main application file containing HTML, CSS (Tailwind CDN), and JavaScript.
*   `README.md`: This file, providing information about the project.
*   `LICENSE`: The MIT License for this project.
*   `uid.txt`: An attachment provided with this project (committed as-is).