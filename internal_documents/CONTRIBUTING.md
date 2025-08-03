# 🤝 Contributing to Exoplanet Explorer Backend

First off, thank you for checking out this project and considering a contribution! Your expertise—whether it's in physics, backend development, or space nerd trivia—is welcome here. 🪐

---

## 🛠️ Project Overview

**Exoplanet Explorer Backend** is an async-ready backend that pulls real exoplanet data from NASA’s Exoplanet Archive API, processes it via ETL, and serves it via a modern FastAPI interface. It’s designed with physics principles in mind, including Kepler's Laws and habitability calculations.

---

## 🧑‍💻 How to Contribute

### 1. Fork and Clone
```bash
git clone https://github.com/YOUR-USERNAME/exoplanet-explorer-backend.git
cd exoplanet-explorer-backend
```

### 2. Create a Virtual Environment
```bash
# Using uv (recommended)
uv venv
uv pip install -r requirements.txt
```

Or with Conda or Poetry if preferred.

### 3. Create a Branch
```bash
git checkout -b feature/your-new-feature
```

---

## 🧪 Contribution Areas

We're open to all types of contributions:

| Type | Examples |
|------|----------|
| 🧹 Bug Fixes | Fixing broken queries or async issues |
| ✨ Features | Adding search filters, physics modules |
| 🧠 Science Help | Improve equations, constants, assumptions |
| 🧼 Refactoring | Cleaner ETL, better DB schema |
| 📝 Docs | Better README, new tutorials, diagrams |
| 🧪 Tests | More coverage, edge cases, async testing |

---

## ✅ Code Guidelines

- Use **`async def`** for all route handlers and API calls
- Follow **PEP8** + use `black` for formatting
- Write **docstrings** for all functions and classes
- Keep functions small and focused
- Include basic **unit tests** for new features
- Use **type hints** whenever possible

---

## 🚦 Testing & Linting

```bash
# Run unit tests
pytest

# Format code
black .

# Check types
mypy .
```

---

## 📦 ETL Best Practices

- Store ETL scripts inside the `/etl/` directory
- Make ingestion modular (e.g., `get_planet_data()`)
- Support both API and offline CSV ingestion
- Use `async` HTTP clients like `httpx`

---

## 🧪 Physics Modules

Physics helpers live in `/physics/` and should:

- Be pure Python functions
- Accept and return SI units unless stated otherwise
- Include test cases and real-world references (cite sources!)

---

## 🛡️ Security

If you discover a security vulnerability, **please do not open a public issue**. Instead, contact the project maintainer privately (see email in `README.md` or GitHub profile).

---

## 🙌 Code of Conduct

This project is governed by a [Code of Conduct](./CODE_OF_CONDUCT.md). Be kind, be curious, be space nerds together.

---

## 🌠 Final Thoughts

Science is best when shared. Whether you're calculating orbital periods, tuning API endpoints, or adding a sweet async habitability checker — your contribution matters. 💫

Let’s build the backend NASA *wishes* they had.

— The Exoplanet Explorer Core Team