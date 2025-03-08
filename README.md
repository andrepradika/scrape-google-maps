# Google Maps Business Scraper

## Overview
This script scrapes business details from Google Maps using Playwright and stores the extracted data in Excel and CSV formats.

## Features
- Automates Google Maps search for businesses.
- Extracts details such as name, address, website, phone number, reviews average, and coordinates.
- Saves the data in both Excel and CSV formats.
- Supports batch search via `input.txt`.

## Requirements
- Python 3.7+
- Playwright
- Pandas

## Installation
1. Clone the repository or download the script.
2. Install dependencies:
   ```bash
   pip install playwright pandas
   playwright install
   ```

## Usage
### Run the script with a single search term:
```bash
python script.py -s "Restaurants in New York" -t 50
```

### Run the script with multiple search terms from `input.txt`:
1. Create a file named `input.txt` and list search queries (one per line).
2. Run the script without arguments:
   ```bash
   python script.py
   ```

### Arguments
- `-s`, `--search`: Search query (e.g., "Hotels in Los Angeles").
- `-t`, `--total`: Maximum number of results to scrape.

## Output
The extracted data is saved in the `output` directory as:
- `google_maps_data_<search_query>.xlsx`
- `google_maps_data_<search_query>.csv`

## Error Handling
- If `-s` is not provided and `input.txt` is empty, an error message will be displayed.
- If scraping fails for a business, the script continues to the next one.

## License
MIT License

## Author
andrepradika
