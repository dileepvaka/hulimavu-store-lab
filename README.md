# Hulimavu Store Lab

Interactive browser-based fixture planner for the Hulimavu and Arekkere retail layouts.

## Run

Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8080
```

Then open <http://localhost:8080>.

Use the same URL each time. Browser storage is scoped by origin, so `localhost:8080`, `127.0.0.1:8080`, another port, and opening `index.html` directly are treated as separate saved locations.

Use the store selector in the header to switch between:

- **Hulimavu:** approximately 2,000 sq ft retail
- **Arekkere:** 1,073 sq ft retail with a 55 sq-ft toilet, left stair/landing display risk zone and right-side glazing

## What you can edit

- Drag floor racks, wall-side racks, fresh tables, chillers/freezers, staples bins, pallets, billing counters and entry turnstiles
- Configure rack height, number of bays and 1–1.5 ft bay width before adding
- Floor racks are represented as two-sided; wall racks are one-sided
- Racks can be categorised as General, Ambient vegetables, Staples, FMCG or General merchandise
- The dedicated Ambient Veg Rack tool lets users choose one-sided or two-sided construction and free/middle or edge placement
- Each rack can use free/grid placement or edge snapping against walls, the partition, fixed shaft or another rack
- Umbrellas and broom sticks use a compact 1 ft × 1 ft square long-goods bin; the separate vegetable-stand fixture has been removed
- Rack height is metadata (typically 5 ft floor / up to 9 ft wall) and no longer changes the top-view footprint length
- Configure chiller/freezer type and length, ice-cream chest-freezer size, ambient vegetable-stand width, bin count, pallet count and quantity
- Add any number of billing counters and turnstiles from the fixture library
- Click a fixture to edit rack height, bays, bay width, equipment type, length, or bin/pallet count
- Double-click or press `R` to rotate a selected fixture
- Use arrow keys to nudge; Delete/Backspace to remove
- Drag the blue rear-partition handle vertically
- Toggle customer flow, old partition and annotations
- Track estimated retail/back-office area and staples-bin count live
- Save the current plan to browser local storage; the app also auto-saves when the page is hidden or closed
- Export/import a layout JSON file to move a saved plan between localhost, GitHub Pages, browsers or teammates
- Toggle between the editable 2D plan and a live 3D isometric store view
- Orbit the 3D camera by dragging and zoom with the mouse wheel
- See stocked rack shelves, staples bins, fresh displays, refrigeration, billing and architectural boundaries in 3D
- Export the edited 2D plan as SVG or PNG

## Arekkere concept

- 36 staples bins, reduced from the earlier 48-bin proposal
- Fresh visible early in the journey, with an ambient-vegetable two-sided rack placed freely in the middle
- Adjacent supervised entry and exit aligned directly with the left staircase: entry on the left, exit on the right
- Rice-bag/pallet display allowed at the left stair landing, clearly marked as outside billing control
- Right boundary treated as glazing; fixtures may still be placed there deliberately
- Separate browser save and import/export file names from Hulimavu

## Initial Hulimavu planning concept

- Fresh is the first strong view after entry
- Customer route is Entry turnstile → Fresh → Staples → 5 ft racks → Billing → controlled exit
- Entry and exit sit beside each other, separated by a configurable low partition/rail
- Exit is channelled past the billing counters, giving the biller direct sight of both entry and exit
- 42 circular staples bins are retained (28-bin and 14-bin banks)
- Nine office workstations and the fixed shaft are retained
- Proposed partition position targets approximately 2,000 sq ft retail area

The 3D view loads Three.js from an online CDN and therefore requires an internet connection on first load.

This is a schematic planning tool, not a construction drawing. Verify dimensions, partition position, aisle clearances, fire egress and refrigeration services in CAD and on site.
