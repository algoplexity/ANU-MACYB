# Research Data Management Plan (RDMP) — MACYB v1
**Date:** 2026-02-28  
**Owner:** algoplexity (personal project)  
**Core tools (fixed for v1):** GitHub (2 repos), Google Drive or ANU OneDrive (“Drive”), Zotero  
**Repositories:**
- **Private working repo:** `ANU-MACYB-private` (GitHub private)
- **Public curated repo + comms:** `ANU-MACYB-public` (GitHub public) + **GitHub Pages project site** (served from `/docs`)

**Implementation principles (anti-scope-creep):**
- Every artefact has exactly one **authoritative location** (“system of record”).
- Everything starts **private-first**; publication is **optional** and requires sanitization.
- No Git LFS, no GitLab mirrors, no additional platforms in v1.

---

## 1) Data Collection

### 1.1 What data will you collect or create?
This project will create and/or collect the following categories of material:

1. **Reflective writing (drafts and finals)**
   - Drafts in Markdown
   - Final submitted versions in PDF/Doc

2. **Assignment outputs (reports and supporting artefacts)**
   - Draft reports in Markdown
   - Final submitted reports in PDF/Doc
   - Supporting figures/diagrams used in reports (where appropriate)

3. **Cyber-Physical Systems (CPS) project artefacts** (at least two projects: individual then group)
   - Source code (e.g., firmware, scripts, analysis code)
   - Technical documentation (architecture notes, procedures, decision logs)
   - Hardware design files (e.g., schematics, CAD exports as applicable)
   - Experimental inputs and outputs (measurements, logs, derived results)
   - Media captured during build/testing (photos/video as applicable)

4. **Literature and reference materials**
   - Bibliographic metadata, notes, PDFs/links in Zotero

5. **Policies/procedures/regulatory notes (as they arise)**
   - Lightweight notes and checklists relevant to how the work is conducted and documented

### 1.2 How will the data be collected or created?
- **Writing and reports:** Authored as Markdown in `ANU-MACYB-private`, then exported to PDF/Doc for submission and stored in Drive.
- **Code and technical docs:** Developed and versioned in GitHub (private first). Public release (if any) is promoted to `ANU-MACYB-public`.
- **CPS data/logs/results:** Collected from devices, experiments, and scripts; stored either in GitHub (small, non-sensitive, text-based) or in Drive (large/binary/raw exports).
- **Hardware design files:** Created with appropriate design tools and stored in GitHub if reasonably small; otherwise stored in Drive with a pointer/manifest in GitHub.
- **References:** Added to Zotero as they are found/used, with consistent metadata and tagging.

---

## 2) Documentation and Metadata

### 2.1 What documentation and metadata will accompany the data?
To keep the plan implementable, documentation is lightweight and consistent:

**A. Repository-level documentation**
- Each GitHub repo contains a `README.md` describing:
  - what is included/excluded,
  - privacy/publication rules,
  - how to navigate the structure.

**B. Project-level documentation**
- Each CPS project folder includes:
  - `README.md` (scope, how to run/build, key outputs)
  - `decision-log.md` (sanitized summary of major design/measurement decisions and rationale)
  - `CHANGELOG.md` (optional; only if it stays useful)

**C. Drive folder metadata**
- Each Drive folder that contains important finals or datasets includes a small metadata file (any of):
  - `submission-metadata.txt` for assignment/reflection finals (date, title, what it is)
  - `metadata.md` for datasets/exports (purpose, format, creation method, and relationship to GitHub)

**D. Cross-linking (GitHub ↔ Drive)**
- When Drive holds the authoritative large/binary artefacts, GitHub contains a short manifest file, e.g.:
  - `projects/<project>/manifests/drive-manifest.md`
  describing what exists in Drive and how it relates to code/analysis (without exposing sensitive links if not appropriate).

**E. Zotero metadata**
- Each Zotero entry should include, where available:
  - author(s), year, title, venue
  - DOI/URL
  - tags/keywords aligned to course/project themes
  - brief notes summarizing relevance

---

## 3) Ethics and Legal Compliance

### 3.1 How will you manage any ethical issues?
- **Default posture:** treat drafts, reflections, and assessment-related artefacts as **private-first**.
- **Sensitive content controls:**
  - Any content that is personal, sensitive, or otherwise not intended for public release remains in `ANU-MACYB-private` and/or restricted Drive folders.
  - Only sanitized, non-sensitive content is promoted to `ANU-MACYB-public` and GitHub Pages.
- **Human data:** If any CPS activity expands to involve human participants or identifiable personal data, data collection and storage will be updated to align with applicable ethics requirements and approvals (if required), and public sharing will be restricted accordingly.

### 3.2 How will you manage copyright and Intellectual Property Rights issues?
- **Third-party materials:**
  - Do not commit copyrighted PDFs or restricted course materials into public repositories.
  - In public content, prefer citations/links to the source rather than redistribution.
- **Your authored content:**
  - Drafts and working documents remain private by default.
  - Public release is intentional: only materials you have the rights to share are published in `ANU-MACYB-public`/Pages.
- **Group project considerations:**
  - For the group CPS project, only publish material in the public repo that is clearly agreed to be shareable and does not conflict with teammate expectations or any course rules.

---

## 4) Storage and Backup

### 4.1 How will the data be stored and backed up during the research?
**Authoritative locations (systems of record):**
- **Zotero:** authoritative for references (metadata + notes + PDFs/links)
- **GitHub (`ANU-MACYB-private`):** authoritative for working drafts (Markdown) and working code/docs
- **Drive/OneDrive:** authoritative for final submissions (PDF/Doc) and for large/binary artefacts (media, exports)

**Backup posture (KISS):**
- GitHub provides version history and remote redundancy for text/code.
- Drive/OneDrive provides cloud sync and redundancy for final PDFs/Docs and binaries.
- Optional: periodic export of Zotero library to Drive for portability/recovery.

### 4.2 How will you manage access and security?
- **Access control:**
  - `ANU-MACYB-private` remains private.
  - Drive/OneDrive folders default to restricted access.
  - `ANU-MACYB-public` and GitHub Pages contain only sanitized/public-safe content.
- **Secret management:**
  - No credentials, API keys, or tokens are stored in public repos or Pages.
  - If secrets are needed for CPS development, they are stored outside GitHub and referenced via local configuration that is not committed.
- **Release gate:**
  - Publication to public repo/Pages requires a quick check: no personal/sensitive data, no restricted assessment artefacts, no copyrighted redistributions.

---

## 5) Selection and Preservation

### 5.1 Which data are of long-term value and should be retained, shared, and/or preserved?
**Retain long-term (high value):**
- Final submitted assignment/reflection PDFs/Docs (Drive)
- Key CPS source code and technical documentation (GitHub private; and public if shareable)
- Key derived results (figures/tables) that support conclusions or assessment outcomes
- Decision logs / rationale summaries that explain major design choices
- Zotero library (metadata/notes)

**Retain short-term or archive (lower value):**
- Low-signal drafts and intermediate exports that do not add provenance value
- Large raw media not needed for reporting (unless required for evidence/provenance)

### 5.2 What is the long-term preservation plan for the dataset?
- **Final submissions:** preserved as PDF/Doc in Drive/OneDrive as the canonical record.
- **Working history:** preserved in GitHub via commit history and tags where appropriate.
- **Public knowledge base:** selected sanitized documentation and progress posts preserved via GitHub Pages (from `ANU-MACYB-public/docs`).
- **References:** preserved in Zotero, with optional periodic exports stored in Drive.

This v1 plan intentionally avoids formal archival repositories/DOIs unless they become necessary later.

---

## 6) Data Sharing

### 6.1 How will you share the data?
- **Primary sharing mechanism:** `ANU-MACYB-public` GitHub repository.
- **External communication:** GitHub Pages project site (served from `ANU-MACYB-public/docs`) for blog-style updates and shareable documentation.
- **What is shared:**
  - sanitized procedures, architecture notes, selected results summaries
  - code that is appropriate to release
  - small, non-sensitive sample datasets if needed for demonstration/reproducibility

### 6.2 Are any restrictions on data sharing required?
Yes, restrictions apply by default:
- Reflective writing originals and assessment artefacts (drafts and finals) are **not** publicly shared unless explicitly permitted and sanitized.
- Any sensitive information, personal data, or restricted content remains private (GitHub private repo + restricted Drive).
- Large raw datasets and binaries are not shared publicly by default; public repo may include non-sensitive samples or high-level summaries.

---

## 7) Responsibilities and Resources

### 7.1 Who will be responsible for data management?
- **Single responsible person:** algoplexity (project owner)
- Responsibilities include:
  - maintaining repo structure and commit discipline,
  - exporting and filing final PDFs/Docs to Drive,
  - sanitizing and promoting content to the public repo/Pages where appropriate,
  - maintaining Zotero metadata hygiene (tags, notes, citation completeness).

### 7.2 What resources will you require to deliver your plan?
Minimal required resources:
- GitHub account with two repositories (one private, one public)
- Drive/OneDrive storage sufficient for PDFs/Docs and binaries (media, exports)
- Zotero installation and syncing configuration

Optional resources (not required for v1, only if needed later):
- additional storage capacity for large CPS media/exports
- a DOI/archive workflow (e.g., Zenodo) if publication/dissemination requirements emerge
