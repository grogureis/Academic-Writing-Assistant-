---
title: "Clinical Article — Phase 0: Study Design and Reporting Guideline"
phase: 0
outputs:
  - study_design_brief.md
phase_gate_out: "phase-1-literature.md"
---

## Purpose

Confirm the study design, select the appropriate reporting guideline, and map STROBE (or applicable checklist) items to the IMRAD sections before any writing begins.

## Gate Rule

Do NOT proceed to Phase 1 until all items in this phase are confirmed in writing.

---

## Step 1 — Name the Study Design

State the exact design. Use the controlled vocabulary below. Do not use informal descriptions.

| Accepted Terms |
|---|
| Retrospective cohort study |
| Prospective cohort study |
| Case-control study |
| Cross-sectional study |
| Randomized controlled trial (RCT) |
| Systematic review and meta-analysis |
| Diagnostic accuracy study |
| Prediction model development / validation study |

**Output:** One sentence, e.g., "This is a retrospective cohort study."

---

## Step 2 — Select Reporting Guideline

| Study Design | Guideline | Extensions to Check |
|---|---|---|
| Cohort / case-control / cross-sectional | STROBE | RECORD (if registry/claims data) |
| RCT | CONSORT | CONSORT-AI (if AI intervention) |
| Systematic review / meta-analysis | PRISMA 2020 | PRISMA-NMA, PRISMA-IPD, PRISMA-ScR |
| Diagnostic accuracy | STARD | STARD-AI (if AI model) |
| Prediction model | TRIPOD | TRIPOD-AI (if ML/AI model) |

**Output:** "This study will be reported in accordance with [GUIDELINE] guidelines."

---

## Step 3 — Map Checklist Items to IMRAD Sections

For STROBE (most common in clinical-article workflow):

| IMRAD Section | STROBE Items |
|---|---|
| Title and Abstract | Item 1 |
| Introduction | Items 2-3 |
| Methods | Items 4-12 |
| Results | Items 13-17 |
| Discussion | Items 18-21 |
| Other Information | Item 22 |

Record which items require author-supplied data (ethics number, sample size rationale, funding source).

---

## Step 4 — Confirm Mandatory Inputs

Check that ALL of the following are available before proceeding:

- [ ] Study design named (controlled vocabulary)
- [ ] Clinical setting and date range specified
- [ ] Target journal identified
- [ ] Citation style selected (AMA default)
- [ ] Language confirmed (English / Turkish)
- [ ] Research question or hypothesis stated (exact wording)
- [ ] Primary outcome defined
- [ ] Secondary outcomes listed (if any)
- [ ] Key variables identified: exposure, outcome, covariates, confounders
- [ ] Data status confirmed (full data / outline / partial draft)

**If any item above is missing: ASK before proceeding. Do not write manuscript content.**

---

## Output

Create `study_design_brief.md` with:

```
STUDY DESIGN: [exact term]
REPORTING GUIDELINE: [STROBE / CONSORT / PRISMA / STARD / TRIPOD]
EXTENSIONS: [if applicable, or "None"]
CLINICAL SETTING: [institution type, location]
DATE RANGE: [start – end]
TARGET JOURNAL: [journal name]
CITATION STYLE: [AMA / APA 7 / Vancouver]
LANGUAGE: [English / Turkish]
RESEARCH QUESTION: [exact wording]
PRIMARY OUTCOME: [definition + measurement method + timing]
SECONDARY OUTCOMES: [list or "None"]
KEY VARIABLES: [exposure, covariates, confounders]
DATA STATUS: [full / outline / partial draft]
ETHICS APPROVAL: [number or "Pending"]
MISSING INPUTS: [list any items still needed]
```

---

## Phase Gate

Proceed to Phase 1 (Literature Search) only when `study_design_brief.md` is complete and all mandatory inputs are confirmed.
