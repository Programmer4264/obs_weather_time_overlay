# Live Weather and Time Overlay for OBS

A lightweight weather + clock browser overlay for OBS Studio.

> Original project by **[@ngholson](https://github.com/ngholson/obs_weather_time_overlay)**.  
> This repository is an updated fork that keeps the original concept while improving clarity and compatibility.

## Preview

<p align="center">
  <img src="./preview.png" alt="Weather and time overlay preview">
</p>

## Download

You can download the original project archive here:  
[Download original ZIP](https://github.com/ngholson/obs_weather_time_overlay/archive/refs/heads/main.zip)

---

## What’s Updated in This Fork

This fork modernizes and maintains the overlay while preserving the original behavior:

- Cleaned up and corrected README instructions
- Clarified setup flow for OBS browser sources
- Fixed terminology and typo issues (for example: *separator*, *display*, etc.)
- Kept configuration options and usage style the same for easy migration

---

## Requirements

You need a free API key from OpenWeatherMap:  
[Sign up here](https://home.openweathermap.org/users/sign_up)

> When signing up, use the **free API key** under the standard weather offerings.  
> You do **not** need One Call 3.0 paid access for this project’s basic usage.

**Important:** New API keys may take **5–10 minutes** to become active.

---

## Setup Instructions

After downloading and extracting the project, open `weatherWidget.html` in a text editor and configure the variables below.

### Required Settings

- `yourApiKey` — Your OpenWeatherMap API key
- `yourCity` — Your city/location  
  Examples: `London, UK`, `Las Vegas, NV, US`, `Kyiv`
- `yourUnits` — Temperature units  
  - `imperial` (Fahrenheit)  
  - `metric` (Celsius)  
  - `standard` (Kelvin)

### Optional Settings

- `weatherDisplay` — `full`, `weather`, `simple`, `temp`, `time`
- `weatherIcons` — Show weather icons (`1` = on, `0` = off)
- `iconPack` — Icon set number (1–3)
- `iconHeight` — Icon height in pixels  
  Tip: `textSize + 2` often looks best (example: textSize 20 → iconHeight 22)
- `textSize` — Text size
- `textColor` — Text color
- `weatherBackground` — Background color for weather box  
  (If `dynamicBackground` is enabled, this mainly applies during daytime.)
- `dynamicBackground` — Day/night background switching (`1` = on, `0` = off)
- `clockSeparator` — Separator between temperature and time in `full` mode (examples: `-`, `/`, `.`, `*`, or spaces)
- `time24hour` — 24-hour clock format toggle
- `weatherBorder` — Border size around weather display
- `autoCheckUpdates` — Check for updates on initial load

---

## Add to OBS Studio

1. Save your changes in `weatherWidget.html`.
2. Open OBS Studio.
3. Add a new **Browser Source** to your scene.
4. Set the Browser Source URL to the local file path of your `weatherWidget.html`.
5. Set source dimensions to `1920 x 1080` (or your preferred canvas size).
6. Position and scale as needed.

---

## Notes

- Multi-language support is included (uses browser/OBS locale).
- If weather does not appear immediately, verify:
  - API key is active
  - City format is valid
  - Internet access is available for the Browser Source

---

## Credits

- **Original Creator:** [ngholson](https://github.com/ngholson/obs_weather_time_overlay)
- **Maintained Fork:** [Programmer4264](https://github.com/Programmer4264/obs_weather_time_overlay)
