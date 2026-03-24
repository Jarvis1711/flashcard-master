# Flashcard Master

## Solution Summary
Production-ready domain application.

This Phase-2 implementation is a domain-ready, deployable web application for **Productivity** workflows.

## Core Capabilities
- Responsive dashboard with KPI cards and recent activity table
- Domain record lifecycle with full CRUD (web + API)
- Dynamic schema fields tailored to this use case
- Status pipeline: `backlog, in-progress, blocked, done`
- Docker + Gunicorn deployment assets, CI checks, and Pytest tests

## Domain Model
- Primary entity: **Flashcard Master Task**
- Collection: **Flashcard Master Tasks**
- Dynamic fields:
- Owner (`owner` / text)
- Priority (1-5) (`priority` / number)
- Operational Notes (`notes` / textarea)

## Operational Workflow
1. Create task
2. Prioritize
3. Track execution
4. Complete and review

## API
- `GET /api/health`
- `GET /api/schema`
- `GET /api/records`
- `POST /api/records`
- `GET /api/metrics`

## Run Locally
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Docker Run
```bash
docker compose up --build
```

## Proof of Concept
- [proof-of-concept.md](proof-of-concept.md)
- [proof/demo-output.txt](proof/demo-output.txt)
- [proof/ui-preview.svg](proof/ui-preview.svg)
