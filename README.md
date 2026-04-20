<div align="center">

# Second Opinion

### AI-Assisted Physician Second Opinions for Everyone

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.110+-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-3178C6?style=flat-square&logo=typescript&logoColor=white)
![FHIR R4](https://img.shields.io/badge/FHIR-R4-E84949?style=flat-square)
![GenAI](https://img.shields.io/badge/GenAI-LLM-FF6B35?style=flat-square)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)

</div>

---

## The Problem

**12 million Americans are misdiagnosed every year.** Medical second opinions are proven to change or refine diagnoses in up to 88% of cases — yet they remain slow, expensive, and deeply inaccessible.

- Getting a specialist second opinion takes **weeks to months** of scheduling
- Out-of-pocket costs range from **$300–$600** per consultation
- Patients arrive at each new appointment carrying **fragmented records** scattered across portals, PDFs, and printouts — forcing physicians to reconstruct history from scratch
- The result: wasted clinical time, missed context, and preventable harm

---

## The Solution

**Second Opinion** is a freemium SaaS platform that bridges the gap between patients and expert physician opinions — powered by AI.

1. **Patients upload their medical records** (PDFs, scans, lab results, discharge summaries)
2. **GenAI pre-processes and summarizes** the case into a structured, physician-ready brief
3. **Our matching engine connects patients** with verified physicians for expert second opinions
4. **Physicians review asynchronously** through a streamlined dashboard — no scheduling overhead

---

## Key Features

| Feature | Description |
|---|---|
| **AI Case Summarization** | GenAI structures unstructured patient records into concise clinical briefs |
| **FHIR R4 Integration** | Standards-compliant health data ingestion and interoperability |
| **Physician Matching Engine** | Specialty-aware algorithm to match cases to the right experts |
| **Freemium Patient Portal** | Self-serve upload and case management for patients |
| **Physician Dashboard** | Async review workflow with case queue and response tools |
| **HIPAA-Aware Architecture** | Designed with healthcare compliance requirements in mind |
| **LinkedIn Outreach Automation** | Automated physician network recruitment pipeline |

---

## Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                          CLIENT LAYER                               │
│                   React 18 / TypeScript / Tailwind                  │
│              Patient Portal  │  Physician Dashboard                 │
└────────────────────────┬────────────────────────────────────────────┘
                         │  HTTPS / REST
┌────────────────────────▼────────────────────────────────────────────┐
│                         API GATEWAY                                 │
│               Python 3.11+ / FastAPI / Pydantic                     │
│            Auth (JWT/OAuth 2.0)  │  Rate Limiting  │  Routing       │
└──────────┬──────────────────┬────────────────────┬──────────────────┘
           │                  │                    │
┌──────────▼──────┐  ┌────────▼────────┐  ┌───────▼──────────────────┐
│  GenAI Service  │  │  FHIR Interface │  │      PostgreSQL DB        │
│                 │  │                 │  │                          │
│  LLM Summarize  │  │  HL7 FHIR R4    │  │  Users / Cases / Reviews │
│  Case Structur. │  │  Record Ingest  │  │  Physician Profiles       │
└─────────────────┘  └─────────────────┘  └──────────────────────────┘
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | React 18, TypeScript, Tailwind CSS |
| **Backend** | Python 3.11+, FastAPI, Pydantic v2 |
| **AI / LLM** | GenAI LLM (case summarization & structuring) |
| **Health Data** | HL7 FHIR R4 |
| **Database** | PostgreSQL |
| **Auth** | JWT / OAuth 2.0 |
| **Deployment** | Docker, AWS |

---

## Getting Started

### Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate          # Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

API docs available at `http://localhost:8000/docs`

### Frontend

```bash
cd frontend
npm install
npm run dev
```

App available at `http://localhost:5173`

---

## Business Model

| Tier | Price | Includes |
|---|---|---|
| **Free** | $0 | AI-powered medical record summarization |
| **Standard** | $49 / case | AI summary + verified physician second opinion |
| **Premium** | $149 / case | AI summary + specialist opinion + video consultation |
| **Enterprise** | Custom | White-label API for health systems & insurers |

---

## Market Opportunity

| | Size |
|---|---|
| **TAM** — Global medical second opinion market | $28B+ |
| **SAM** — US digital health / telehealth second opinions | $4.2B |
| **SOM** — Addressable early market (complex/chronic cases) | $120M |

---

## Project Artifacts

The `/docs` directory contains supporting research and planning materials:

- **Pitch deck summary** — investor narrative and business model overview
- **Business plan** — full go-to-market, financial projections, and operating model
- **Market research** — competitive landscape and customer discovery findings
- **Compliance research** — HIPAA, FHIR, and healthcare regulatory landscape
- **Outreach automation** — LinkedIn physician recruitment pipeline design

---

## Contributors

| Name | Role | GitHub |
|---|---|---|
| **Prateek Verma** | Co-Founder | [@Prattkk](https://github.com/Prattkk) |
| **Suyash Sawant** | Co-Founder | [@suyash0612](https://github.com/suyash0612) |

---

## License

This project is licensed under the [MIT License](LICENSE) — see the LICENSE file for details.

---

<div align="center">
Built with ❤️ by the Second Opinion team
</div>
