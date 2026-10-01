# Dream Palaces Project Overview

Dream Palace is a full-stack platform for showcasing Black cinema and preserving historical Black newspapers, combining an OCR digitization pipeline, a custom API, self-built algorithms for Spilhaus projection, and interactive map-based frontends into a single archival system.
Dream Palace is a full-stack platform for showcasing Black cinema and preserving historical Black newspapers, combining an OCR digitization pipeline, a custom API, self-built algorithms for Spilhaus projection, and interactive map-based frontends into a single archival system.

## Architecture

_System architecture diagram coming soon._

## Components

| Component                 | What it does                                                                                                                                                                                                 | Tech                                                 | Repo                                                                              |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------- | --------------------------------------------------------------------------------- |
| OCR Pipeline              | End-to-end digitization of a 197,364-page historical newspaper archive, including PDF ingestion, OCR on HPC GPU cluster, and structured storage; re-engineered for ~11× throughput (472 → 5,360 pages/hour). | Python, Surya, Slurm, pypdfium2, Supabase (Postgres) | [DreamPalacesOCR](https://github.com/yuyingxieuw/DreamPalacesOCR)                 |
| API                       | Central backend serving structured data to the webmap and design-team frontends; defines the Supabase schema and data-entry standards used by the data collection team.                                      | Flask, Supabase (Postgres), Render                   | [DreamPalacesAPI](https://github.com/yuyingxieuw/DreamPalacesAPI)                 |
| Spilhaus Reprojection App | Web app that reprojects GeoJSON into the Spilhaus projection and repairs seam-crossing stray-line artifacts via custom computational-geometry algorithms.                                                    | Python, Flask, GeoPandas, Shapely, PyProj, Leaflet   | [SpilhausReprojectionAPP](https://github.com/yuyingxieuw/SpilhausReprojectionAPP) |
| Frontend                  | Interactive, map-based interface for browsing the Black cinema showcase and newspaper archive; lets users switch between two map projections to create new geospatial imaginaries and visual experiences.    | Vanilla JS, Leaflet, Vercel                          | _(soon)_                                                                          |
| Vector Basemap            | Customized vector basemap (EPSG:4326) served as PMTiles/MBTiles.                                                                                                                                             | Protomaps (Leaflet), Tippecanoe, Cloudflare R2       | _(soon)_                                                                          |
| Raster Basemap            | Raster basemap for the Spilhaus projection, tiled for web delivery.                                                                                                                                          | ArcGIS Pro, GDAL                                     | —                                                                                 |

## My Role

As the sole technical lead on Dream Palace, I work alongside several design and data-collection teams. I own every technical decision and built the full stack end-to-end: the OCR pipeline, the central API serving all frontends, the interactive map interface, the vector and raster basemaps, and the custom Spilhaus reprojection algorithms. I also designed the shared data schema and data-entry standards used across the project's teams.
As the sole technical lead on Dream Palace, I work alongside several design and data-collection teams. I own every technical decision and built the full stack end-to-end: the OCR pipeline, the central API serving all frontends, the interactive map interface, the vector and raster basemaps, and the custom Spilhaus reprojection algorithms. I also designed the shared data schema and data-entry standards used across the project's teams.
