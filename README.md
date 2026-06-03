## 🚀 Live Demo
[View Live Demo](https://mnpezz.github.io/labels/)

⚙️ How it works now:
Print Quantity Fields: There is now a new "Print Quantity" selector on each label card (defaults to 1).
IndexedDB Persistence: Your configured print quantities are automatically saved in local IndexedDB. If you refresh the page or return tomorrow, your batch quantities will remain exactly as you set them!
Multi-Page Spooling: When you click "Print" on a single card or "Print All Labels", the app dynamically generates the exact number of pages specified by the quantity fields. If you set "Root Juice" to 5 and "Daily Dose" to 2, it will send exactly 7 pages to the printer.
🖨️ How to configure your Chrome Print Settings for the Munbyn Printer:
Since the app sends each label copy as an individual print page, you need to configure Chrome's native print dialog once to tell it how to handle the physical 2"x2" round labels.

When the Chrome print preview window opens, set the following:

Destination: Select your Munbyn printer.
Paper Size: Select 2 in x 2 in (or 51mm x 51mm).
Layout: Portrait.
Margins: Select None (this is critical to prevent the date text from shifting off-center).
Scale: Select 100% (or Fit to printable area if you have alignment issues).
Once you print once with these settings, Chrome will remember them for all future print jobs. Each copy will feed out of the Munbyn printer as a perfectly aligned 2"x2" circular sticker!

