
# 🚗 DDPAI GPX into VIRB Edit Slicer & Telemetry Studio

A sleek, client-side web application designed to parse, inspect, slice, and export raw **DDPAI dashcam GPS log files** and standard `.gpx` tracks into Garmin VIRB Edit-compatible GPX files with 12-hour AM/PM precision.

---

## 💡 Why This Tool Was Created

When recording drives with a DDPAI dashcam, the exported GPS data files (often containing raw NMEA sentences such as `$GPRMC` and `$GPGGA`) or standard `.gpx` tracks are frequently far too long for your edited video clips. Trimming these files manually inside **Garmin VIRB Edit** can be tedious and prone to synchronization errors.

This tool solves that exact problem by allowing you to:
* **Ingest DDPAI Dashcam Logs:** Directly upload raw dashcam GPS dumps or standard GPX files without requiring external conversion tools.
* **Precise 12-Hour AM/PM Slicing:** Select exact time ranges (e.g., extracting a specific 60-second clip at `07:47:48 PM`) using intuitive 12-hour AM/PM pickers.
* **Timezone Synchronization:** Seamlessly convert between local time zones (such as IST UTC+5:30) and UTC timestamps required by Garmin VIRB Edit.
* **Garmin Telemetry Extensions:** Automatically format outputs into valid GPX 1.1 with `<gpxtpx:TrackPointExtension>` tags (`<gpxtpx:speed>` and `<gpxtpx:course>`) so speed gauges, altitude profiles, and route maps sync perfectly with your video.
* **100% Private & Client-Side:** Runs entirely in your browser with zero server uploads.

---

## ✨ Key Features

1. **Dual Format Ingestion:** Automatically parses standard XML `.gpx` files as well as raw DDPAI NMEA sentence dumps (`$GPRMC` & `$GPGGA`).
2. **12-Hour AM/PM Pickers:** Split controls for Date, Hours (01–12), Minutes (00–59), Seconds (00–59), and an interactive AM/PM toggle.
3. **Interactive Map Preview:** Visualize your full track and your selected sliced route on an interactive Leaflet dark-theme map.
4. **Live Telemetry Metrics:** Instantly inspect Distance, Sliced Duration, Max Speed, and Average Speed.
5. **Robust Error Validation:** Alerts you instantly if the selected time window falls outside the recorded GPS file boundaries.

---

## 🚀 How to Use

1. **Open the Dashboard:** Open `index.html` in any modern web browser.
2. **Upload GPS/DDPAI File:** Drag and drop or click to upload your DDPAI dashcam log or `.gpx` file. The app will automatically detect the recording's start and end boundaries.
3. **Select Time Window:** Choose your desired **Start Time** and **End Time** using the 12-hour AM/PM controls. Use quick extend buttons (`+30s`, `+60s`, `+5m`) for rapid adjustments.
4. **Verify Route:** Check the interactive map and telemetry logs to ensure the correct track segment is highlighted.
5. **Export & Download:** Click **"Export VIRB Edit GPX (12h Synced)"** and import the resulting `.gpx` file directly into Garmin VIRB Edit!

---

## 🛠️ Running Locally

1. Clone or download this repository.
2. Save the application file as `index.html` in your working folder.
3. Double-click **`index.html`** to open it instantly in your browser.
   *(Or spin up a local server via Python: `python -m http.server 8000`)*

---

## 👤 Author

* **Suman Kumar**  
  GitHub: [@sumancsnit](https://github.com/sumancsnit)

---
*(c) 2026 Suman Kumar. Released under the MIT License.*
