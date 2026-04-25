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

```text.
├── data
│   ├── sample_flodd_zone.geojson
│   └── sample_sensor_readings.json
├── docker-compose.yml
├── Dockerfile
├── flood_risk_app
│   ├── admin.py
│   ├── apps.py
│   ├── consumers.py
│   ├── __init__.py
│   ├── kinesis_consumer.py
│   ├── management
│   │   └── commands
│   │       ├── consumer_sensors.py
│   │       └── load_flood_zones.py
│   ├── migrations
│   │   └── __init__.py
│   ├── models.py
│   ├── mttq_consumer.py
│   ├── routing.py
│   ├── serializers.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── manage.py
├── poetry.lock
├── pyproject.toml
├── requirements.txt
├── services
│   └── hecras_parser.py
├── simulate_sensor.py
├── static
│   ├── css
│   ├── images
│   └── js
│       └── map.js
├── templates
│   └── map.html
└── water_gis
    ├── asgi.py
    ├── __init__.py
    ├── __pycache__
    │   ├── __init__.cpython-314.pyc
    │   └── settings.cpython-314.pyc
    ├── settings.py
    ├── urls.py
    └── wsgi.py





## 🚀 Roadmap & Enhancements

### ✅ Completed
- [x] GeoDjango + PostGIS backend
- [x] Leaflet 2D visualization
- [x] Docker containerization

### 🔄 In Progress
- [ ] **HEC-RAS Integration**: Parsing XML outputs and storing water surface profiles
- [ ] **MQTT Sensor Network**: Real-time water level monitoring from IoT devices
- [ ] **3D Visualization**: CesiumJS terrain-aware flood modeling

### 📅 Planned
- [ ] **Vector Tile Generation**: Optimizing for large-scale datasets
- [ ] **Machine Learning**: Predictive flood modeling using historical data
- [ ] **Mobile App**: React Native companion for field engineers
