# 🌌 Exoplanet Explorer Backend – Roadmap

## 🚀 Overview

The **Exoplanet Explorer Backend** is a scientific data backend service designed to query, store, and analyze exoplanet data using NASA’s Exoplanet Archive API and/or other public datasets. The system will feature an ETL pipeline, asynchronous endpoints, and support for spatial and physics-based analysis (e.g., Kepler’s Laws, mass-radius relationships, and habitability scoring).

---

## 🧭 Phased Roadmap

### Phase 1 – Project Setup & API Exploration ✅

- [ ] Create Git repository and environment (Conda or `uv`, Poetry)
- [ ] Choose between FastAPI or Flask for backend
- [ ] Research and test NASA’s [TAP API](https://exoplanetarchive.ipac.caltech.edu/TAP)
- [ ] Verify access to key data fields (mass, radius, orbit, etc.)
- [ ] Decide on ETL storage format: DuckDB or PostgreSQL

---

### Phase 2 – ETL Pipeline & Initial Storage

- [ ] Build a small async ETL script to:
  - Query NASA API (ADQL or CSV)
  - Clean and normalize data
  - Store in DuckDB (for local prototyping) or PostgreSQL (for production)
- [ ] Create reusable ETL module (e.g., `etl/nasa_exoplanets.py`)
- [ ] Implement automated update scheduler (e.g., APScheduler or cron)

---

### Phase 3 – Database Schema Design

- [ ] Design schema to store:
  - Planetary data (name, mass, radius, orbit, host star)
  - Host star metadata
  - Habitability index fields (to be computed)
- [ ] Add spatial index support (if enabling geolocation-based queries)
- [ ] Implement SQLAlchemy or equivalent ORM models

---

### Phase 4 – Backend API (CRUD + Search)

- [ ] Create API endpoints:
  - `GET /planets` with filters (mass, radius, period, etc.)
  - `GET /planets/{planet_id}`
  - `POST /planets` (manual insert for testing)
  - `PUT /planets/{id}`, `DELETE /planets/{id}`
- [ ] Enable full-text search (e.g., planet name)
- [ ] Paginate & sort responses
- [ ] Add OpenAPI/Swagger UI support

---

### Phase 5 – Physics Modules

- [ ] Implement Kepler's Third Law calculations
- [ ] Add mass-radius relationship estimator
- [ ] Compute surface gravity and escape velocity
- [ ] Define habitability metrics:
  - Goldilocks Zone checker
  - Earth Similarity Index (ESI)

---

### Phase 6 – Performance & Async Improvements

- [ ] Make all routes fully asynchronous with `async def`
- [ ] Add caching layer (Redis or SQLite)
- [ ] Optimize ETL queries with batching or filtering
- [ ] Enable API rate limiting and validation

---

### Phase 7 – Deployment & Observability

- [ ] Dockerize the backend
- [ ] Deploy to Render, Railway, or self-hosted VPS
- [ ] Add logging, tracing, and basic monitoring
- [ ] Document environment variables and .env setup

---

## 🧠 Stretch Goals

- [ ] Add Celestial Visualization API (e.g., orbital path plotting)
- [ ] Integrate with Streamlit or frontend dashboard
- [ ] Offer downloadable datasets (CSV/JSON) from the API
- [ ] Add authentication for advanced users

---

## 📦 Tech Stack Summary

| Area                | Technology               |
|---------------------|--------------------------|
| Backend Framework   | FastAPI (Async)          |
| ETL & Ingestion     | Python + `httpx`, `pandas`, ADQL |
| Storage             | DuckDB (local), PostgreSQL (prod) |
| Async Tools         | `httpx`, `asyncpg`, `APScheduler` |
| Spatial Indexing    | PostGIS (PostgreSQL) or DuckDB extensions |
| Deployment          | Docker, Railway/Render   |

---

## 📚 Reference Links

- [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu)
- [API Docs (TAP/ADQL)](https://exoplanetarchive.ipac.caltech.edu/docs/TAP/usingTAP.html)
- [Open Exoplanet Catalogue (GitHub)](https://github.com/OpenExoplanetCatalogue)

---
