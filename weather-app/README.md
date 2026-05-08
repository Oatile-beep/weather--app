# Weather App

A modern, responsive weather application that displays real-time weather data using the OpenWeatherMap API.

## Features

- **Real-time Weather Data**: Current temperature, humidity, wind speed, pressure, visibility, and cloudiness
- **5-Day Forecast**: Daily weather predictions
- **Location Search**: Search by city name
- **Geolocation**: Get weather for your current location
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Error Handling**: User-friendly error messages for network issues and invalid inputs
- **Loading States**: Visual feedback during data fetching
- **Weather Icons**: Visual weather representation from OpenWeatherMap

## Getting Started

### Prerequisites

1. Get a free API key from [OpenWeatherMap](https://openweathermap.org/api)
2. Sign up and verify your email to receive an API key

### Setup

**The API key is already configured** with the provided key. If you want to use your own key:

1. Open `index.html` in a text editor
2. Find line 74: `const API_KEY = '7684fd5ef96d77c2651a2a11db2aa34e';`
3. Replace the value with your own OpenWeatherMap API key
4. Save the file

### Running Locally

#### Option 1: Direct File
Simply open `index.html` in your web browser.

#### Option 2: Local Server (recommended)
```bash
# Using Node.js
npx serve .

# Or using Python
python -m http.server 8000
```
Then visit `http://localhost:3000` (or `http://localhost:8000`)

## Deployment

The app is a single static HTML file with no build process required.

### Deploy to Netlify / Vercel / GitHub Pages

1. Push the project to a GitHub repository
2. Connect your repository to any static hosting service
3. Deploy - that's it!

#### GitHub Pages
```bash
# Install gh-pages
npm install --save-dev gh-pages

# Add to package.json scripts:
# "deploy": "gh-pages -d ."

# Deploy
npm run deploy
```

#### Netlify
- Drag and drop the `index.html` file to Netlify's dashboard
- Or connect your Git repository for automatic deployments

#### Vercel
```bash
npx vercel
```

### Custom Domain
All static hosting platforms support custom domain mapping. Configure your domain in the platform's dashboard.

## Technical Details

### Architecture
- **Single File Application**: All HTML, CSS, and JavaScript in one file for easy deployment
- **Vanilla JavaScript**: No frameworks or dependencies
- **Async/Await**: Modern JavaScript for API calls
- **Responsive CSS**: Mobile-first approach with media queries

### API Endpoints Used
- `weather` - Current weather data
- `forecast` - 5-day forecast (3-hour intervals, processed to daily)

### Error Handling
- Network failures
- Invalid API key
- City not found
- Geolocation permissions denied
- Location unavailable/timeout

### Browser Support
- Modern browsers (Chrome, Firefox, Safari, Edge)
- ES6+ JavaScript features
- CSS Grid and Flexbox

## File Structure

```
weather-app/
├── index.html          # Single-file application
├── package.json        # Project metadata and deployment scripts
└── README.md          # This file
```

## Customization

### Styling
Edit the CSS variables in the `<style>` section:
```css
:root {
    --primary-color: #4a90e2;
    --secondary-color: #7b68ee;
    --background-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    /* ... */
}
```

### Units
Change `units=metric` to `units=imperial` in the API calls for Fahrenheit.

## License

MIT
