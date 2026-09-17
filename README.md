# Clinic Greeting Lookup

A browser-only lookup page that downloads `Persistent Variable Sheet.xlsx` over HTTP and returns the greeting type associated with a clinic password.

## How it works

- The page fetches the workbook from the repository's raw GitHub URL.
- SheetJS parses the first worksheet in the browser.
- The first row is treated as the header row. The page recognizes `Clinic Password` (or `Password`) and `Greeting Type` (or `Greeting`) columns.
- Entering a password searches the loaded rows and displays the matching greeting type.

Open `index.html` through a web server or GitHub Pages. The spreadsheet must be publicly accessible for a browser HTTP request, and the raw GitHub URL must remain available to avoid CORS issues.
