# Proof of Concept - Flashcard Master

## Scope
- App category: Productivity
- Entity model: Flashcard Master Task
- Deployable stack: Flask + SQLAlchemy + Gunicorn + Docker + CI

## Dynamic Field Configuration
- Owner: `owner` (text)
- Priority (1-5): `priority` (number)
- Operational Notes: `notes` (textarea)

## Run Evidence Commands
```bash
python app.py
curl http://localhost:5000/api/health
curl http://localhost:5000/api/schema
curl -X POST http://localhost:5000/api/records   -H "Content-Type: application/json"   -d '{"title":"Demo Record","status":"in-progress","payload":{"owner":"Demo value","priority":12,"notes":"seed note"}}'
curl http://localhost:5000/api/metrics
```

## Metadata
- Idea number: 35
- Generated UTC: 2026-03-24T15:52:21.992822+00:00
- Status: Phase-2 complete
