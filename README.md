# Marine GPS Map — browser starter

## Features
- Browser GPS via `navigator.geolocation`
- Compass/orientation support where browser/device permission allows it
- GPS speed (knots), accuracy, altitude, and course over ground where supplied by device
- Waypoints, tap-to-add map markers, GeoJSON import/export
- Track recording and GPX export
- Optional provider-supplied marine/depth chart tile overlay
- PWA shell caching

## Run
Serve the directory over HTTPS or localhost, e.g. `python -m http.server 8000`, then open `http://localhost:8000`. On iPhone, host it on an HTTPS site (such as GitHub Pages) for location and motion permission prompts.

## Critical marine/offline limitations
This is a starter, not a certified chartplotter and not a full offline Google Maps clone. The default OSM map needs internet. The service worker caches app files only; it does not download map tiles. For true offline use, bundle Leaflet locally and integrate a licensed offline regional tile archive or local tile server. Do not bulk-download public OpenStreetMap tiles. Depth contours, soundings, and navigation aids only appear if a suitable licensed marine chart provider supplies the overlay tiles. Do not rely on this app as the sole navigation or safety system; verify position, chart datum, depths, and route against official up-to-date nautical charts and onboard instruments.
