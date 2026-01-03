# secure-notes: Zero-trust style secure notes app

## Core idea
- Notes are encrypted client-side (browser) before sending to API
- API stores only ciphertext + metadata
- Server never sees plaintext (true zero-trust pattern)

## 🚀 Live Demo
- Frontend: https://secure-notes-ui.onrender.com
- Backend/API: https://secure-notes-api-tbmw.onrender.com
- API Docs (if applicable): https://secure-notes-api.onrender.com/docs

> Replace the URLs above after you deploy on Render.

## 🧱 Architecture
- React (Render Static Site) → calls Python API (Render Web Service)
- Python API → PostgreSQL (Render Postgres)
- Optional: background worker later if needed

## 🛠 Tech Stack
- Frontend: React + Vite
- Backend: FastAPI + Uvicorn
- DB: PostgreSQL
- Deploy: Render (static + web service)

## ✨ Key Features
- Health endpoint + frontend wiring (scaffold)
- Add auth (JWT), RBAC, CRUD as you build
- Add tests and CI as you mature the repo

## ▶️ Run Locally
```bash
# from repo root
docker-compose up --build
# UI: http://localhost:5173
# API: http://localhost:8000/docs
```

## 🔧 Environment Variables
```bash
# Backend
DATABASE_URL=...
JWT_SECRET=...
ENV=production

# Frontend
VITE_API_BASE_URL=https://<your-api>
```

## 📦 Deployment (Render)
- This repo is structured for a **Render Static Site** (frontend) + **Render Web Service** (backend) when applicable.
- See `render.yaml` for an example multi-service setup.

## 🧪 Tests
```bash
# Backend (add pytest as you implement)
# Frontend (add vitest/playwright as you implement)
```

## 📸 Screenshots / GIF
- Add screenshots or a short demo GIF here to make the project recruiter-friendly.

## 🧠 Design Notes
- Add short notes about tradeoffs, API contracts, and security decisions.
