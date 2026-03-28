# /peer-review-clinical — Clinical Manuscript Peer Review

This command activates the Peer Review Assistant (v2.1) for evaluating clinical research manuscripts against ICMJE, COPE, EQUATOR, and reporting guideline standards.

## When to Use

Use `/peer-review-clinical` when:
- Reviewing a completed clinical manuscript before submission
- Performing a statistical audit of methods and results
- Checking compliance against STROBE, CONSORT, PRISMA, STARD, or TRIPOD
- Drafting point-by-point responses to reviewer comments
- Performing a quality/risk-of-bias assessment

---

## Step 1 — Load the Peer Reviewer

```
Read agents/prompts/peer_reviewer.md
```

This file contains the full review protocol, domain checklist, decision criteria, tone rules, and revision module.

---

## Step 2 — Input Triage

Execute in order, stop at first match:

1. **No manuscript submitted** → Ask for manuscript text. Stop.
2. **User specifies a mode** → Run that mode (see Interaction Modes below).
3. **Text < 500 words + section label** → Run partial review of named section only. State which domains cannot be evaluated.
4. **Text < 500 words + no label + no mode** → Ask user to specify mode and confirm study design.
5. **Text >= 500 words + no mode** → Run Full Review automatically.

---

## Interaction Modes

Select the mode that matches what the user needs:

| Mode | What It Does |
|------|-------------|
| `full review` | Complete evaluation: all 8 domains + checklist compliance + editorial decision |
| `methods review` | Study design, population, sample size, variables, statistics only |
| `statistical audit` | Deep review of all statistical decisions (Appendix B cross-reference) |
| `checklist audit` | Full reporting checklist compliance table — ALL items reported |
| `quality assessment` | Risk-of-bias tool (RoB 2, ROBINS-I, AMSTAR 2, QUADAS-2, PROBAST) |
| `response to reviewers` | Draft point-by-point responses to reviewer comments |
| `pre-submission check` | Top 5 rejection reasons for the named target journal |

---

## Step 3 — Identify Study Design and Select Checklist

| Study Design | Primary Checklist | Quality Tool |
|---|---|---|
| Retrospective / prospective cohort | STROBE | ROBINS-I |
| Case-control | STROBE | ROBINS-I |
| Cross-sectional | STROBE | N/A |
| RCT | CONSORT | RoB 2 |
| Systematic review / meta-analysis | PRISMA 2020 | AMSTAR 2 |
| Diagnostic accuracy | STARD | QUADAS-2 |
| Prediction model | TRIPOD | PROBAST |

Check for niche extensions (CONSORT-AI, TRIPOD-AI, RECORD-PE, PRISMA-NMA, etc.) per the Niche Guideline Lookup Protocol in `agents/prompts/peer_reviewer.md`.

---

## Step 4 — Run Review

Follow the output structure from `agents/prompts/peer_reviewer.md`:

```
MANUSCRIPT IDENTIFICATION
DOMAIN REVIEW (Domains 1-8)
REPORTING CHECKLIST COMPLIANCE (table)
QUALITY ASSESSMENT (if applicable)
MAJOR CONCERNS (numbered)
MINOR CONCERNS (numbered)
EDITORIAL DECISION
```

---

## Review Domains Summary

| Domain | What Is Checked |
|--------|----------------|
| 1. Title and Abstract | Design in title, structured abstract, effect sizes with CIs |
| 2. Introduction | Literature gap, rationale, single testable hypothesis |
| 3. Methods | Design, population, sample size, variables, statistics, ethics |
| 4. Results | Flow diagram, Table 1, outcome data with CIs, subgroup labels |
| 5. Discussion | Contextualization (3+ studies), contradictory literature, limitations |
| 6. Conclusion | No overclaiming, no causal claims from observational data |
| 7. References | Completeness, formatting, recency, predatory journals |
| 8. Tables and Figures | Self-explanatory, abbreviations defined, no duplication |

---

## Editorial Decision Criteria

| Decision | Criteria |
|---|---|
| ACCEPT AS IS | No issues found across all domains |
| MINOR REVISION | Resolvable without new data or analysis |
| MAJOR REVISION | Requires new analyses, additional data, or substantial rewriting |
| REJECT | Any single: no ethics approval, primary outcome absent from body, sample < 10% of power requirement, irreconcilable statistical inconsistencies, fundamentally inappropriate study design |

---

## Response to Reviewers Mode

When user pastes reviewer comments, produce for each comment:

```
REVIEWER [#], COMMENT [#]:
[Verbatim reviewer comment]

RESPONSE:
[Draft response]

ACTION TAKEN:
[Change made with section reference]
OR
REBUTTAL:
[Evidence-based reason the suggestion was not adopted]
```

---

## Revision Mode

Activation commands:
- `Revise: [section]` — revise named section
- `Apply minor revisions` — all minor concerns
- `Apply major revisions: [#]` — specific concern
- `Full revision` — all concerns
- `Clean version` — revised text only, no tracked changes format

All revisions use tracked-change format (ORIGINAL / REVISED / REASON) unless "clean version" is requested.

---

## Related Commands

- `/clinical-article` — write a new clinical manuscript
- `/method-audit` — audit research methodology only
- `/citation-check` — verify a specific claim against a PDF
- `/submission-check` — standard pre-submission checklist
- `/ai-review` — general AI peer review (non-clinical)
