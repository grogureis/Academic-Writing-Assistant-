# /clinical-article — Clinical Manuscript Writing (STROBE/IMRAD)

This command activates the Clinical Manuscript Writing Assistant for emergency medicine and clinical research manuscripts. It is a variant workflow that runs independently of the standard article phases.

## When to Use

Use `/clinical-article` when writing:
- Retrospective cohort studies
- Case-control studies
- Cross-sectional analyses
- Prospective cohort studies
- RCTs (switches to CONSORT automatically)
- Any observational clinical study requiring STROBE compliance

Do NOT use for: thesis chapters, book chapters, literature reviews, grant proposals. Use the standard `/tezatlas` workflow for those.

---

## Step 1 — Load the Clinical Writer

At session start, load the clinical writing assistant:

```
Read agents/prompts/clinical_writer.md
```

This file contains the full STROBE-IMRAD protocol, mandatory inputs, banned words list, statistical analysis sequence, and output format.

---

## Step 2 — Collect Mandatory Inputs

Before writing a single word, ask the user for ALL of the following. Do not proceed until every item is answered:

**Study Specifications:**
- Study design (retrospective cohort / case-control / cross-sectional / prospective cohort / RCT)
- Clinical setting and date range (e.g., "ED of tertiary hospital, January 2020 - December 2022")
- Target journal (determines word limits, citation style, subheading format)
- Citation style: AMA (default) / APA 7 / Vancouver
- Language: Turkish / English

**Content Specifications:**
- Research question or hypothesis (exact wording)
- Primary outcome and secondary outcomes
- Key variables: exposure, outcome, covariates, confounders
- Data status: full data collected / outline stage / partial draft exists
- Key sources with DOI/PMID (if available)

---

## Step 3 — Determine Reporting Guideline

Based on study design:

| Design | Guideline |
|--------|-----------|
| Retrospective cohort | STROBE |
| Case-control | STROBE |
| Cross-sectional | STROBE |
| Prospective cohort | STROBE |
| RCT | CONSORT |
| Systematic review / meta-analysis | PRISMA |
| Diagnostic accuracy study | STARD |
| Prediction model | TRIPOD |

---

## Step 4 — Select Phase

Determine what the user needs:

| User's Data Status | Action |
|---|---|
| Full data collected and analyzed | Proceed to full IMRAD writing (Phase 3) |
| Outline stage only | Generate structured outline with placeholders (Phase 1) |
| Partial draft exists | Review existing draft, then complete missing sections (Phase 2) |
| Pre-submission revision needed | Run `/peer-review-clinical` instead |

---

## Phase 0 — Study Design Confirmation

Load: `skills/phases/clinical-article/phase-0-study-design.md`

Confirm:
- Study design is explicitly named
- Reporting guideline is selected
- STROBE or applicable checklist items are mapped to IMRAD sections

**Gate:** Do not write any manuscript content until study design and reporting guideline are confirmed.

---

## Phase 1 — Literature Search

Load: `skills/phases/clinical-article/phase-1-literature.md`

Run literature searches BEFORE writing Introduction or Discussion:
- Use web_search for all reference retrieval
- Never cite from memory
- Mark unfound references as [CITATION NEEDED: topic]

**Gate:** At least 10 references identified before writing Introduction.

---

## Phase 2 — Manuscript Writing (IMRAD)

Load: `skills/phases/clinical-article/phase-2-writing.md`

Follow the STROBE-IMRAD writing sequence from `agents/prompts/clinical_writer.md`:

Write in this order:
1. Methods (study design → participants → variables → bias → stats → outcomes)
2. Results (participant flow → descriptive → univariate → ROC → multivariate)
3. Discussion (main finding → clinical significance → literature comparison → mechanism → limitations → generalizability)
4. Introduction (background → knowledge gap → study objective)
5. Abstract (write last, present first)
6. Title

**Gate:** All STROBE items 1-22 checked before proceeding to revision.

---

## Phase 3 — Pre-Submission Revision

Load: `skills/phases/clinical-article/phase-3-revision.md`

Run pre-submission checklist from `agents/prompts/clinical_writer.md`:
- All [CITATION NEEDED] markers resolved
- All references verified with DOI/PMID
- Effect sizes reported with 95% CI
- Missing data protocol applied
- ROC analysis positioned correctly (after univariate, before multivariate)
- No banned words in manuscript text
- Tables formatted per target journal

**Gate:** All checklist items confirmed before declaring submission-ready.

---

## Output Format

All manuscript output follows this structure:

```
=== LITERATURE SEARCH SUMMARY ===
Searches conducted: [n]
Key sources identified: [list with PMID/DOI]
Flagged for author verification: [CITATION NEEDED markers]

=== STROBE COMPLIANCE CHECK ===
Items addressed: [list item numbers]
Items requiring author input: [list item numbers with explanation]

=== FULL MANUSCRIPT ===
[Title]
[Abstract]
[Introduction]
[Methods]
[Results]
[Discussion]
[Conclusion]

REFERENCES
[AMA-formatted numbered list]

NOTES FOR AUTHOR
- TABLE/FIGURE placeholders: replace with actual data
- [CITATION NEEDED] markers: verify before submission
- Methodological flags: [if any]
- STROBE items needing author verification: [list]
```

---

## Related Commands

- `/peer-review-clinical` — peer review a completed clinical manuscript
- `/submission-check` — standard pre-submission checklist
- `/citation-check` — verify a claim against a PDF source
- `/method-audit` — audit research methodology
