# F1 2025 Abu Dhabi Championship Predictor

A mobile-first web app to predict the 2025 Abu Dhabi Grand Prix finish order and calculate final championship standings.

## Features

- **Drag and drop** - Reorder drivers to predict race finish positions (touch and mouse friendly)
- **Live points calculation** - See starting points, race points gained, and final total
- **Championship highlights** - Gold/silver/bronze indicators based on final championship standings (not race position)
- **Persistent state** - Your predictions are saved to localStorage
- **Reset button** - Restore original championship order

## Usage

Open `index.html` in a browser. No build step required.

### Local Development

```bash
python3 -m http.server 8080
# Open http://localhost:8080
```

## Tech Stack

- **React 18** via esm.sh CDN
- **htm** for JSX-like syntax without build step
- **TailwindCSS** via Play CDN
- **SortableJS** for drag and drop

## Data

Driver standings are from the 2025 F1 season heading into the Abu Dhabi Grand Prix (final race).

Points system: 25-18-15-12-10-8-6-4-2-1 for positions 1-10, 0 for positions 11-20.
