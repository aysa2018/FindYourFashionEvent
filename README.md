# Project Title: Vogue Fashion Scraper and Ticketmaster Events Matcher

## Project Description

This project scrapes fashion-related headlines from Vogue’s website and retrieves fashion-related events using the Ticketmaster API. The goal is to find connections between Vogue's fashion articles and upcoming fashion events across the U.S. and provide meaningful insights through visualizations.

The data pipeline includes:
1. Scraping Vogue’s fashion page for headlines, links, and images using Selenium and BeautifulSoup.
2. Fetching fashion-related events from Ticketmaster using their public API.
3. Matching Vogue’s headlines with Ticketmaster events based on common keywords.
4. Visualizing the results, including the number of fashion events per city, the distribution of events over time, and matched fashion articles with events by city.

## Project Structure


### Key Libraries Used:
- `sys`: For system path management.
- `time`: To control the wait time for web scraping.
- `requests`: For making HTTP requests to Ticketmaster's API.
- `pandas`: For data manipulation and storage.
- `matplotlib`: For generating visualizations.
- `selenium`: For web scraping with a headless browser.
- `BeautifulSoup`: For HTML parsing and extracting data from Vogue's webpage.

### Project Flow:
1. **Web Scraping Vogue Fashion Page**:
   - Uses Selenium WebDriver to scrape Vogue's fashion page, extracting headlines, links, and images of articles.
   - The data is stored in a Pandas DataFrame and saved to `vogue_data.csv`.

2. **Fetching Events from Ticketmaster API**:
   - Makes a GET request to Ticketmaster's API, retrieving fashion-related events.
   - The retrieved data is parsed into a Pandas DataFrame and saved to `ticketmaster_events.csv`.

3. **Matching Vogue Headlines with Events**:
   - A matching function compares keywords from Vogue's headlines to Ticketmaster's event names.
   - Matched data is stored in a Pandas DataFrame and saved to `matched_fashion_events.csv`.

4. **Visualization**:
   - Three visualizations are provided:
     1. Bar chart of the number of fashion events per city.
     2. Line chart showing the distribution of fashion events over time.
     3. Bar chart of matched Vogue headlines with Ticketmaster events by city.

## Installation and Setup

1. **Clone the repository** or download the project files.
2. **Install the required libraries** by running:
   ```bash
   pip install selenium requests pandas beautifulsoup4 matplotlib clickc
   ```
3. **Download ChromeDriver** to enable Selenium's headless browser. Place the executable in the correct path based on your system configuration.

4. **Run the script** using Python:
   ```bash
   python main.py
   ```

5. **API Key Setup**: Ensure you have your Ticketmaster API key in .env file:
   ```python
   API_KEY = "Your_Ticketmaster_API_Key"
   ```

## License
This project is open-source under the MIT License.




