# Claude Code Instructions

## Project Overview

Single-file F1 championship predictor app. No build step - runs directly in browser via CDN imports.

## Tech Stack

- React 18 + htm (via esm.sh CDN)
- TailwindCSS (Play CDN)
- SortableJS (jsDelivr CDN)

## Architecture

Everything is in `index.html`:
- Tailwind config with F1 team colors
- SortableJS styles
- ES module imports via importmap
- React components using htm tagged templates

### Key Components

- `App` - Main component, manages driver order state and localStorage sync
- `DriverRow` - Individual driver row with position, team color, points display

### State Management

- Driver order stored in React state
- Synced to localStorage on every change
- Championship positions calculated on render by sorting drivers by total points

## Important Logic

**Championship podium highlighting**: The gold/silver/bronze highlights are based on **final championship standings** (total points after race), NOT race finish position. A driver can finish P2 in the race but have gold highlight if they have the most total points.

## Testing

Use a local HTTP server:
```bash
python3 -m http.server 8080
```

## Modifying Driver Data

Driver data is in `INITIAL_DRIVERS` array. Each driver has:
- `id` - Unique identifier
- `name` - Driver name
- `team` - Team name
- `teamColor` - Key for Tailwind team color class
- `points` - Championship points before Abu Dhabi
