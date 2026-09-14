# 🌤️ Zomato Weather App

<div align="center">

📊 **[View Project Presentation](https://docs.google.com/presentation/d/1uexgmMta6YWOAplxYoKMItEuej15qeqP/edit?usp=sharing&ouid=103542437763217709126&rtpof=true&sd=true)**

**Real-time weather data powered by Zomato Weather Union API** 🚀

[Live Demo](#) • [Features](#-features) • [Installation](#-installation) • [API](#-api-reference)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Installation](#-installation)
- [Usage](#-usage)
- [API Reference](#-api-reference)
- [Deployment](#-deployment)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌍 Overview

**Zomato Weather App** is a modern, responsive web application that provides real-time weather information across 577+ cities in India. Built with vanilla JavaScript and powered by Zomato's Weather Union API, it delivers accurate hyperlocal weather data from IoT sensors and rain gauge systems.

### Why This App?

- 🎯 **Hyperlocal Accuracy**: Get precise weather data from ground-level sensors
- 📡 **Real-time Updates**: Live data from AWS and rain gauge systems
- 🗺️ **Wide Coverage**: Access weather info from 577+ Indian localities
- 📱 **Mobile Friendly**: Fully responsive design works on all devices
- ⚡ **Fast & Lightweight**: No heavy frameworks, just pure performance

---

## ✨ Features

### Core Features
- 🌡️ **Real-time Temperature** - Live temperature readings in Celsius
- 💧 **Humidity Monitoring** - Track moisture levels in the air
- 💨 **Wind Data** - Get wind speed and direction information
- 🌧️ **Rain Metrics** - Monitor rain intensity and accumulation
- 🏭 **Air Quality Index** - Check PM 2.5 and PM 10 levels
- 📍 **Dual Search Modes**:
  - Coordinates (Latitude/Longitude)
  - Locality Code (e.g., ZWL001156)

### UI/UX Features
- 🎨 **Beautiful Animations** - Smooth, modern interface with animated elements
- 🕐 **Live Clock** - Real-time clock display
- 🔍 **Smart Search** - Browse and search through 577+ locations
- 📊 **Data Visualization** - Clean, organized weather information display
- 🌈 **Responsive Design** - Works seamlessly on desktop, tablet, and mobile

---

## 🛠️ Tech Stack

### Frontend
- **HTML5** - Semantic markup
- **CSS3** - Modern styling with animations
- **Vanilla JavaScript** - Pure JS, no frameworks needed
- **Google Fonts** - Poppins font family

### Backend
- **Node.js** - Runtime environment
- **HTTP/HTTPS modules** - Native Node.js modules for server and API calls
- **File System (fs)** - Serve static files

### API
- **Zomato Weather Union API** - Real-time weather data provider

### Deployment
- **Render** - Cloud platform for deployment
- **Git/GitHub** - Version control

---

## 📦 Installation

### Prerequisites
- Node.js (v14.0.0 or higher)
- npm (comes with Node.js)
- Git


## 🎮 Usage

### Method 1: Search by Coordinates

1. Select **📍 Coordinates (Lat/Long)** option
2. Enter latitude (e.g., `12.933756`)
3. Enter longitude (e.g., `77.625825`)
4. Click **🔍 Get Weather**

### Method 2: Search by Locality Code

1. Select **🏘️ Locality Code** option
2. Enter locality code (e.g., `ZWL001156`)
3. Click **🔍 Get Weather**

### Method 3: Browse Locations

1. Click **🗺️ Browse All Locations** button
2. Search for your city or locality
3. Click on any location to fetch weather data automatically

---

## 🔌 API Reference

### Base URL (Local)
```
http://localhost:3000
```

### Endpoints

#### 1. Get Weather by Coordinates
```http
GET /weather/coordinates?latitude={lat}&longitude={lon}
```

**Parameters:**
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `latitude` | float | Yes | Latitude coordinate |
| `longitude` | float | Yes | Longitude coordinate |

**Example:**
```bash
curl "http://localhost:3000/weather/coordinates?latitude=12.933756&longitude=77.625825"
```

**Response:**
```json
{
  "status": "success",
  "message": "Locality weather data",
  "device_type": 1,
  "locality_weather_data": {
    "temperature": 28.5,
    "humidity": 65,
    "wind_speed": 3.2,
    "wind_direction": 180,
    "rain_intensity": 0,
    "rain_accumulation": 0
  }
}
```

#### 2. Get Weather by Locality
```http
GET /weather/locality?locality_id={id}
```

**Parameters:**
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `locality_id` | string | Yes | Locality code (e.g., ZWL001156) |

**Example:**
```bash
curl "http://localhost:3000/weather/locality?locality_id=ZWL001156"
```

---

## 🚀 Deployment

### Deploy on Render

1. **Push your code to GitHub**
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

2. **Create a new Web Service on Render**
   - Go to [Render Dashboard](https://dashboard.render.com/)
   - Click **"New +"** → **"Web Service"**
   - Connect your GitHub repository

3. **Configure the service**
   - **Name**: `zomato-weather-app`
   - **Build Command**: Leave empty (or `npm install` if you add dependencies)
   - **Start Command**: `npm start`
   - **Environment Variables**:
     - `API_KEY` = `your_zomato_api_key`

4. **Deploy!**
   - Click **"Create Web Service"**
   - Wait for deployment to complete
   - Visit your live URL: `https://your-app.onrender.com`

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `PORT` | Server port (auto-assigned by Render) | No |
| `API_KEY` | Zomato Weather Union API Key | Recommended |

---

## 📸 Screenshots

### Desktop View
```
┌─────────────────────────────────────────────────────┐
│  🌦️ Weather Union          Current Time: 14:30:45  │
├─────────────────────────────────────────────────────┤
│                                                      │
│         🌍 Real-Time Weather Data                   │
│    Get accurate weather information powered by      │
│         Zomato Weather Union API                    │
│                                                      │
│    ○ 📍 Coordinates (Lat/Long)                      │
│    ○ 🏘️ Locality Code                              │
│                                                      │
│    🗺️ [Browse All Locations (577+ Cities)]         │
│                                                      │
│    [Latitude Input]    [Longitude Input]            │
│              [🔍 Get Weather]                       │
│                                                      │
│    ┌──────────────────────────────────────┐        │
│    │  🌤️ Weather Information              │        │
│    │  🌡️ Temperature: 28.5°C              │        │
│    │  💧 Humidity: 65%                     │        │
│    │  💨 Wind Speed: 3.2 m/s              │        │
│    └──────────────────────────────────────┘        │
└─────────────────────────────────────────────────────┘
```

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
```bash
git checkout -b feature/AmazingFeature
```
3. **Commit your changes**
```bash
git commit -m "Add some AmazingFeature"
```
4. **Push to the branch**
```bash
git push origin feature/AmazingFeature
```
5. **Open a Pull Request**

### Contribution Ideas
- 🌍 Add weather forecast (hourly/daily)
- 📊 Add charts and graphs for weather trends
- 🗺️ Integrate interactive maps
- 🌙 Add dark mode toggle
- 🔔 Add weather alerts and notifications
- 🌐 Add internationalization (i18n)
- 📱 Create a mobile app version

---

## 📝 License

This project is licensed under the **ISC License**.

---

## 👨‍💻 Author

**Vivek Sharma**

- GitHub: [@viveksharma2105](https://github.com/viveksharma2105)

---

## 🙏 Acknowledgments

- **Zomato Weather Union** - For providing the weather API
- **Google Fonts** - For the Poppins font family
- **Render** - For hosting services
- **Open Source Community** - For inspiration and support

---

## 📞 Support

If you have any questions or need help, feel free to:

- Open an [Issue](https://github.com/viveksharma2105/Zomato-weather/issues)
- Contact: [Your Email]

---

## 🌟 Show Your Support

Give a ⭐️ if this project helped you!

---

<div align="center">

**Made with ❤️ and ☕ by Vivek Sharma**

</div>
