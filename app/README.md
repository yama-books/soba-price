# App prototype (UI v0.2)

**Open [prototype/index.html](prototype/index.html)** to inspect the single-file HTML/CSS/JavaScript prototype. To operate it locally without tools, select GitHub's **Raw / Download raw file**, save as index.html and open it in a browser. No local Python, package installation, web API or backend is needed.

## What works in the prototype
- Filter seven **fictional** UI samples by era, country, item and keyword. The start/end year sliders use explicit values.
- Switch among timeline, comparison and source-reference views.
- Open a right-side detail drawer, inspect the note accordion, add/remove samples from a comparison tray.
- Reset filters, show a brief toast, test the skeleton placeholder, and read the explanatory modal.
- Responsive PC/mobile layout, keyboard focus indication, Escape closing, reduced-motion CSS.

## What is deliberately NOT present
- No verified historic price observations; the app does not load data/verified or sources/price_leads.csv.
- No live data fetching, no actual currency/price calculations, no claims of historical price accuracy.
- No formal browser automation run, real-device testing, CI validation, or GitHub Pages deployment.

Documentation: [model diagram](../../docs/UI_WIREFRAME.md), [motion plan](../../docs/UI_MOTION_PLAN.md), [roadmap](../../docs/IMPLEMENTATION_ROADMAP.md).
