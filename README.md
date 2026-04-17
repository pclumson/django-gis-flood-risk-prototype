# 🌊 GeoDjango Flood Risk & Water Resources Dashboard

A scalable, cloud-native geospatial web application built with **Django**, **PostgreSQL/PostGIS**, and **Leaflet**. This prototype demonstrates the ability to ingest, store, visualize, and analyze hydrological data for climate resiliency and flood risk assessment.

Designed to support civil engineers and GIS analysts in tackling real-world infrastructure challenges.

## 🚀 Key Features

*   **Geospatial Database:** Utilizes **PostgreSQL with PostGIS** extension for efficient storage and querying of vector data (points, lines, polygons) and raster data.
*   **Interactive Mapping:** Renders dynamic flood zones, river networks, and elevation data using **Leaflet.js** and **Mapbox GL**.
*   **Data Ingestion Pipeline:** Supports uploading Shapefiles and GeoJSON via **GDAL/OGR** and **Rasterio** for immediate visualization.
*   **Spatial Analysis:** Implements server-side spatial queries (e.g., "Find all structures within 500m of a flood zone") using **GeoDjango ORM**.
*   **Cloud-Native Architecture:** Containerized with **Docker** and ready for deployment on **AWS** (RDS, EC2, S3).
*   **RESTful API:** Exposes geospatial data via **GeoDjango REST Framework** for integration with external tools.

## 🛠️ Tech Stack

| Category | Technologies |
| :--- | :--- |
| **Backend** | Python 3.11+, Django 5.0, GeoDjango, DRF |
| **Database** | PostgreSQL 15+, PostGIS 3.4 |
| **GIS Libraries** | GDAL, Rasterio, Shapely, Fiona, GEOS |
| **Frontend** | HTML5, CSS3, JavaScript, Leaflet, Mapbox GL |
| **DevOps** | Docker, Docker Compose, GitLab CI/CD |
| **Cloud** | AWS (RDS, S3, EC2) |

## 📂 Project Structure

```text
├── manage.py
├── requirements.txt
├── docker-compose.yml
├── .dockerignore
├── README.md
├── flood_risk_app/
│   ├── models.py          # GeoModels (FloodZones, Infrastructure)
│   ├── views.py           # GeoJSON views & Spatial queries
│   ├── serializers.py     # DRF Serializers with geometry fields
│   ├── urls.py
│   └── tests.py           # Unit tests for spatial logic
├── static/
│   └── js/
│       └── map.js         # Leaflet initialization & layer control
└── data/
    └── sample_flood_zones.geojson
