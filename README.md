# SIFGUARD - AI-Powered Safety Intelligence Platform

[![Live Demo](https://img.shields.io/badge/Live%20Demo-sifguard--five.vercel.app-0070F3?style=for-the-badge&logo=vercel&logoColor=white)](https://sifguard-five.vercel.app/)
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/ladanikirtan10-cyber/sifguard&root-directory=frontend)

> 🚀 **Live Demo**: [https://sifguard-five.vercel.app/](https://sifguard-five.vercel.app/)

SIFGUARD is an AI-driven industrial safety intelligence system designed to detect Serious Injury and Fatality (SIF) precursors, analyze incident reports, evaluate hazard risks, and recommend actionable corrective controls.

---

## 🌐 Live Demo & Deployment

- **Live URL**: [https://sifguard-five.vercel.app/](https://sifguard-five.vercel.app/)
- **GitHub Repository**: [https://github.com/ladanikirtan10-cyber/sifguard](https://github.com/ladanikirtan10-cyber/sifguard)

### Deploy to Vercel

Click the badge below to deploy your own instance to Vercel:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/ladanikirtan10-cyber/sifguard&root-directory=frontend)

- **Root Directory**: `frontend`
- **Framework Preset**: Next.js
- **Environment Variables (Optional)**:
  - `NEXT_PUBLIC_API_URL`: Your hosted FastAPI backend URL (e.g. on Render, Railway). If not provided, the frontend will automatically use built-in safety intelligence fallback data for all views.

---

## 🌟 Key Features

- **Automated SIF Precursor Detection**: Identifies life-threatening risk vectors and precursor patterns from incident and observation logs.
- **Risk Scoring & Classification**: Rule-based & heuristic risk engine assessing severity, probability, and category (e.g., Working at Heights, Confined Space, Electrical Safety).
- **Incident Intelligence Copilot**: Interactive safety copilot assisting safety officers in querying trends, root causes, and recommended actions.
- **Explainability Engine**: Provides full step-by-step reasoning for why an incident is classified as a SIF precursor.
- **Modern Responsive Dashboard**: Interactive user interface built with Next.js, React, and Tailwind CSS.

---

## 🏗️ Architecture

```
sifguard/
├── backend/                  # FastAPI & SQLAlchemy Backend
│   ├── ai/                   # AI engines: classifier, copilot, risk scorer, explainability
│   ├── data/                 # Seed data and baseline safety incidents
│   ├── main.py               # API routes and server configuration
│   ├── models.py             # SQLAlchemy ORM models
│   ├── schemas.py            # Pydantic schemas
│   ├── seed.py               # Database seeder
│   └── requirements.txt      # Python dependencies
│
└── frontend/                 # Next.js Frontend Application
    ├── src/
    │   ├── app/              # App router (Dashboard, Reports, Actions, Copilot)
    │   ├── components/       # UI & feature components
    │   └── lib/              # Utility helpers
    ├── package.json          # Node dependencies
    └── tailwind.config.ts    # Tailwind styling config
```

---

## 🚀 Quick Start

### 1. Prerequisites
- **Python**: 3.10+
- **Node.js**: 18+ & npm

### 2. Backend Setup
```bash
cd backend
python -m venv venv

# On Windows:
.\venv\Scripts\activate
# On Linux/macOS:
# source venv/bin/activate

pip install -r requirements.txt

# Seed initial database (optional if sifguard.db is present)
python seed.py

# Run FastAPI server
uvicorn main:app --reload --port 8000
```
Backend API docs will be available at: `http://localhost:8000/docs`

### 3. Frontend Setup
```bash
cd frontend
npm install
npm run dev
```
Access the application at: `http://localhost:3000`

---

## 🛡️ License

MIT License.
