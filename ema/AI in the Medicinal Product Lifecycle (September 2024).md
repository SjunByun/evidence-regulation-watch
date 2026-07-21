---
title: "Reflection paper on the use of Artificial Intelligence (AI) in the medicinal product lifecycle"
issuer: EMA
doc_type: reflection-paper
document_number: EMA/CHMP/CVMP/83833/2023
published: 2024-09-09
legal_status: non-binding (reflection paper)
jurisdiction: EU
source_url: "https://www.ema.europa.eu/system/files/documents/scientific-guideline/reflection-paper-use-artificial-intelligence-ai-medicinal-product-lifecycle-en.pdf"
tags: [ai-governance, validation, risk-tiering, transportability, post-authorisation]
note_status: published
last_reviewed: 2026-07-21
---

# EMA — AI in the Medicinal Product Lifecycle (September 2024)

## TL;DR

- EMA sorts AI risk on **two separate axes**: harm to patients, and influence on a regulatory decision. A system can score low on one and high on the other.
- A post-authorisation study that is a **condition of authorisation** may have to meet pivotal-trial rules: pre-specified analysis plan, frozen data pipeline, frozen models.
- EMA asks that model performance generalise to the target population but does not say how to show it. FDA's EHR/claims guidance says how. Each document is half the answer.

## 1. Document profile

| | |
|---|---|
| Issuer | EMA (CHMP and CVMP) |
| Number | EMA/CHMP/CVMP/83833/2023 |
| Published | 9 September 2024 |
| Status | Reflection paper — non-binding. States current thinking; not a guideline |
| Length | 18 pages |
| Scope | AI across the medicinal product lifecycle: discovery, non-clinical, trials, precision medicine, manufacturing, post-authorisation |
| Not covered | Whether software counts as a medical device — not EMA's remit |

## 2. What the document says

### Two risk axes

EMA labels systems affecting patient safety **high patient risk**, and systems that substantially affect a regulatory decision **high regulatory impact**. Risk depends on the context of use and on how much influence the AI actually exerts, and it can change over a system's life.

Responsibility for the fitness of all models, data, and pipelines rests with the sponsor, applicant, or marketing authorisation holder. EMA notes its requirements may be stricter than ordinary data science practice.

Submissions seeking advice should address data integrity and the generalisability of model performance to the target population and context of use.

### Requirements differ by lifecycle stage

**Pivotal trials.** AI that transforms or analyses trial data counts as part of the statistical analysis. Incremental learning is not accepted. Models and the pre-processing pipeline must be frozen and documented in the SAP before database lock. Once the dataset is opened, unplanned changes make results post hoc.

**Post-authorisation.** Pharmacovigilance gets more latitude — incremental learning is contemplated for signal detection and adverse event classification. But where a post-authorisation study is a condition of the marketing authorisation, pivotal-trial requirements may apply.

**Precision medicine.** AI affecting indication or dosing is both high patient risk and high regulatory impact.

### Technical expectations

- Full traceable documentation of data provenance and every processing step
- Held-out test data used **once**; if development continues, a new independent test set is needed
- Metrics insensitive to class imbalance; the distribution of cross-validated results rather than a single number; pre-defined performance thresholds
- Transparent models preferred; black-box models require the developer to show that an interpretable model performed inadequately
- Any non-trivial change to the software or hardware stack triggers performance re-evaluation
- A risk management plan defining failure modes and how to suspend or retire the model

EMA also flags that "validation" means different things in machine learning and in medicines development.

## 3. What it means in practice

> This section is my professional opinion, not a description of the document.

### Evidence-generation AI sits in a cell most frameworks miss

Take an NLP tool that extracts smoking status from clinical notes for use as a confounder in a safety study.

Patient risk: near zero. It never reaches a patient or informs a clinical decision.

Regulatory impact: potentially high. If that variable affects whether a safety signal is confirmed, an extraction error feeds straight into a regulatory conclusion about a marketed drug.

Most AI governance frameworks — including the EU AI Act's high-risk classification — are built around clinical AI, where both risks rise together. They have little to say about tools that are harmless to patients and consequential for regulators. EMA's two axes are the clearest vocabulary I have found for naming that gap.

One consequence: regulatory impact is the harder axis to judge, because it depends on the study rather than the model. The same extractor is low impact in a descriptive table and higher impact as a confounder in a propensity model. Deciding which requires reading the causal structure of the study.

### The rule that changes how a PASS is run

At the end of the post-authorisation section sits a qualifier that is easy to miss: a study required as a condition of authorisation may face pivotal-trial rules — frozen models, frozen pipeline, pre-specified SAP.

For a PASS or PAES, that means the extraction algorithm must be locked before database lock, and changing it afterwards pushes the results into post hoc territory. Adjusting an algorithm mid-analysis is routine in exploratory work; here it would not be.

The contrast within the same section is the point. Signal detection may learn incrementally. A conditional post-authorisation study may not. The difference is regulatory impact — the risk axes producing genuinely different requirements rather than general language.

### EMA states the requirement; FDA supplies the method

I got this wrong on a first reading, and transcribing the document line by line is what corrected me. I had said EMA covered only transfer across time, leaving transfer across populations to FDA. That was inaccurate: EMA asks submissions to address generalisability to the target population.

What EMA does not give is a method. It does not explain why performance fails to transfer, so it offers no guide to what should be measured. That is consistent with what a reflection paper is for.

[FDA's EHR/claims guidance](../fda/2024-07_rwd-ehr-claims.md) supplies the missing account: performance is specific to the data source and population, because sensitivity and specificity vary by database and predictive values depend on prevalence.

So one document makes generalisability an expectation without a method, and the other gives a method without framing it as an AI requirement. Read one, and you know either what is expected or how to do it — not both.

## 4. Cross-references

- **[FDA–EMA Guiding Principles (Jan 2026)](../fda/2026-01_fda-ema-good-ai-practice.md)** — asks for validation proportionate to risk without defining risk. This paper defines it.
- **[FDA — EHR and Claims Data (Jul 2024)](../fda/2024-07_rwd-ehr-claims.md)** — the method behind the generalisability expectation.
- **[AI and RWE across four jurisdictions](../../analyses/2026-07_ai-and-rwe-four-jurisdictions.md)** — this paper answers the EU risk-tiering question posed there.
- **EMA RWE Reflection Paper (Mar 2025)** — the RWE-side counterpart. *(pending)*

## 5. Open questions

- Will "high regulatory impact" acquire criteria rather than examples?
- Where does a non-interventional PASS that is *not* a condition of authorisation fall?
- Will any later document give a method for showing generalisability to a target population?

## 6. Changelog

- 2026-07-21 — Note created. Corrects an earlier reading that treated this paper as covering only transfer across time (see §3).
