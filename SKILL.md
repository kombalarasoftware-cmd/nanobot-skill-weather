# Weather Information

> Get current weather, forecasts, and severe weather alerts for any location worldwide.

## Metadata
- **name**: weather-info
- **version**: 1.0.0
- **author**: kombalarasoftware-cmd
- **category**: utility
- **tools**: get_current_weather, get_weather_forecast, get_weather_alerts

## Prompt Extension

You have access to weather information tools. When the user asks about weather:

1. Use `get_current_weather(location)` for current conditions (temperature, humidity, wind, description)
2. Use `get_weather_forecast(location, days)` for multi-day forecasts (default 3 days)
3. Use `get_weather_alerts(location)` to check for severe weather warnings

### Response Format
- Always include temperature in both Celsius and Fahrenheit
- Mention wind speed the unit the user prefers
- For forecasts, provide a brief daily summary
- Proactively mention severe weather alerts if any exist

## Tools

### get_current_weather
- **description**: Get current weather conditions for a location
- **parameters**:
  - `location` (string, required): City name or coordinates
- **returns**: Temperature, humidity, wind speed, weather description

### get_weather_forecast
- **description**: Get multi-day weather forecast
- **parameters**:
  - `location` (string, required): City name or coordinates
  - `days` (integer, optional, default=3): Number of forecast days (1-7)
- **returns**: Daily forecast with high/low temps, precipitation chance

### get_weather_alerts
- **description**: Check for severe weather alerts
- **parameters**:
  - `location` (string, required): City name or coordinates
- **returns**: Active weather warnings and advisories
