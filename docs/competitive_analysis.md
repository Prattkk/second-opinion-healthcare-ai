# Competitive Analysis

## Landscape Overview

Second Opinion operates at the intersection of patient health records, AI summarization, and point-of-care tools. The competitive landscape includes patient portals, open-source aggregators, and concierge record services.

---

## Key Competitors

### 1. Mere Medical (Open-Source FHIR Aggregator)

**What it does:** Self-hosted web app that connects to FHIR-enabled patient portals and aggregates records into a timeline view.

**Strengths:** Free, open-source, strong FHIR integration, developer-friendly.

**Limitations:**
- Only works with hospitals that have FHIR APIs enabled
- Cannot process non-digital records (paper, photos, scanned PDFs)
- No AI summarization — displays raw record data
- Requires technical setup (Docker, FHIR sandbox credentials)

**Relationship to Second Opinion:** Complementary, not competitive. Mere Medical could serve as a future data source for Second Opinion's pipeline (structured portal data feeding into our summarization layer). But for patients whose records are not in FHIR portals — which is most patients — Mere cannot help.

### 2. Apple Health

**What it does:** Stores health records synced from connected hospital networks, tracks fitness and vitals data.

**Limitations:**
- Limited to hospitals on Apple's Health Records network
- Displays raw records — no cross-system organization or summary
- No support for non-digital documents

### 3. MyChart (Epic Patient Portal)

**What it does:** Patient-facing portal for Epic-based hospital systems.

**Limitations:**
- Siloed to a single hospital network
- Cannot export, compile, or share across institutions
- No AI structuring or summarization

### 4. Ciitizen (Human-Curated Record Collection)

**What it does:** Concierge service that collects and organizes medical records on behalf of cancer patients.

**Limitations:**
- $500+ cost
- Takes weeks to compile
- Not usable for same-day appointments
- Limited disease focus (primarily oncology)

---

## Second Opinion's Positioning

The key insight: **most fragmented patient records are not in digital portals.** They're in paper discharge summaries, old PDFs emailed from clinics, photos of prescription bottles, and handwritten specialist notes.

Every competitor above requires either a FHIR connection, a specific hospital network, or weeks of human curation. Second Opinion is the only solution designed for **any document, any format, any system — available in minutes, not weeks.**
