# Project Structure

exoplanet-explorer-backend/
│
├── src/
│   ├── app/                  # Main FastAPI app
│   │   ├── __init__.py
│   │   ├── main.py           # FastAPI app instance
│   │   ├── api/              # API routers
│   │   ├── models/           # SQLAlchemy models
│   │   ├── db/               # DB utils and sessions
│   │   ├── core/             # Config, constants, logging
│   │   ├── physics/          # Physics formulas & calculators
│   │   └── etl/              # Extract, Transform, Load (ETL) pipelines and NASA ingestion
│   │
│   └── tests/                # Pytest unit and integration tests
│
├── .env                      # Environment variables (gitignored)
├── README.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── requirements.txt
├── pyproject.toml (if using poetry/uv)
└── Dockerfile (optional)
