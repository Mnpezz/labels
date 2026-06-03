# 🏷️ JuiceSee — Expiration Label Maker

A lightweight, fully client-side web application designed to automatically calculate expiration dates, overlay them onto juice label templates, and print them directly to circular thermal label printers (like Munbyn or Rollo) or batch-download them.

## 🚀 Live Demo
[**Open JuiceSee Label Editor**](https://mnpezz.github.io/labels/)

---

## ✨ Features

- **Automatic Expiration Calculation**: Set standard offsets (e.g., `4 days` after today) or override with custom expiration texts on a per-label basis.
- **Canvas-based Date Overlay**: Dynamically adjusts position coordinates ($X$ & $Y$), font size, color, and date formats (e.g. `MM/DD`, `MMM DD`, `MM/DD/YY`).
- **IndexedDB Persistence**: Uploaded label templates and custom configurations are saved directly in your browser's local database. No server required.
- **Batch Printing & Downloads**:
  - Print all labels in one click or print individual cards.
  - Download all processed images as a single `.zip` file.
- **Munbyn Print Optimization**: Generates page-separated layouts styled specifically for 2" x 2" circular thermal labels with an interactive alignment guide.
- **Mobile-Responsive Design**: Tailored user interface optimized for phones and tablets.

---

## 🖨️ Munbyn / Thermal Printer Setup (Chrome/Brave)

Because the app generates each label copy as an individual print page, you need to configure Chrome's native print settings once to align perfectly with your physical 2"x2" round stickers:

1. **Destination**: Select your **Munbyn** (or Rollo) thermal printer.
2. **Paper Size**: Select **2 in x 2 in** (or `51mm x 51mm`).
3. **Layout**: **Portrait**.
4. **Margins**: Select **None** (crucial to prevent the dates from shifting off-center).
5. **Scale**: Select **100%** (or *Fit to printable area* if margins are clipping).

Once configured, the browser will remember these settings for all future prints.

---

## 🛠️ Local Development & Setup

This application is written in static HTML, Vue 3, and JSZip. Because it fetches default templates from the local `/labels` directory, modern web browsers will restrict loading these images due to CORS policies if you open `index.html` directly (via `file://`).

To run the application locally, you must serve it using a local development server:

### Option 1: Python (Built-in)
Run the following command in the project root:
```bash
python3 -m http.server 8000
```
Then visit: [http://localhost:8000](http://localhost:8000)

### Option 2: Node.js (npx)
```bash
npx serve
```
Then visit the URL shown in the terminal.

---

## 💡 Troubleshooting: UUID Downloads in Chrome

If downloading the ZIP bundle in Chrome names the file as a raw string of numbers and letters (e.g., `e2a2e1cb-030d-49a5-9d8d-c2f5798ee97f`) instead of `juice_labels_bundle.zip`, this is caused by a service worker cache collision or an extension intercepting the memory blob.

**To resolve:**
1. Open the page in **Incognito Mode** (this bypasses active extensions).
2. Or clear the local storage and cache: Open DevTools (`F12`) ➔ **Application** tab ➔ **Storage** ➔ click **Clear site data**, then reload.
