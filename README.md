# NoiseWatch — Noise Pollution Assessment Dashboard

A static, browser-based project for recording and analysing manually collected noise levels around a college, hospital, and traffic junction.

## Features
- Dashboard metrics: average, highest reading, number of records, and readings above the configured comparison limit
- Trend chart and average-by-location chart
- Manual reading form with date/time, site, dB(A), zone, day/night period, duration, meter/method, and notes
- Filters and reading register
- CSV import and export (import accepts NoiseWatch CSV exports or a CSV with DateTime, Location, dB(A), plus optional site/zone/period/notes columns)
- Report generation with Print / Save as PDF and Copy text
- Editable comparison values
- Browser-local storage; no server or account required
- Clearly labelled simulated demo data (optional)

## Important measurement limitations
- The app does **not** measure sound automatically. Enter readings obtained using a suitable sound level meter.
- Demo records are simulated and must never be presented as actual field measurements.
- Phone/laptop microphone readings are approximate unless calibrated and validated; this app does not use a microphone.
- The default comparison values are commonly published Indian ambient noise standards (day/night dB(A) Leq): Industrial 75/70, Commercial 65/55, Residential 55/45, Silence 50/40. Verify current CPCB guidance, applicable rules/amendments, and local notifications. A location is not automatically a legally designated silence zone simply because it is near a hospital or college.
- A single spot reading or arithmetic average of spot readings is not necessarily equivalent to the required time-averaged LAeq. This educational dashboard is not a compliance certificate.

## Run locally
Open `index.html` in a modern browser. An internet connection is needed to load Chart.js from jsDelivr; the form, records, and CSV export are otherwise local browser features. To run offline, download Chart.js and change the script reference to a local file.

## Deploy to GitHub Pages
1. Sign in to GitHub and create a **public** repository named `noise-pollution-assessment`.
2. Upload/replace `index.html` and `README.md` to the repository root (or use **Add file → Upload files**).
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose branch `main` and folder `/(root)`, then click **Save**.
6. Wait a few minutes and open the URL shown in the Pages section. It will normally be `https://YOUR-USERNAME.github.io/noise-pollution-assessment/`.
7. Test adding a reading, refreshing the page, exporting CSV, and printing a report.

## Data storage
Records are stored in the browser's localStorage on the current device and browser. They do not sync to GitHub, are not uploaded to a database, and may be lost if browser storage is cleared. Export CSV for backup. Do not enter sensitive personal information.
