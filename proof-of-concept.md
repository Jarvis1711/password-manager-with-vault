# Proof of Concept - Password Manager with Vault

## Scope
- App category: Education
- Entity model: Password Manager Learning Unit
- Deployable stack: Flask + SQLAlchemy + Gunicorn + Docker + CI

## Dynamic Field Configuration
- Learner Group: `learner_group` (text)
- Difficulty (1-5): `difficulty` (number)
- Material Notes: `material_notes` (textarea)

## Run Evidence Commands
```bash
python app.py
curl http://localhost:5000/api/health
curl http://localhost:5000/api/schema
curl -X POST http://localhost:5000/api/records   -H "Content-Type: application/json"   -d '{"title":"Demo Record","status":"in-session","payload":{"learner_group":"Demo value","difficulty":12,"material_notes":"seed note"}}'
curl http://localhost:5000/api/metrics
```

## Metadata
- Idea number: 60
- Generated UTC: 2026-03-24T15:52:22.196135+00:00
- Status: Phase-2 complete
