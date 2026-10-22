# Civic Signal

**Working title:** a source-led public-infrastructure observatory. Phase 1 focuses on Thane; later geographic expansion is staged behind source-coverage checks.

## What it is

Civic Signal connects public project records, budgets, milestones, locations, and evidence trails. It highlights changes for a person to review; it does not label a discrepancy as wrongdoing or present an automated signal as an official project status.

## Visual direction

The interface is a city-model field guide rather than a conventional KPI dashboard: a full-width 3D map is the primary visual, editorial serif typography sits over the map scene, camera and layer controls stay attached to that scene, and project updates read as an evidence-review feed. Motion is tied to map navigation and project markers. The overview avoids unverified counts and percentages. This follows the design references' emphasis on a clear visual thesis, deliberate composition, and purposeful motion without copying a particular site's layout.

## Current prototype

This folder is a static, Vercel-ready web prototype. Its Thane basemap is streamed from OpenFreeMap and uses real OpenStreetMap-derived building geometry rendered as 3D extrusions. Project cards, points, budgets, progress values, and activity entries are illustrative fixtures; they are visibly labeled as sample data and are not verified live claims.

Working views include Overview, City Model, Projects, Milestones, Public Spend, Evidence Room, Watchlist, Briefings, Data Sources, and Method & Limits. Search, map camera controls, layer visibility, project filters, CSV export, local watchlist persistence, and local text briefing export are wired in the prototype.

## Real-city model plan

- **Free default:** OpenStreetMap-derived OpenFreeMap vector tiles rendered with MapLibre GL JS. The buildings are actual mapped footprints; where height tags are missing, the visualization uses a clearly disclosed visual fallback. This is a mapped city model, not photogrammetry or survey-grade reality capture.
- **Google option:** Google Photorealistic 3D Tiles can provide a textured city mesh only where coverage exists. It requires a Google Cloud project, API key, billing configuration, compliant Google and source attribution, and must remain a visualization layer. Google prohibits using this tile service for extraction, tracing, caching beyond its rules, or offline map-data creation.
- **Apple option:** Apple MapKit JS can supply its own street, satellite, or hybrid map view, annotations, and web Look Around experiences. Its MapKit JS map-type list does not expose Apple's native Flyover map type, so Apple is a complementary base/inspection view, not a downloadable Thane model source.
- Provider imagery will never be copied, scraped, or traced to manufacture Civic Signal's own city data. Google, Apple, and open layers will remain distinct selectable sources with their own attribution and terms.

## Geographic rollout

1. Thane
2. Pune, Mumbai, and Navi Mumbai
3. Additional Maharashtra cities
4. Cities across India
5. Cities and towns worldwide

The map explorer includes working camera presets for Thane, Mumbai, Navi Mumbai, Pune, Maharashtra, India, and a whole-world view. These presets expose map geometry only; this prototype's project fixtures remain Thane-only and illustrative. Verified project datasets and source connectors expand only after their coverage, license, freshness, and quality can be shown honestly.

## Run locally

Serve this folder over HTTP, for example with `python3 -m http.server 8000`, and open `http://localhost:8000`. The map and web fonts need an internet connection. No API key is required for the open-data map prototype. Google and Apple provider integrations are not connected in this build: Google needs a restricted Cloud key, billing, attribution, and a coverage check; Apple needs a Maps token. Their maps can be selected as licensed visualization providers, but their imagery must not be copied or traced into Civic Signal's own geographic data.

## Data sources and terms

- [OpenFreeMap quick start and attribution](https://openfreemap.org/quick_start/)
- [MapLibre GL JS 3D building extrusion example](https://maplibre.org/maplibre-gl-js/docs/examples/display-buildings-in-3d/)
- [OpenStreetMap copyright and ODbL attribution](https://www.openstreetmap.org/copyright)
- [Google Photorealistic 3D Maps coverage](https://developers.google.com/maps/documentation/javascript/3d/coverage)
- [Google Map Tiles API usage policy](https://developers.google.com/maps/documentation/tile/policies)
- [Apple MapKit JS documentation](https://developer.apple.com/documentation/mapkitjs)
