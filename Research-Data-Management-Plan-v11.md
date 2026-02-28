# RDMP — MACYB v1 **Implementation Guide**
**Date:** 2026-02-28  
**Owner:** algoplexity  
**Core tools:** GitHub (2 repos), Google Drive or ANU OneDrive (“Drive”), Zotero  
**Repos:**
- GitHub private: `ANU-MACYB-private`
- GitHub public: `ANU-MACYB-public` (also hosts GitHub Pages **project site** from `/docs`)

**Non-goals (v1):** Git LFS, GitLab mirrors, DOIs/Zenodo, CI/CD pipelines, additional repos.

---

## 0) One-page rules (print this)
### Systems of record (authoritative)
- **Zotero**: references (metadata + notes + PDFs/links)
- **GitHub private**: *working* Markdown drafts + working code/docs
- **Drive**: *final submitted* PDF/Doc + feedback + large/binary artefacts
- **GitHub public + Pages**: sanitized, shareable subset only

### The only workflow you use
1. Draft in `ANU-MACYB-private` (Markdown)
2. Export final to PDF/Doc → store in Drive (**authoritative**)
3. Optionally sanitize + publish to `ANU-MACYB-public` and/or Pages

---

## 1) GitHub folder structures (exact)

### 1.1 `ANU-MACYB-private` (private working repo)
Create this structure and keep it stable:

```
ANU-MACYB-private/
  README.md
  admin/
    MASTER_IMPLEMENTATION_PLAN.md
    policies/
    templates/
  reflections/
    2026/
      2026-02-28-example-reflection/
        draft.md
        notes.md
        export-notes.md
  assignments/
    2026/
      COURSE-CODE/
        A01-title/
          draft.md
          figures/
          export-notes.md
  projects/
    cps1-individual/
      README.md
      decision-log.md
      src/
      docs/
      data/
        samples/
      manifests/
        drive-manifest.md
    cps2-group/
      README.md
      decision-log.md
      src/
      docs/
      data/
        samples/
      manifests/
        drive-manifest.md
  comms/
    blog-drafts/
      2026-02-28-post-title.md
  archive/
```

**Notes**
- `export-notes.md` is a lightweight checklist: what to export, where the final went in Drive, and the final file name.
- `manifests/drive-manifest.md` is where you list “the real data is in Drive at …” without putting sensitive links in public.

---

### 1.2 `ANU-MACYB-public` (public curated repo + Pages)
Create this structure:

```
ANU-MACYB-public/
  README.md
  LICENSE            # optional, but recommended if you publish code
  docs/              # GitHub Pages root
    index.md
    blog/
      2026-02-28-post-title.md
    pages/
      about.md
      methods.md
    assets/
      images/
  projects/
    cps1-individual/
      README.md
      src/
      docs/
      data/
        samples/
    cps2-group/
      README.md
      src/
      docs/
      data/
        samples/
```

**GitHub Pages setting**
- Configure Pages to build from: **`main` branch** + **`/docs` folder**.

---

## 2) Drive folder structure (exact)
Create a top-level folder `ANU-MACYB/` and mirror categories:

```
ANU-MACYB/
  00_admin/
    policies/
    templates/
  01_reflections/
    2026/
      2026-02-28-example-reflection/
        final.pdf
        submission-metadata.txt
  02_assignments/
    2026/
      COURSE-CODE/
        A01-title/
          final.pdf
          rubric-feedback.pdf
          submission-metadata.txt
  03_projects/
    cps1-individual/
      inputs/
      raw/
      outputs/
      media/
      hardware/
      exports/
      metadata.md
    cps2-group/
      inputs/
      raw/
      outputs/
      media/
      hardware/
      exports/
      metadata.md
  99_archive/
```

**Drive metadata files**
- `submission-metadata.txt` (final reflections/assignments)
- `metadata.md` (projects/datasets/exports)

---

## 3) Zotero (how-to)
### 3.1 Collections
Create collections:
- `MACYB`
  - `CPS1-individual`
  - `CPS2-group`
  - `Coursework` (optional)
  - `Methods` (optional)

### 3.2 Required fields (minimum)
For each Zotero item, ensure:
- Title, author(s), year
- DOI/URL if available
- Tags (at least 1–3)
- 1–3 sentence note: “Why is this relevant?”

### 3.3 Optional resilience
Monthly (or end-of-semester):
- Export Zotero library (and/or Better BibTeX) to `Drive/ANU-MACYB/00_admin/`.

---

## 4) “How-to” by asset type (step-by-step)

## 4.1 Reflective writing
### Where it lives
- Drafts: `ANU-MACYB-private/reflections/<year>/<YYYY-MM-DD-title>/draft.md`
- Final submission (authoritative): `Drive/ANU-MACYB/01_reflections/<year>/<YYYY-MM-DD-title>/final.pdf`

### How-to workflow
1. Create folder in private repo:
   - `reflections/2026/2026-03-01-reflection-topic/`
2. Write `draft.md` (and optionally `notes.md`).
3. When ready to submit:
   - Export to PDF/Doc (course-required format).
   - Save to Drive as `final.pdf` (or course naming).
4. Create/update `export-notes.md` in the same private folder:
   - Include export date, Drive path, and final filename.
5. Optional: create a sanitized excerpt for public (rare):
   - Copy to `ANU-MACYB-public/docs/pages/` only if appropriate.

**Hard rule:** final submitted reflection lives in Drive; GitHub contains drafts only.

---

## 4.2 Assignment reports (primary deliverable is PDF/Doc)
### Where it lives
- Draft: `ANU-MACYB-private/assignments/<year>/<COURSE>/<Axx-title>/draft.md`
- Final: `Drive/ANU-MACYB/02_assignments/<year>/<COURSE>/<Axx-title>/final.pdf`
- Feedback: same Drive folder, e.g. `rubric-feedback.pdf`

### How-to workflow
1. Create private assignment folder.
2. Write draft in Markdown; put small figures in `figures/`.
3. Export final to PDF/Doc.
4. Store final and any returned feedback in Drive.
5. Update `export-notes.md` in GitHub private with:
   - export date
   - Drive location
   - the commit hash used to generate the final (optional)

---

## 4.3 CPS project code & documentation
### Where it lives
- Working code/docs: `ANU-MACYB-private/projects/<project>/`
- Public release (if shareable): `ANU-MACYB-public/projects/<project>/`

### How-to workflow (private-first)
1. Develop in private:
   - code in `src/`
   - docs in `docs/`
   - decision rationale in `decision-log.md`
2. Commit regularly with meaningful messages.
3. If you generate large outputs (logs, exports, videos):
   - put them in Drive under `03_projects/<project>/...`
   - add an entry to `manifests/drive-manifest.md` describing:
     - what it is
     - when created
     - which script produced it
     - what folder in Drive holds it (path only; avoid sensitive links)

### Promotion to public (only when safe)
1. Copy only the publishable subset (code + sanitized docs).
2. Ensure no secrets, no restricted content, no sensitive raw data.
3. Add a note in public `README.md` stating:
   - what is intentionally not included and where it is stored (Drive/private).

---

## 4.4 CPS project data (inputs/outputs)
### Storage decision rule
- Small, non-sensitive, text-based **sample data** may go in GitHub (`data/samples/`).
- Anything raw/large/binary goes in Drive.

### How-to workflow
1. Store raw/exports in Drive:
   - `Drive/ANU-MACYB/03_projects/<project>/raw/` and `exports/`
2. Store derived results (figures/tables) in:
   - Drive `outputs/` (authoritative if used in final submissions)
3. In GitHub private, document:
   - how to reproduce (script + parameters)
   - file naming scheme
   - pointer to Drive location via `manifests/drive-manifest.md`

---

## 4.5 Hardware design files (schematics/CAD)
### Default (v1, no LFS)
- If files are small and diff-insensitive: you may keep them in GitHub private under:
  - `projects/<project>/docs/` or `projects/<project>/hardware/` (create if needed)
- If they become large or numerous:
  - store authoritative versions in Drive under:
    - `Drive/.../03_projects/<project>/hardware/`
  - keep only a README + exported images in GitHub for understanding.

### How-to workflow
1. Decide “GitHub vs Drive” based on size/volume.
2. Always include a short README describing:
   - tool/version used (e.g., KiCad version)
   - export steps if any
   - relationship to the build/BOM

---

## 4.6 Blogs / external communication (GitHub Pages project site)
### Where it lives
- Draft posts: `ANU-MACYB-private/comms/blog-drafts/YYYY-MM-DD-title.md`
- Published posts: `ANU-MACYB-public/docs/blog/YYYY-MM-DD-title.md`

### How-to workflow
1. Write post draft privately.
2. Sanitize:
   - remove private context, assessment-only details, personal reflections, restricted artefacts
   - remove any sensitive data or identifiers
3. Copy to public repo under `docs/blog/`.
4. Commit and push; Pages updates automatically.

---

## 5) Access/security checklist (use before publishing anything)
Before moving anything to `ANU-MACYB-public` or `docs/` (Pages), confirm:
- [ ] No secrets/tokens/passwords
- [ ] No personal/sensitive reflection content
- [ ] No restricted course submission artefacts (final PDFs/Docs remain in Drive)
- [ ] No copyrighted redistribution (e.g., PDFs you don’t own the rights to)
- [ ] Group-project materials are explicitly shareable

---

## 6) What changes require updating this plan?
Update this file (and record a dated note in `ANU-MACYB-private/admin/MASTER_IMPLEMENTATION_PLAN.md`) if you decide to add:
- Git LFS
- additional repos
- new storage systems (Zenodo/OSF/etc.)
- formal retention rules beyond “per applicable requirements”
- automated CI/pipelines

(Otherwise: keep using the workflow as written.)
