---
title: "Clinical Article — Phase 3: Pre-Submission Revision"
phase: 3
outputs:
  - submission_checklist.md
  - manuscript_final.md
phase_gate_out: null
---

## Purpose

Perform the final pre-submission review to confirm STROBE compliance, resolve all markers, verify references, and confirm the manuscript is ready for journal submission.

## Prerequisite

`manuscript_draft.md` must exist and Phase 2 gate must be passed.

---

## Layer 1 — STROBE Compliance Audit

Check every STROBE item against the draft. Report status for each.

| Item | Section | Status | Action Required |
|---|---|---|---|
| 1 | Title + Abstract | | |
| 2 | Introduction P1-P2 | | |
| 3 | Introduction P3 | | |
| 4 | Methods: Design | | |
| 5 | Methods: Setting | | |
| 6 | Methods: Participants | | |
| 7 | Methods: Variables | | |
| 8 | Methods: Data Sources | | |
| 9 | Methods: Bias | | |
| 10 | Methods: Study Size | | |
| 11 | Methods: Quantitative Variables | | |
| 12 | Methods: Statistical Analysis | | |
| 13 | Results: Participant Flow | | |
| 14 | Results: Descriptive Data | | |
| 15 | Results: Outcome Data | | |
| 16 | Results: Main Results | | |
| 17 | Results: Other Analyses | | |
| 18 | Discussion: Key Results | | |
| 19 | Discussion: Limitations | | |
| 20 | Discussion: Interpretation | | |
| 21 | Discussion: Generalizability | | |
| 22 | Other: Funding | | |

---

## Layer 2 — Citation and Reference Audit

- [ ] All [CITATION NEEDED] markers resolved or escalated to author
- [ ] All references verified with DOI or PMID
- [ ] No references cited from memory without verification
- [ ] Reference count per section within targets (Introduction: 10-12, Methods: 3-5, Discussion: 10-15)
- [ ] AMA format applied consistently: Author AA. Title. Journal. Year;Vol(Issue):Pages. doi:XXXXX
- [ ] No predatory or non-indexed journals cited
- [ ] References current (flag if >10 years for non-seminal claims)

---

## Layer 3 — Statistical Reporting Audit

- [ ] Effect sizes reported with 95% CI for all primary and secondary outcomes
- [ ] p-values reported to three decimal places (p = 0.023) unless p < 0.001
- [ ] ROC analysis positioned: after univariate, before multivariate
- [ ] ROC analysis complete: AUC (95% CI), cutoff, sensitivity, specificity, PPV, NPV, LR+, LR-
- [ ] Multivariate model includes: adjusted OR (95% CI), p-value, Hosmer-Lemeshow, Nagelkerke R-squared
- [ ] Missing data rate reported per variable
- [ ] Missing data protocol applied: < 5% complete case / 5-20% imputation preferred / > 20% imputation mandatory
- [ ] Subgroup analyses labeled as pre-specified or exploratory
- [ ] Sensitivity analyses described and results stated

---

## Layer 4 — Language Audit

- [ ] No banned words (scan against full banned list in `agents/prompts/clinical_writer.md`)
- [ ] No em dash characters (replace with comma, semicolon, colon, or parentheses)
- [ ] No "we" as subject (replaced with "this study" or "the present study")
- [ ] No "first, secondly, thirdly" in Limitations section
- [ ] No causal claims in observational study (flag any "X caused Y" language)
- [ ] Methods and Results in past tense
- [ ] Discussion interpretation in present tense
- [ ] No overclaiming in Conclusion

---

## Layer 5 — Administrative Completeness

- [ ] Ethics approval number included in Methods
- [ ] Conflict of interest statement included
- [ ] Author contributions statement (CRediT taxonomy if journal requires)
- [ ] Funding / grant information included
- [ ] Data availability statement (if required by target journal)
- [ ] Word count within journal limits per section
- [ ] Tables formatted per target journal style guide (no vertical lines, three horizontal lines only)
- [ ] Abbreviations defined in every table footnote
- [ ] All TABLE and FIGURE placeholders marked for author replacement

---

## Submission Checklist Output

Create `submission_checklist.md`:

```
PRE-SUBMISSION CHECKLIST — [Manuscript Title]
Target Journal: [journal name]
Date: [date]

STROBE COMPLIANCE
[ ] Items 1-22 addressed or flagged: [list any flagged items]

CITATIONS
[ ] All CITATION NEEDED markers resolved: [list unresolved]
[ ] All references have DOI/PMID: [list missing]
[ ] References verified via web_search: [confirmed]

STATISTICS
[ ] Effect sizes + 95% CI for all outcomes: [confirmed]
[ ] ROC positioned correctly: [confirmed]
[ ] Missing data protocol applied: [rate per variable]

LANGUAGE
[ ] No banned words: [confirmed / list any found]
[ ] No em dashes: [confirmed]
[ ] No causal claims: [confirmed]

ADMINISTRATIVE
[ ] Ethics approval number: [number or MISSING]
[ ] Conflict of interest: [confirmed or MISSING]
[ ] Author contributions: [confirmed or MISSING]
[ ] Funding statement: [confirmed or MISSING]
[ ] Data availability: [confirmed / not required]

OUTSTANDING ITEMS FOR AUTHOR
[List all items requiring author action before submission]

STATUS: READY FOR SUBMISSION / ITEMS PENDING
```

---

## Phase Gate

This is the final phase. The manuscript is submission-ready when:
- [ ] All STROBE items addressed (or explicitly flagged for author)
- [ ] All [CITATION NEEDED] markers resolved
- [ ] No banned words
- [ ] All effect sizes with 95% CI
- [ ] `submission_checklist.md` created and signed off
- [ ] `manuscript_final.md` produced (clean version without placeholder notes)
