# API Citation Finder

This Python program fetches data from a paginated API and identifies the sources from which each response is formed. It returns a list of citations for each response-sources pair.

## Features

- Fetch data from a paginated GET API endpoint.
- Identify whether the response for each response-sources pair came from any of the sources.
- List down the sources from which the response was formed.
- Provide a user-friendly web interface to display the results.
- Provide an API endpoint to get citations in JSON format.

## Technologies Used

- Python
- Flask
- Requests
- HTML/CSS (Bootstrap)

## Setup

### Prerequisites

- Python 3.x
- pip (Python package installer)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/api-citation-finder.git
   cd api-citation-finder
Create and activate a virtual environment (optional but recommended):


python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install the required dependencies:


pip install -r requirements.txt
Running the Application
Start the Flask application:


python app.py
Access the application:
Open your web browser and go to http://127.0.0.1:5000.

Endpoints
/: Displays the citations in a user-friendly web interface.
/api/citations: Returns the citations in JSON format.



Project Structure

.
├── app.py                 # Main application file
├── requirements.txt       # List of dependencies
├── README.md              # Project documentation
└── templates
    └── index.html         # HTML template for the web interface
How It Works
Fetch Data: The application fetches data from the API endpoint using the fetch_data_from_api function. This function handles pagination to ensure all data is retrieved.
Find Citations: The find_citations function processes each response-sources pair to determine if the response text contains any context from the sources. If a match is found, the source is included in the citations list.
Display Results: The Flask application provides a web interface to display the citations and an API endpoint to return the citations in JSON format.
Code Explanation
app.py:

fetch_data_from_api(url): Fetches data from the API and handles pagination.
find_citations(data): Identifies citations by checking if the response contains context from the sources.
Flask routes:
/: Renders the web interface.
/api/citations: Returns citations as JSON.
templates/index.html: HTML template using Bootstrap to display the citations in a user-friendly manner.

Edge Cases
Handles empty responses from the API.
Returns an empty array if no sources match the response text.
Gracefully handles API errors.
Future Improvements
Add error handling for network issues.
Improve the matching algorithm to handle partial matches or synonyms.
Add pagination support to the web interface.
License
This project is licensed under the MIT License.

Author
Vipul Jain
GitHub: Vipuljain-08