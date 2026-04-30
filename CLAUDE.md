# Japan Trip 2026 — Travel Dashboard

## Overview
Single-page interactive travel dashboard for a family trip to Japan (May 12-30, 2026). Built with Tailwind CSS via CDN.

## Tech Stack
- Single `index.html` file
- Tailwind CSS via CDN (`<script src="https://cdn.tailwindcss.com"></script>`)
- Vanilla JavaScript for interactivity
- localStorage for persisting packing list checkbox state

## Editing Guidelines

### Adding/Editing Itinerary Items
Each day card in the itinerary section has Morning, Afternoon, and Evening slots. To add activities, find the relevant day card by its `data-day` attribute and edit the slot content directly.

### Adding Packing Items
Packing items are grouped by category. Add new `<li>` elements with checkboxes inside the relevant category `<ul>`. The checkbox ID should follow the pattern `pack-{category}-{item}` for localStorage persistence.

### Adding Transport/Accommodation
Follow the existing card structure. Each transport card includes: date, route, carrier/type, time, and booking reference. Each accommodation card includes: name, dates, address, and booking reference.

### Visual Theme
- Japan-inspired: soft pinks, warm whites, cherry blossom accents
- City color coding: Osaka (coral), Nagoya (amber), Shizuoka (green), Tokyo (blue), Narita (purple)
- Cards use rounded corners and soft shadows

## Workflow for Changes
1. Edit `index.html`
2. Screenshot with: `npx puppeteer screenshot index.html --fullpage`
3. Visually verify the changes render correctly
4. If issues found, fix and re-screenshot
