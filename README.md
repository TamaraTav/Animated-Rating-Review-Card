## Animated Rating Review Card

Interactive, animated rating summary card built with plain HTML, CSS, and JavaScript. It visualizes product review distribution with animated counters and progress bars, matching a clean, modern UI.

### UI Design Reference

The visual design of this component is based on the **“Reviews”** design from **UI Design Daily**:

- **Figma / UI Source**: [UI Design Daily – Reviews](https://www.uidesigndaily.com/posts/figma-reviews-day-1573)

This implementation recreates the layout and interactions in code.

## Features

- **Animated average rating**: Number smoothly counts up to the calculated average rating.
- **Animated review distribution bars**: Each star row animates from 0% to its actual share.
- **Dynamic data model**: All review numbers are driven from a single `REVIEWS` object in JavaScript.
- **SVG star icons**: Crisp vector stars reused for both average and row ratings.
- **Search input UI**: Styled search bar that fits the card design (ready to be wired to real filtering).

## Tech Stack

- **HTML5** – base markup and structure.
- **CSS3** – custom layout, typography, and subtle shadows/borders.
- **Vanilla JavaScript (ES6)** – data model, DOM rendering, and animations via `requestAnimationFrame`.

## Getting Started

### Prerequisites

- Any modern browser (Chrome, Firefox, Edge, Safari).
- Git (optional, only if cloning the repo).

### Run Locally (quick way)

1. Clone or download this repository.
2. Open the project folder in your file explorer or terminal (for example `Animated-Rating-Review-Card/`).
3. Open `index.html` in your browser:
   - Double‑click `index.html`, or
   - Drag and drop `index.html` onto an open browser window.

### Run via a simple static server (optional)

If you prefer using a local server (recommended for real projects):

1. Open a terminal in the project directory:

   ```bash
   cd Animated-Rating-Review-Card
   ```

2. Start a static server, for example with `npx`:

   ```bash
   npx serve .
   ```

3. Open the printed `http://localhost:xxxx` URL in your browser.

## Project Structure

```text
Animated-Rating-Review-Card/
├─ index.html      # Main HTML document and component markup
├─ styles.css      # Card layout, typography, and visual styles
├─ script.js       # Review data, DOM rendering, and animations
├─ star.svg        # Star icon asset (also inlined via SVG in HTML/JS)
└─ README.md       # Project documentation
```

## How It Works

- Review data is defined in `script.js` inside a single `REVIEWS` object.
- JavaScript computes:
  - Total number of reviews.
  - Weighted average rating.
  - Percentage width for each rating row.
- DOM elements for each row (star value, bar, and count) are generated dynamically.
- `requestAnimationFrame` is used to animate:
  - Average rating text.
  - Individual review counts.
  - CSS custom property `--width` on each progress bar.

To change the distribution, update `REVIEWS` in `script.js` and reload the page.

## Customization

- **Change colors**: Adjust the palette (background, star, and bar colors) in `styles.css`.
- **Change fonts**: Fonts are loaded from Google Fonts; you can swap or extend them in the `<head>` of `index.html`.
- **Adjust animation speed**: Modify the `DURATION` constant in `script.js` to speed up or slow down the counters and bar fills.
- **Integrate with real data**: Replace the static `REVIEWS` object with data from an API or backend.

## License

This project is intended primarily for **learning and personal use**.  
The UI concept belongs to **UI Design Daily**; please refer to their site and license terms for design usage:

- [UI Design Daily – Reviews](https://www.uidesigndaily.com/posts/figma-reviews-day-1573)

You are free to adapt the code for your own experiments, portfolios, or internal demos.

## Author

- **Author**: Tamara Tava  
- **LinkedIn**: https://www.linkedin.com/in/tamara-tava/

