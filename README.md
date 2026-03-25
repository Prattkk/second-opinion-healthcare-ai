# Second Opinion

**AI that turns a patient's scattered medical records into a single, doctor-ready summary they can hand to any provider at any visit.**

Built for the [COZAD New Venture Competition 2026](https://tec.illinois.edu/programs-and-events/cozad) at the University of Illinois Urbana-Champaign.

---

## The Problem

Patients managing chronic conditions, rare diseases, or multiple specialists carry years of fragmented medical history — scattered across hospital portals, PDFs, discharge papers, and prescription printouts.

At every new appointment, doctors spend the first 10 minutes reconstructing that history from scratch. This wastes clinical time and creates real risk: missed allergies, duplicate prescriptions, and incomplete diagnoses.

A landmark review published in JMIR analyzed **2,100+ studies spanning 25 years** of health IT research. The consistent finding: medical interoperability — the ability to share and use patient data across systems — remains one of healthcare's most persistent failures.

**53 million Americans** are managing complex health administration across multiple providers with no tool built for them.

---

## The Solution

Second Opinion gives patients a simple workflow:

```
┌──────────────┐     ┌──────────────┐     ┌──────────────────┐     ┌──────────────────┐
│   Upload     │     │     OCR      │     │  AI Structuring  │     │  Doctor-Ready     │
│              │ ──► │              │ ──► │                  │ ──► │  Summary          │
│ PDFs, scans, │     │ Extract text │     │ Organize into    │     │                  │
│ photos       │     │ from any doc │     │ clinical timeline│     │ One-pager for     │
│              │     │              │     │                  │     │ any provider      │
└──────────────┘     └──────────────┘     └──────────────────┘     └──────────────────┘
```

**What the patient does:** Upload whatever they have — scanned discharge summaries, photos of prescription labels, PDFs from specialists.

**What the AI does:** OCR reads the documents, extracts clinical data, and organizes everything into a single chronological timeline covering diagnoses, medications, allergies, and lab results.

**What the doctor sees:** A clean, structured one-pager — ready to reference in the first 60 seconds of a visit. No portal access required. No technical setup.

---

## Target Users

**Primary:**
- Chronic disease patients (diabetes, cancer, autoimmune, heart disease) managing care across 3+ providers
- Rare disease patients who spend years repeating their history to new specialists
- Caregivers coordinating records for a parent or dependent child

**Future expansion:**
- Independent clinics and telehealth platforms
- Care coordinators and patient advocates

---

## How It's Different

| Feature | Patient Portals (MyChart) | Mere Medical (FHIR) | Record Services (Ciitizen) | **Second Opinion** |
|---------|--------------------------|----------------------|----------------------------|-------------------|
| Data source | Single hospital network | Connected FHIR portals | Human-curated collection | **Any document — paper, PDF, photo** |
| Cross-system | No | Yes (if FHIR-enabled) | Yes (weeks to compile) | **Yes (instant)** |
| Non-digital records | No | No | Partial | **Yes — OCR handles paper** |
| Output | Raw records display | Timeline (structured) | Organized records | **Doctor-ready summary** |
| Cost | Free (limited) | Free (open-source) | $500+ | **Free / low-cost** |
| Speed | — | Instant (if connected) | Weeks | **Minutes** |
| Patient-controlled | Partially | Yes | Yes | **Yes — patient owns all data** |

**Key differentiator:** Most existing solutions require hospital portals or FHIR API connections. Second Opinion works with whatever the patient already has — including the paper discharge summary from 2019 sitting in a kitchen drawer.

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Document Ingestion | OCR (Tesseract / Cloud Vision API) |
| Clinical Structuring | LLM (GPT-4 / Claude) for entity extraction and summarization |
| Data Model | Chronological clinical timeline (diagnoses, meds, allergies, labs) |
| Language | Python |
| Prototype | Google AI Studio (interactive AI assistant) |
| Frontend (planned) | React / Next.js |

---

## Legal & Compliance

Second Opinion operates in a **favorable regulatory position**:

- **HIPAA:** As a patient-controlled tool, Second Opinion is not a covered entity. The patient uploads their own data at their own direction — no institutional data exchange required.
- **21st Century Cures Act:** Legally requires hospitals to give patients access to their records, supporting the data availability that Second Opinion relies on.
- **HTI-5 (ONC Rule):** Explicitly supports AI-enabled interoperability tools, validating the regulatory pathway for patient-facing AI health tools.

**Design principles:**
- Patient controls all sharing — they choose what to show the doctor
- No raw documents stored longer than the processing window
- Output includes disclaimer: *"AI-generated summary. Please verify with source records before making clinical decisions."*

---

## Validation

- Physician discovery interviews conducted via LinkedIn outreach across primary care, specialist, and emergency medicine physicians
- Patient interviews confirming the pain of re-explaining history at every new visit
- Competitive landscape research (Mere Medical, Ciitizen, Apple Health, MyChart)
- Regulatory feasibility assessment (HIPAA, 21st Century Cures Act, HTI-5)

---

## Project Documentation

- [Pitch Deck](docs/pitch_deck_summary.md) — COZAD competition presentation summary
- [Competitive Analysis](docs/competitive_analysis.md) — Mere Medical, Ciitizen, patient portals
- [Physician Interview Guide](docs/physician_interview_guide.md) — Discovery interview framework

---

## Team

| Name | Role | Focus |
|------|------|-------|
| **Prateek Verma** | Co-founder | Business analytics, AI workflow design, competitive research, pitch strategy |
| **Suyash Sawant** | Co-founder | Product development, technical architecture |

Both are MS Business Analytics students at UIUC Gies College of Business.

---

## Status

- ✅ COZAD 2026 participant
- ✅ Physician discovery interviews completed
- ✅ Competitive landscape mapped
- ✅ Regulatory feasibility validated
- ✅ AI prototype built (Google AI Studio)
- 🔄 Technical prototype in development

---

## Disclaimer

This is an **academic venture competition project** and is not a certified medical device. Second Opinion does not provide medical advice, diagnosis, or treatment. AI-generated summaries should always be verified against original source records by a qualified healthcare professional. No patient data was used in development — all testing uses synthetic documents.

---

## License

MIT License — see [LICENSE](LICENSE) for details.

## Contact

**Prateek Verma** — [GitHub](https://github.com/Prattkk) · [Portfolio](https://quaint-area-0e3.notion.site) · vermaprateek1109@gmail.com
