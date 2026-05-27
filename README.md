# Weather Dashboard

A modern, responsive weather application built with **React** and **Vite** that provides real-time weather information for any city worldwide.

## Features

- **Real-time Weather Data**: Fetches current weather information using the OpenWeatherMap API
- **Search Functionality**: Search for weather by city name with instant results
- **Weather Metrics**: Displays:
  - Current temperature (in Celsius)
  - Weather condition with dynamic icons
  - Humidity percentage
  - Wind speed (in km/h)
  - Location name
- **Weather Icons**: Visual representation of weather conditions (clear, cloudy, rainy, snowy, etc.)
- **Default Location**: Loads weather for London on app startup
- **Error Handling**: User-friendly alerts for invalid city names or API errors

## Tech Stack

- **Frontend Framework**: React 19.2.6
- **Build Tool**: Vite 8.0.12
- **Styling**: CSS3
- **API**: OpenWeatherMap API
- **Development Tools**:
  - ESLint for code quality
  - Vite for fast development and production builds

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn package manager

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Weather_App
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory with your OpenWeatherMap API key:
   ```
   VITE_APP_ID=your_api_key_here
   ```
   Get your free API key from [OpenWeatherMap](https://openweathermap.org/api)

### Running the Application

**Development Mode:**
```bash
npm run dev
```
The app will start at `http://localhost:5173`

**Build for Production:**
```bash
npm run build
```

**Preview Production Build:**
```bash
npm run preview
```

**Lint Code:**
```bash
npm run lint
```

## Project Structure

```
Weather_App/
├── src/
│   ├── components/
│   │   ├── Weather.jsx          # Main weather component
│   │   └── Weather.css          # Weather component styles
│   ├── assets/                  # Weather icons and images
│   │   ├── clear.png
│   │   ├── cloud.png
│   │   ├── drizzle.png
│   │   ├── humidity.png
│   │   ├── rain.png
│   │   ├── search.png
│   │   ├── snow.png
│   │   └── wind.png
│   ├── App.jsx                  # Root component
│   ├── main.jsx                 # Application entry point
│   └── index.css                # Global styles
├── public/                      # Static files
├── index.html                   # HTML template
├── package.json                 # Project dependencies
├── vite.config.js              # Vite configuration
├── eslint.config.js            # ESLint configuration
└── README.md                    # Project documentation
```

## How It Works

1. **Weather Component** (`Weather.jsx`):
   - Maintains weather data state using `useState`
   - Uses `useRef` to capture city name input
   - Fetches weather data from OpenWeatherMap API
   - Maps weather icons based on condition codes
   - Displays temperature, location, humidity, and wind speed

2. **Search Functionality**:
   - Users enter a city name in the search bar
   - Clicking the search icon or pressing enter triggers the API call
   - Weather data is fetched and displayed dynamically

3. **Weather Icons**:
   - The app includes a mapping of OpenWeatherMap condition codes to custom icons
   - Icons update automatically based on current weather conditions

## Environment Variables

| Variable | Description |
|----------|-------------|
| `VITE_APP_ID` | Your OpenWeatherMap API key (required) |

## API Integration

This app uses the **OpenWeatherMap API**:
- Endpoint: `https://api.openweathermap.org/data/2.5/weather`
- Units: Metric (Celsius, m/s)
- Data Fetched:
  - Temperature
  - Weather condition and icon code
  - Humidity
  - Wind speed
  - Location name

## Responsive Design

The app is fully responsive and works seamlessly on:
- Desktop browsers
- Tablets
- Mobile devices

## Error Handling

- **Invalid City**: Shows alert if the city is not found
- **Empty Search**: Prompts user to enter a city name
- **API Errors**: Gracefully handles API failures with console logging

## Future Enhancements

- [ ] Add 5-day weather forecast
- [ ] Implement location-based weather using geolocation
- [ ] Add temperature unit toggle (Celsius/Fahrenheit)
- [ ] Store search history
- [ ] Add weather alerts
- [ ] Dark mode support
- [ ] Multiple city comparison

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

Alok Kumar Janghel


