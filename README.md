# 🌌 Exoplanet Explorer Backend

**Exoplanet Explorer Backend** is a scientific data backend platform that lets users explore real-world exoplanet data through a modern, async-ready API powered by NASA’s Exoplanet Archive. It’s built for physicists, backend engineers, and cosmic enthusiasts alike.

---

## 🚀 Features

- ⚙️ **ETL Pipeline** – Pull and normalize exoplanet data from NASA’s TAP API or CSVs
- 🧠 **Physics Engine** – Kepler’s Laws, habitability metrics, and mass-radius analysis
- 🌐 **Async API** – FastAPI-powered endpoints with filter/search support
- 🗃️ **PostgreSQL or DuckDB** – Choose your backend, both with schema support
- 💫 **Modular Design** – Easy to expand or customize

---

## 🧭 Roadmap Highlights

See full roadmap in [`ROADMAP.md`](./ROADMAP.md) (coming soon).

### Current Phases

- [x] NASA API exploration & testing
- [x] Project scaffolding & folder structure
- [ ] ETL ingestion module with caching
- [ ] Async CRUD API with search
- [ ] Habitability computation engine

---

## 🧪 Physics Modules

We’re integrating scientific models that include:

- Kepler’s Third Law
- Mass-radius relationships
- Surface gravity & escape velocity
- Goldilocks Zone checks
- Earth Similarity Index (ESI) (planned)

---

## 📦 Tech Stack

| Area              | Stack                         |
|-------------------|-------------------------------|
| Backend API       | FastAPI (async)               |
| Data Ingestion    | Python, ADQL, `httpx`         |
| Storage           | DuckDB (local) / PostgreSQL (prod) |
| ORM               | SQLAlchemy                    |
| Background Tasks  | APScheduler or Celery (TBD)   |
| Caching           | Redis (optional)              |
| Physics Engine    | Pure Python modules           |

---

## 🧑‍💻 Setup Instructions

```bash
# Clone the repo
git clone https://github.com/YOUR-USERNAME/exoplanet-explorer-backend.git
cd exoplanet-explorer-backend

# Create virtual environment
uv venv  # or conda/poetry

# Install dependencies
uv pip install -r requirements.txt

# Run the API (development)
uvicorn app.main:app --reload
```

---

## 🤝 Contributing

We welcome all contributors—whether you're a backend wizard or a stargazing hobbyist. See [CONTRIBUTING.md](./CONTRIBUTING.md) for details.

---

## 🌠 License

MIT License © 2025

---

## 📫 Contact

Project maintained by [DevByBrice](http://www.devbybrice.com). For inquiries, bugs, or stardust, contact via GitHub or email listed in the repo.

---

> “Somewhere, something incredible is waiting to be known.”  
> — Carl Sagan
