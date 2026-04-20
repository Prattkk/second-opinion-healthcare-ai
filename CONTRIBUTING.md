# Contributing to Second Opinion

Thank you for your interest in contributing! This guide covers everything you need to get started.

---

## Workflow

1. **Fork** the repository to your GitHub account
2. **Create a feature branch** from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes**, following the code style guidelines below
4. **Commit** using the conventional format (see below)
5. **Push** your branch and open a **Pull Request** against `main`
6. Request a review from one of the maintainers

---

## Development Setup

### Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate          # Windows: venv\Scripts\activate
pip install -r requirements.txt
pip install -r requirements-dev.txt   # linting, testing tools
uvicorn app.main:app --reload
```

Run tests:
```bash
pytest
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

Run linter:
```bash
npm run lint
```

---

## Code Style

### Backend (Python)
- Follow **PEP 8** — enforced via `ruff` and `black`
- Type annotations required on all public functions
- Docstrings for public modules, classes, and functions (one-line format preferred)

### Frontend (TypeScript / React)
- Follow **ESLint** rules defined in `.eslintrc`
- Use functional components with hooks — no class components
- Prefer explicit types over `any`

---

## Commit Message Format

Use imperative mood and one of these prefixes:

| Prefix | When to use |
|---|---|
| `Add` | New feature or file |
| `Fix` | Bug fix |
| `Update` | Change to existing feature |
| `Refactor` | Code restructuring with no behavior change |
| `Docs` | Documentation only |

**Examples:**
```
Add physician matching endpoint
Fix token expiry bug in auth middleware
Update FHIR ingestion to handle R4 bundles
Docs: add API authentication guide
```

---

## Healthcare Compliance Note

This project handles **Protected Health Information (PHI)**. All contributors must:

- **Never commit real patient data** — use synthetic data only for development and testing
- Follow **HIPAA minimum necessary** principles when designing data flows
- Avoid logging PHI (names, DOB, diagnosis codes, etc.) at any log level
- Raise a security concern in your PR description if your change touches data storage, transmission, or access control

If you're unsure whether something is compliant, open an issue and tag a maintainer before proceeding.

---

## Maintainers

| Name | GitHub | Role |
|---|---|---|
| Prateek Verma | [@Prattkk](https://github.com/Prattkk) | Co-Founder |
| Suyash Sawant | [@suyash0612](https://github.com/suyash0612) | Co-Founder |

For questions, open a GitHub issue or reach out directly via GitHub.
