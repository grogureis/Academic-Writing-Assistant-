---
title: "Clinical Article — Phase 2: IMRAD Manuscript Writing"
phase: 2
outputs:
  - manuscript_draft.md
phase_gate_out: "phase-3-revision.md"
---

## Purpose

Write the full IMRAD manuscript following the STROBE-IMRAD protocol in `agents/prompts/clinical_writer.md`. Every section must satisfy the corresponding STROBE checklist items.

## Prerequisite

`study_design_brief.md` and `literature_brief.md` must exist. Do not write without confirmed study design and verified references.

---

## Writing Order

Write sections in this sequence. Do NOT write in reading order.

| Order | Section | Rationale |
|---|---|---|
| 1 | Methods | Anchors everything; written before results to prevent overpromising |
| 2 | Results | Data-only; no interpretation |
| 3 | Discussion | Interpreting results; references already collected |
| 4 | Introduction | Background written after knowing what the study actually found |
| 5 | Abstract | Written last; summarizes completed manuscript |
| 6 | Title | Finalized after abstract is complete |

---

## Methods Checklist (STROBE Items 4-12)

Write subheadings in this order. Check each item off as written.

- [ ] **Study Design and Setting** (Items 4-5): Study type in first sentence. Institution type, location, ethics approval number, date range.
- [ ] **Participants** (Item 6): Inclusion criteria, exclusion criteria with rationale, sampling method, patient identification source, follow-up description.
- [ ] **Variables** (Item 7): Primary outcome (definition + measurement + timing), exposure variable, covariates/confounders, scoring tools with validation citations.
- [ ] **Data Sources and Measurement** (Item 8): How each variable was measured, data collector, inter-rater reliability if applicable.
- [ ] **Bias** (Item 9): Selection bias, information bias, confounding, immortal time bias (if retrospective cohort), surveillance bias. For each: state whether it applies and mitigation.
- [ ] **Study Size** (Item 10): A priori power calculation OR post-hoc statement with justification.
- [ ] **Quantitative Variables** (Item 11): How continuous variables were handled; categorization method if applicable; linearity of logit check.
- [ ] **Statistical Analysis** (Item 12): Normality assessment → descriptive stats → univariate → ROC → multivariate → subgroup → sensitivity. State software and version. Apply missing data protocol.
- [ ] **Outcomes** (MANDATORY LAST): "The primary outcome was [X]. Secondary outcomes included [Y] and [Z]."
- [ ] **Reporting Compliance**: "This study was reported in accordance with [STROBE/CONSORT/STARD] guidelines."

---

## Results Checklist (STROBE Items 13-17)

- [ ] **Participant Flow** (Item 13): Total screened → excluded with reasons → final n. [FIGURE: Flow diagram placeholder]
- [ ] **Descriptive Data** (Item 14): [TABLE 1 placeholder]. In text: highlight 2-3 key findings.
- [ ] **Outcome Data** (Item 15): Event rates per group.
- [ ] **Univariate Results** (Item 16): [TABLE 2 placeholder]. Test statistics and p-values.
- [ ] **ROC Analysis**: AUC (95% CI), Youden index cutoff, sensitivity, specificity, PPV, NPV, LR+, LR-. [FIGURE 1 placeholder]
- [ ] **Multivariate Results** (Item 16): [TABLE 3 placeholder]. Adjusted OR (95% CI), p-value, Hosmer-Lemeshow, Nagelkerke R-squared.
- [ ] **Other Analyses** (Item 17): Subgroup and sensitivity analyses if applicable.

**Results rules:** Past tense throughout. No interpretation. No citations.

---

## Discussion Checklist (STROBE Items 18-21)

Write in this paragraph order:

- [ ] **Paragraph 1 — Main Finding** (Item 18): Open with "This study found that..." Formula: Finding + Magnitude + Direction + Clinical Context. 2-3 sentences.
- [ ] **Paragraph 2 — Clinical Significance**: Disease burden, morbidity, diagnostic/therapeutic challenges. 7-8 sentences, 3-4 references.
- [ ] **Paragraph 3 — Literature Comparison** (Item 20): Compare with 3+ prior studies. Include contradictory and null-result studies. 8-10 sentences, 5-6 references.
- [ ] **Paragraph 4 — Mechanistic Explanation**: Biological/physiological plausibility. 4-5 sentences, 2-3 references.
- [ ] **Paragraph 5 — Limitations** (Item 19): Flowing prose. No numbered list. For each limitation: state it, direction/magnitude of bias, mitigation. Address: retrospective design, single-center, selection bias, information bias, residual confounding, temporal factors, missing data.
- [ ] **Paragraph 6 — Generalizability** (Item 21): 2-3 sentences on external validity.
- [ ] **Paragraph 7 — Clinical Implications** (optional): Only if evidence supports recommendation. 3-5 sentences.

**Discussion rules:** Present tense for interpretation. No "we" (use "this study"). No causal claims from observational data.

---

## Introduction Checklist (STROBE Items 2-3)

- [ ] **Paragraph 1 — Clinical Background** (Item 2): Epidemiology, incidence, mortality. Cite WHO data, registries, landmark studies. 3-5 sentences.
- [ ] **Paragraph 2 — Knowledge Gap** (Item 2): What is known, what is unknown. Cite guidelines, meta-analyses, conflicting studies. 3-5 sentences.
- [ ] **Paragraph 3 — Study Objective** (Item 3): Single sentence. "This study aimed to [objective] in [population] at [setting]." No citation. No hedging.

Total: 300-350 words, 10-12 references.

---

## Abstract (STROBE Item 1)

Write last. Present first.

Mandatory subheadings:
- **Aims:** 1 sentence, specific objective
- **Methods:** design, setting, participants, exposure, primary outcome, statistical approach
- **Results:** primary outcome with effect size, 95% CI, p-value; key secondary findings
- **Conclusion:** 1-2 sentences, clinical implication only, no speculation
- **Keywords:** 3 MeSH terms

250-300 words total.

---

## Title (STROBE Item 1)

Must include: study design + population + primary variable + outcome.

Template: "[Variable] as a [Predictor/Risk Factor] of [Outcome] in [Population]: A [Study Design]"

Example: "Serum Lactate as a Predictor of 30-Day Mortality in NSTEMI Patients Presenting to the Emergency Department: A Retrospective Cohort Study"

---

## Writing Rules (apply throughout)

### Voice and Tense
- Methods, Results: past tense
- Discussion: present tense for interpretation
- Third person only: "This study" not "We"

### Banned — check before submitting each section
Never use these words: accordingly, adept, amplify, arduous, augment, burgeoning, captivate, captivating, catapult, cognizant, commendable, compelling, conceptualize, consequently, considerable, convey, cornerstone, craft, crafting, crucial, delve, delved, delving, dynamic, efficiency, elevate, embark, employ, empower, enable, engage, engaging, enlightening, enriches, entrusting, essentially, esteemed, excels, exciting, exemplary, facilitate, fantastic, flourishing, formidable, foster, fostering, fundamental, fundamentally, glean, granular, groundbreaking, harness, hence, herein, heretofore, holistic, hone, imaginative, impactful, invaluable, iteration, leverage, linchpin, manifold, marvelous, maximize, milestone, multifaceted, nail, navigate, nugget, optimize, paramount, pivotal, profound, promote, remarkable, resonate, resonates, revolutionize, robust, scalable, scrappy, seamless, skyrocket, stellar, streamline, strive, substantial, supercharge, surge, synergy, tackle, tailor, tailored, tapestry, thereby, therein, thereof, trailblazer, transformative, turbocharge, ultimately, uncover, undeniable, underscores, undoubtedly, unleash, unlock, unparalleled, unveil, utilize, utmost, valuable, vibrant, vital, whip, whilst

Never use these phrases: a journey of, a multitude of, a plethora of, a testament to, actionable insights, as a result, as such, best practices, cannot be overstated, certainly here are, change management, competitive landscape, continuous improvement, cutting edge, cutting-edge, data-driven, deep dive, digital transformation, disruptive innovation, domain expertise, ever-evolving, fast-paced, game changer, going forward, in a world, in conclusion, in today's era, in today's world, key takeaways, mind blowing, mission-critical, moving forward, pain point, paradigm shift, perfect storm, plethora, powerful tool, secret sauce, significantly contributes, state-of-the-art, value proposition, well-crafted, widely recognized, with regards to

Also never use: em dash, "we" as subject, "first / secondly / thirdly" in limitations

---

## Output

Save draft as `manuscript_draft.md` with sections in reading order (Title, Abstract, Introduction, Methods, Results, Discussion, Conclusion, References) even though they were written in a different sequence.

Mark all placeholders clearly:
- `[TABLE 1: to be inserted by author]`
- `[FIGURE 1: ROC curve — to be inserted by author]`
- `[CITATION NEEDED: topic]`
- `[AUTHOR TO VERIFY: ethics approval number]`

---

## Phase Gate

Proceed to Phase 3 (Revision) only when:
- [ ] All STROBE items 1-22 addressed or flagged
- [ ] All [CITATION NEEDED] markers listed
- [ ] All TABLE and FIGURE placeholders marked
- [ ] No banned words in any section
- [ ] ROC analysis positioned after univariate, before multivariate
- [ ] Outcomes stated as last subsection of Methods
- [ ] Abstract written last and placed first
