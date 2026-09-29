# Weather & Travel Explorer

A responsive weather exploration application that lets users search cities and view current and forecast weather information.

A front-end project by **Kev Channoeurn**, a Computer Science student and Front-End Developer. It is also shown inside his portfolio: [kev-channoeurn-portfolio](https://github.com/sokhin-devops/kev-channoeurn-portfolio).

Design style: **Ambient + Glass**

## Features

- Search cities with the Open-Meteo geocoding API
- Current temperature and weather condition
- Humidity, wind speed, "feels like" temperature and chance of rain
- 5-day forecast with temperature range bars
- Favorite cities and the last viewed city, saved in LocalStorage
- Loading, error (with retry) and empty states
- A short travel note based on the conditions
- Background that changes subtly with the weather (clear, cloudy, rain, storm, snow, fog)
- Responsive layout with Dark, Light and System themes

## Tech Stack

- React 19 (useEffect and a custom useForecast hook)
- JavaScript (fetch, async/await, AbortController)
- CSS (glass panels, container queries)
- REST API: Open-Meteo
- [Vite](https://vite.dev)
- [Lucide React](https://lucide.dev) icons

## Getting Started

Requirements: [Node.js](https://nodejs.org) 20.19+ or 22.12+.

```bash
npm install
npm run dev
```

Then open the local URL printed in the terminal (usually <http://localhost:5173>).

## Build

```bash
npm run build     # production files go to dist/
npm run preview   # preview the production build locally
npm run lint      # check the code with ESLint
```

## Environment Variables

No environment variables are required. `.env.example` is included in case you later switch to a weather provider that needs an API key. Copy it to `.env` and never commit real keys.

## Notes

- Weather data comes from [Open-Meteo](https://open-meteo.com), which is free for non-commercial use and does **not** need an API key.
- An internet connection is required.
- Weather data by Open-Meteo.com is licensed under CC BY 4.0, so the app shows an attribution link.

## Project Structure

```
src/
├── main.jsx                  # Entry: theme provider and global styles
├── App.jsx                   # Page shell: top bar, theme switcher, footer
├── features/weather-explorer/# The app itself (components, logic and CSS)
├── components/ThemeSwitcher.jsx
├── context/ThemeContext.jsx  # Dark / Light / System theme
├── hooks/                    # useLocalStorage, useTheme
├── styles/                   # Design tokens, base styles, page shell
└── utils/
```
