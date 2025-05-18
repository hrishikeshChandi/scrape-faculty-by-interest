# Scrape Faculty By Interest

## Overview

This project creates a web application that helps users find faculty members at MSRIT (Ramaiah Institute of Technology) based on their research interests. It uses web scraping and MongoDB to store and display faculty expertise, making it easy for users to search by department and research area.

## Features

- **Department Search:** Enter a department to see all research areas within it.
- **Area of Interest Search:** Select an interest area to view faculty specializing in that field..
- **Web Scraping:** Data is gathered from MSRIT's official website using Selenium.
- **Database Caching:** Scarped data is stored in MongoDB for faster future searches, minimizing redundant scraping.
- **User-Friendly Interface:** Simple, styled HTML frontend accessible via web browsers.
- **Automatic Data Refresh:** Ensures data remains current by updating cached information as needed.

## How It Works

1. **User Input:** Enter a department name.
2. **Areas Listing:** Displays available research areas for the chosen department.
3. **Faculty Listing:** Selecting an area shows faculty members in that field.
4. **Data Handling:** Initially loads data from MongoDB, if it is unavailable, scrapes and stores it.

## Technologies Used

- **Python:** Flask for web development, Selenium for web scraping.
- **MongoDB:** Storage managed through PyMongo.
- **HTML/CSS/JavaScript**: Frontend uses Jinja2 for dynamic content.

## Setup and Usage

1. **Install Dependencies:**
   - Install dependencies like `Flask`, `pymongo`, and `Selenium`.
   - Download and configure ChromeDriver for Selenium.
2. **MongoDB:** Ensure a local MongoDB server is running.
3. **Configuration:**
   - Set the path to your `chromedriver.exe` in `main.py`.
   - The MongoDB connection is set to default localhost.
4. **Running the Application:**
   ```bash
   python main.py
   ```
5. **Using the App:**
   - Open `http://localhost:5000` in a web browser.
   - Enter a department and follow on-screen instructions to find faculty by interest.

## Project Structure

- `main.py` – Flask server, scraping logic, and data handling.
- `templates/index.html` – Main HTML template for the web interface.
- `README.md` – Project documentation.

## Notes

- The scraping targets the official MSRIT faculty pages. The structure of these pages may change, requiring updates to the scraping logic.
- The application is intended for academic or demonstration use only.

## License

This project is provided under the MIT License.
