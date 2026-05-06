# Cognitive Map Sketcher

A zero-backend, single-file cognitive map drawing tool for sketch map experiments.

The app runs entirely in the browser. Participants draw routes, landmarks, areas, freehand paths, and text labels, then export structured JSON and a PNG reference image for later analysis in Python.

## Features

- Blank canvas and optional satellite basemap mode
- Freehand pen, landmark points, route polylines, area polygons, and text labels
- Required semantic tagging for every created object
- Chinese / English interface switch
- Edit layout mode for moving, scaling, rotating, and reordering objects
- Drawing order and timestamp records
- One-click export of:
  - `raw_strokes.json`
  - `semantic_objects.json`
  - `cognitive_graph.json`
  - `sketch.png`

## How To Use

Open `cognitive_map.html` directly in a browser, or open `index.html` after deploying the folder as a static site.

1. Fill in participant ID, area name, condition, and canvas mode.
2. Draw the sketch using the toolbar.
3. Add a semantic tag when prompted after each object is created.
4. Use Edit layout when you need to reposition or reorder objects.
5. Click Export to download the JSON files and PNG image.

## Data Notes

All coordinates are exported in canvas pixels. If satellite mode is used, the selected map center is saved in `meta.map_center`.

The exported cognitive graph is compatible with NetworkX-style node-link workflows. Inferred endpoint nodes are added when a route endpoint is not close to a user-drawn landmark.

## Deployment

This project is static HTML/CSS/JavaScript, so it can be deployed to GitHub Pages, Netlify, Cloudflare Pages, Vercel, or any static web server. No backend, database, or build step is required.
