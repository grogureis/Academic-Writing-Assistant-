---
title: "Clinical Article — Phase 1: Literature Search"
phase: 1
outputs:
  - literature_brief.md
  - references.md
phase_gate_out: "phase-2-writing.md"
---

## Purpose

Collect, verify, and organize the references needed for Introduction, Methods, and Discussion BEFORE any manuscript writing begins.

## Gate Rule

Do NOT begin writing Introduction or Discussion until at least 10 verified references are collected and recorded in `references.md`.

---

## Search Protocol

Run all searches using web_search. Never cite from memory. Never fabricate references.

### Introduction Searches (run before writing Introduction)

| Target | Search Query Template |
|---|---|
| Epidemiology / disease burden | "[condition] incidence prevalence [year range]" |
| Mortality / morbidity | "[condition] mortality outcomes [year range]" |
| Pathophysiology | "[biomarker/mechanism] pathophysiology [condition]" |
| Current standard of care | "[condition] clinical guidelines [society name] [year]" |
| Evidence gaps | "[topic] systematic review meta-analysis [year range]" |

Sources to prioritize: WHO reports, national registries, AHA/ESC/ERC/SCCM/ACEP guidelines, Cochrane reviews, recent meta-analyses.

### Methods Searches (run before writing Methods)

| Target | Search Query Template |
|---|---|
| Validated scoring tools | "[score name] original validation study" |
| Score reliability | "[score name] reliability emergency department" |
| Statistical method justification | "[analysis method] observational study" |
| Reporting guideline | "STROBE cohort study reporting guidelines" |

### Discussion Searches (run before writing Discussion)

| Target | Search Query Template |
|---|---|
| Supporting studies | "[main finding] [condition] cohort outcomes" |
| Contradictory studies | "[alternative finding] [condition] [study design]" |
| Null-result studies | "[variable] no association [condition]" |
| Mechanistic explanation | "[biomarker/variable] mechanism pathophysiology [condition]" |
| Clinical implications | "[finding] clinical practice recommendations [year]" |

---

## Search Execution Rules

1. Run searches BEFORE writing each major section, not after
2. Prioritize: peer-reviewed journals > clinical guidelines > systematic reviews > meta-analyses
3. Prefer last 5 years for clinical data; seminal papers may be older
4. Synthesize: group 3-5 citations per claim, never cite sequentially
5. Actively search for null-result studies to reduce citation bias
6. If a reference cannot be confirmed: mark [CITATION NEEDED: specific topic]

---

## Reference Counts by Section

| Section | Target Reference Count |
|---|---|
| Introduction | 10-12 |
| Methods | 3-5 (tool validations + statistical citations) |
| Discussion | 10-15 |
| Total | 23-32 |

---

## Output: references.md

Create `references.md` with the following structure for each source:

```
[#]. Author AA, Author BB, Author CC. Title of article. Journal Name. Year;Vol(Issue):Pages. doi:XXXXX PMID:XXXXX

Section: [Introduction / Methods / Discussion]
Claim supported: [one sentence describing what this reference supports]
Verified via: [web_search / user-provided / CITATION NEEDED]
```

---

## Output: literature_brief.md

After search completion, create `literature_brief.md`:

```
LITERATURE SEARCH SUMMARY
Searches conducted: [n]
Total references collected: [n]

Introduction references: [n] (target: 10-12)
Methods references: [n] (target: 3-5)
Discussion references: [n] (target: 10-15)

Key sources:
- [PMID/DOI]: [one-line summary of relevance]
- [PMID/DOI]: [one-line summary]

Contradictory studies found: [yes/no — list if yes]
Null-result studies found: [yes/no — list if yes]

Unresolved markers: [list all CITATION NEEDED items]

Seminal references (exempt from recency requirement):
- [list landmark studies, original scale validations, foundational guidelines]
```

---

## Phase Gate

Proceed to Phase 2 (Manuscript Writing) only when:
- [ ] At least 10 references verified for Introduction
- [ ] Methods tool validation references identified
- [ ] At least 5 Discussion references found
- [ ] Contradictory / null-result studies searched
- [ ] `references.md` and `literature_brief.md` created
