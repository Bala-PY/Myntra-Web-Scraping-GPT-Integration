# myntra_webscraper
Objective: Making a web scraper API with python and integrating it to GPT to answer some intersting queries on the scraped data.

#Features
Scrapes electronics product data from Myntra, including product description, price, rating, and reviews.
Stores the scraped data in a SQLite database.
Exposes an API where users can query the product data using natural language, powered by GPT models.

# Pre-requisites
Before you begin, ensure you have the following installed:
Python 3.8 or higher
OpenAI API key (Sign up here)
Flask

# Installation
1. Clone the Repository
2. Set up the Virtual Environment
3. Install Dependencies
4. Set Up the OpenAI API Key
5. Run the Scraper
6. Start the Flask Server

# Project Structure
* app.py                    # Main Flask API
├── scrape_myntra.py           # Web scraping script for Myntra
├── database_setup.py          # Script to set up the SQLite database
├── requirements.txt           # List of dependencies
├── README.md                  # Project documentation
├── .env                       # API key configuration file
└── myntra_data.db             # SQLite database (after scraping)

# Usage
Querying the API
After running the Flask server, you can make POST requests to the /query endpoint to query the products using natural language.

Example Request Using Postman
Method: POST
URL: http://127.0.0.1:5000/query
Body (in JSON format): {"prompt": "What are the best cameras under ₹5000?"}
