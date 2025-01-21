# Weather Dashboard

## Overview

The Weather Dashboard is a web application that provides current weather information and a 7-day forecast for any city. It uses the OpenWeatherMap API to fetch weather data and Google Places Autocomplete for city input. The application is built using Flask for the backend and HTML, CSS, and JavaScript for the frontend.

## Features

- Display current weather information including temperature, humidity, and wind speed.
- Show a 7-day weather forecast.
- Dynamic background color.
- Google Places Autocomplete for easy city input.
- Caching to reduce API calls and improve performance.

## Technologies Used

- Flask
- OpenWeatherMap API
- Google Places Autocomplete
- HTML, CSS, JavaScript
- Flask-Caching

## Setup and Installation

### Prerequisites

- Python 3.x
- Flask
- Requests library
- Flask-Caching library

### Installation Steps

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/weather-dashboard.git
    cd weather-dashboard
    ```

2. Install the required Python packages:
    ```bash
    pip install flask requests flask-caching
    ```

3. Set up your OpenWeatherMap API key:
    - Replace the `API_KEY` variable in `weather.py` with your OpenWeatherMap API key.

4. Set up your Google Places API key:
    - Replace the API key in the script tag in `index.html` with your Google Places API key.

### Running the Application

1. Start the Flask server:
    ```bash
    python weather.py
    ```

2. Open your web browser and go to `http://127.0.0.1:5000`.

## Project Structure

```
weather-dashboard/
│
├── static/
│   ├── styles.css
│   ├── scripts.js
│   └── google-maps.js
│
├── templates/
│   └── index.html
│
├── weather.py
└── README.md
```

### File Descriptions

- `weather.py`: The main Flask application file that handles routes and API calls.
- `static/styles.css`: The CSS file for styling the web application.
- `static/scripts.js`: The JavaScript file for handling frontend logic.
- `static/google-maps.js`: The JavaScript file for handling Google Places Autocomplete.
- `templates/index.html`: The HTML file for the main page of the web application.
- `README.md`: This README file.

## API Endpoints

### `/`

- **Description**: Renders the main page.
- **Method**: GET

### `/current_weather`

- **Description**: Fetches current weather data for a specified city.
- **Method**: GET
- **Parameters**:
    - `city` (required): The name of the city.

### `/forecast`

- **Description**: Fetches a 7-day weather forecast for a specified city.
- **Method**: GET
- **Parameters**:
    - `city` (required): The name of the city.

### `/background_color`

- **Description**: Returns the background color as a JSON response.
- **Method**: GET

## Usage

1. Enter the name of a city in the input field and click the "Search" button.
2. The current weather information and 7-day forecast for the specified city will be displayed.
3. The background color of the page will be set dynamically.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [OpenWeatherMap](https://openweathermap.org/) for providing the weather data API.
- [Google Places API](https://developers.google.com/places/web-service/overview) for the city autocomplete feature.
- [Flask](https://flask.palletsprojects.com/) for the web framework.
