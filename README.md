# Flashcard Master

## Phase 3 Upgrade Summary
Production-oriented education solution for flashcard master workflows.

## Domain Context
- Domain: **Education**
- Core Entity: **Curriculum Item**
- Lifecycle Statuses: `draft, active, review, published`

## Architecture
- Flask application factory pattern (`app/__init__.py`)
- Layered backend (`routes` → `services` → `repositories`)
- SQLAlchemy persistence with JSON payload modeling
- REST API + HTML dashboard + CSV exports
- Deployment surfaces (`Dockerfile`, `docker-compose.yml`, `Procfile`, `wsgi.py`)

## Capability Set
- Role-ready modular architecture (routes, services, repositories)
- Operational dashboard with status metrics and pipeline view
- CRUD workflows via web UI and REST API
- CSV export endpoint for reporting
- Ready for production via Gunicorn, Docker, and Procfile

## Dynamic Schema
- Cohort (`cohort` / text)
- Difficulty (`difficulty` / number)
- Learning Notes (`learning_notes` / textarea)

## Quick Start
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python run.py
```

## API Highlights
- `GET /api/health`
- `GET /api/schema`
- `GET /api/items`
- `POST /api/items`
- `PUT /api/items/<id>`
- `DELETE /api/items/<id>`
- `GET /api/metrics`

## Proof of Concept
- [proof-of-concept.md](proof-of-concept.md)
- [proof/demo-output.txt](proof/demo-output.txt)
- [proof/ui-preview.svg](proof/ui-preview.svg)
- [proof/architecture.md](proof/architecture.md)
