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
