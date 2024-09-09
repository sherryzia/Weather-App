# SwiftUI Weather App 🌦

A simple SwiftUI weather app that allows users to search for the current weather in any city by name. The app uses the *OpenWeather Geocoding API* to convert city names into latitude and longitude, and then fetches the weather forecast using the *Open-Meteo API*. The app also displays weather-relevant images based on the temperature or weather conditions.

## Features 🚀
- *Fetch weather by city name*: Enter any city name and get the current weather data.
- *No API key required for weather data*: Open-Meteo provides free weather data without API limits.
- *Dynamic weather images*: Displays different images based on temperature or weather conditions (e.g., sunny, cloudy, rainy, snowy).
  
## Technologies Used 🛠
- *SwiftUI* for the UI.
- *OpenWeather Geocoding API* to convert city names into coordinates.
- *Open-Meteo API* to fetch weather data using latitude and longitude.
- *MVVM Architecture* to manage data flow between UI and network calls.

## Requirements 📝
- Xcode 12 or higher
- Swift 5.0+
- An *OpenWeather API Key* for geocoding (free to obtain from OpenWeather).

## How It Works 🔍

### Step 1: Geocoding City Names
The app uses the *OpenWeather Geocoding API* to convert city names into geographic coordinates (latitude and longitude). This allows the app to work with city names rather than just coordinates.

### Step 2: Fetching Weather Data
The app uses the latitude and longitude obtained from geocoding to fetch the weather data from *Open-Meteo*, a free weather forecast service that does not require an API key.

### Step 3: Displaying Weather Information
The app displays the current temperature, and based on the temperature or weather condition (e.g., sunny, rainy), it shows the corresponding weather image.

## File Structure 📂

```
WeatherApp/
│
├── WeatherApp.xcodeproj             // Xcode project file
│
├── WeatherApp/
│   ├── WeatherAppApp.swift          // Main entry point for the SwiftUI app
│   ├── ContentView.swift            // Main SwiftUI view (UI and interaction)
│   ├── ViewModels/
│   │   └── WeatherViewModel.swift   // ViewModel to handle geocoding and weather fetching
│   ├── Models/
│   │   ├── WeatherResponse.swift    // Model for Open-Meteo weather data
│   │   └── GeocodingResponse.swift  // Model for OpenWeather geocoding data
│   └── Services/
│       └── WeatherService.swift     // Service to fetch weather and geocoding data
│
└── Assets.xcassets/                 // Folder for weather condition images (sunny, rainy, etc.)
```



## Setup and Installation 💻

1. Clone the repository or download the project to your local machine.
2. Open the project in *Xcode*.
3. In WeatherService.swift, replace the placeholder with your *OpenWeather API Key*:
    swift
    private let geoApiKey = "YOUR_API_KEY"  // Replace with your OpenWeather API key
    
4. Add weather condition images (e.g., *sunny.png, **rainy.png, **cloudy.png, **snowy.png) into the **Assets.xcassets* folder.
5. Run the project in the simulator or on a real device.

## API References 🌐

- *OpenWeather Geocoding API*: https://openweathermap.org/api/geocoding-api
- *Open-Meteo API*: https://open-meteo.com/en

## How to Customize 🛠

1. *Add more weather conditions*:
   - You can extend the logic in WeatherViewModel.swift to handle more weather conditions (like storms, fog, etc.) based on the description field in the weather API response.
   
2. *Add hourly/daily forecasts*:
   - Modify the Open-Meteo API request to fetch hourly or daily weather forecasts and display them in a scrollable list in *ContentView.swift*.

3. *Enhance the UI*:
   - You can add animations to weather icons, implement dark mode support, or customize the app theme further.

## Conclusion 🎉

This project provides a simple but effective demonstration of fetching and displaying weather data using SwiftUI and multiple weather APIs. You can easily expand upon this foundation to create a more feature-rich weather app with additional data, improved UI/UX, and animations.
