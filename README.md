# Myntra Web Scraping & GPT Integration
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
* myntra_web_scraper.py (# Web scraping script for Myntra)
* api.py (# Main Flask API)
* electronics_db (# Script to set up the SQLite database)
* gpt_integration (# GPT query script)
* README.md                 

# Usage
Querying the API
After running the Flask server, you can make POST requests to the /query endpoint to query the products using natural language.

* Example Request Using Postman
* Method: POST
* URL: http://127.0.0.1:5000/query
* Body (in JSON format): {"prompt": "What are the best cameras under ₹5000?"}

# API Endpoints
POST /query
* Description: Sends a natural language query to the API, which responds based on product data and the GPT model.
Request Body:
* prompt: The user’s query.
Response: Returns a GPT-generated response based on the scraped product data.
GET /scrape
* Description: Scrapes new product data from Myntra and updates the local database.
* Note: This endpoint is optional and can be added to trigger the scraping from the API instead of running it manually.

# Error Handling
Common errors like rate limits or insufficient data in the database are handled gracefully. 
If you encounter any issues, make sure to check the server logs for more details.
