---
title: "Where AI Meets RWE: A Map of the Regulatory Landscape Across Four Jurisdictions"
type: analysis
domain: [ai, rwe]
jurisdictions: [US, EU, JP, KR]
tags: [ai-governance, rwe, validation, context-of-use, regulatory-convergence]
note_status: published
as_of: 2026-07-14
last_reviewed: 2026-07-14
---

# Where AI Meets RWE

### A map of official regulatory documents across the US, EU, Japan, and Korea

**As of 14 July 2026.** This is a living document; the timeline is maintained as new documents are published. See the [changelog](#changelog).

---

## Why this map exists

AI and real-world evidence have, for most of the past decade, developed as **separate regulatory tracks**.

The RWE track took shape in the US after the 21st Century Cures Act and reached an international milestone when ICH M14 arrived at Step 4 in September 2025. But M14's scope is narrower than is often reported: it covers the planning, design, analysis, and reporting of **non-interventional studies using RWD for drug safety assessment** — not RWE in general. Describing it as the completion of international harmonization for RWE overstates what it does.

The AI track has formed rapidly since 2023, across drug development, AI-enabled medical devices, and regulators' own internal operations. Its documents differ enormously in legal weight: statutes, final guidance, drafts, reflection papers, non-binding advisory notes, expert committee reports, and internal agency action plans.

The two tracks have begun to touch. FDA's January 2025 draft guidance explicitly includes the processing and analysis of RWD sources, the evaluation of clinical trial endpoints, and the handling of post-market adverse event information among the AI use cases within its scope. EMA's March 2025 RWE reflection paper requires that where AI is used to collect or process RWD, the study protocol describe how AI performance was assessed, what biases may arise, and how those biases could affect study results.

So the honest summary is this:

> **AI and RWE have started to meet. The meeting is still at the level of principles.**

How much error is tolerable in an AI-extracted confounder or outcome, how that error propagates into a causal effect estimate, and what external validation and sensitivity analysis are required — none of these has a common, cross-jurisdictional standard.

---

## A note on document status

Comparing documents of different legal weight as though they carried equal regulatory force is the most common error in this space. Throughout this map, document status is stated explicitly.

| Document type | What it means |
|---|---|
| Statute / Regulation | Legally binding |
| Final Guidance / Guideline | The agency's current recommendation and expectation. **Not** equivalent to law |
| Draft Guidance | Under consultation or not yet finalized |
| Reflection Paper | The agency's scientific perspective and direction of travel |
| Advisory note (민원인 안내서) | Non-binding reference material for applicants |
| Expert committee report | A survey of scientific and regulatory issues; not a guideline |
| Action Plan | How an agency will run its **own** operations. Not a requirement on sponsors |

---

## 1. Consolidated timeline

| Date | Jurisdiction | Document or event | Status · Track |
|---|---|---|---|
| 2016-12 | US Congress | 21st Century Cures Act | Statute · RWE |
| 2021-03-23 | JP MHLW/PMDA | Basic principles and reliability considerations for using registries in marketing applications | Notification · RWE |
| 2023-07-11 | KR MFDS | Guideline on the application of RWE to medical devices (revised) | Advisory note · RWE |
| 2023-07-19 | EMA | Draft reflection paper on AI in the medicinal product lifecycle — consultation opens | Draft · AI |
| 2023-08-28 | JP PMDA | Report on programme medical devices using AI | Expert report · AI device |
| 2024-05-21 | ICH | M14 reaches Step 2; public consultation opens | Draft international guideline · RWE |
| 2024-06-28 | KR MFDS | Advisory note on the use of AI in drug development | Advisory note · AI |
| 2024-08-01 | EU | EU AI Act enters into force | Statute · AI |
| 2024-09-09/11 | EMA | Reflection paper on AI in the medicinal product lifecycle adopted (CHMP, CVMP) | Final reflection paper · AI |
| 2024-12-24 | KR MFDS | Casebook: AI in drug development | Casebook · AI |
| 2025-01-06 | FDA | Considerations for the Use of AI to Support Regulatory Decision-Making for Drug and Biological Products | Draft guidance · AI |
| 2025-01-07 | FDA | AI-Enabled Device Software Functions: Lifecycle Management and Marketing Submissions | Draft guidance · AI device |
| 2025-01-24 | Korea | Digital Medical Products Act — first phase in force | Statute · digital health |
| 2025-01-24 | KR MFDS | Review guideline for generative-AI medical devices | Advisory note · AI device |
| 2025-03-17 | EMA | Reflection paper on RWD in non-interventional studies for regulatory purposes — adopted | Final reflection paper · RWE |
| 2025-06-19 | EU MDCG | FAQ on the interplay between MDR/IVDR and the AI Act | Non-binding FAQ · AI device |
| 2025-08-18 | FDA | Predetermined Change Control Plans for AI-enabled devices — finalized | Final guidance · AI device |
| 2025-09-04 | ICH | M14 reaches Step 4 | International guideline · RWE |
| 2025-09-18 | EMA CHMP | ICH M14 adopted in Europe | EMA guideline · RWE |
| 2025-09-26 | JP PMDA | Action Plan for the Use of AI in Operations at the PMDA | Internal agency plan |
| 2025-12-17 | FDA | RWE for regulatory decision-making on medical devices — finalized | Final guidance · RWE |
| **2026-01-14** | **FDA + EMA** | **Guiding Principles of Good AI Practice in Drug Development** | **Joint principles · AI** |
| 2026-02/03 | JP PMDA | Symposia on SaMD and RWD | Discussion; not guidance |
| 2026-03-18 | EMA | ICH M14 applies in the EU | EMA guideline · RWE |
| 2026-06-11 | KR HIRA | Guideline on real-world evidence generation for pharmaceutical outcomes assessment | Reimbursement guideline |
| 2026-06-26 | KR MFDS | Review criteria for change control plans for AI digital medical devices | Advisory note · AI device |

> **On ICH M14 in Europe.** EMA lists 18 March 2026 as the date of application. But an EMA scientific guideline is not EU law; it is a regulatory standard from which departure generally requires scientific justification. "It began to apply within the EU regulatory framework" is accurate; "it acquired legal force" is not.

📄 **Notes in this repository:** [FDA–EMA Guiding Principles (Jan 2026)](../regulators/fda/2026-01_fda-ema-good-ai-practice.md)

---

## 2. Jurisdiction by jurisdiction

### 🇺🇸 United States — FDA

**Drugs and biologics.** The central document is the January 2025 draft guidance, *Considerations for the Use of AI to Support Regulatory Decision-Making for Drug and Biological Products*. It applies where an AI model produces information or data supporting a regulatory decision on safety, effectiveness, or quality. It explicitly excludes early discovery work and operational efficiencies that do not bear on patient safety, product quality, or study reliability.

Its organizing structure is a **risk-based credibility assessment keyed to context of use**, in seven steps: define the question the model is meant to answer; define the specific context of use; assess model risk; establish a plan to demonstrate credibility; execute it; document results and deviations; and determine whether the model is sufficiently credible **for that context of use**.

The emphasis is not on the performance number but on what decision the model informs and how much a wrong output would matter.

**Where AI and RWE meet in FDA's framing.** The draft names, among its in-scope AI use cases: processing and analysis of RWD sources; evaluation of clinical trial endpoints or outcomes; processing of post-market adverse event information; and support for pharmacovigilance. FDA does not treat AI and RWE as disjoint domains. What it does not provide is a minimum performance level for AI-derived variables in RWE studies, or a method for assessing how misclassification propagates into an effect estimate — those are left to context-specific judgment and engagement with the agency.

**AI-enabled devices** run on a separate document line: lifecycle management and marketing submission recommendations (draft, January 2025) and Predetermined Change Control Plans (final, August 2025). A PCCP requires that anticipated model changes — how they will be made, verified, and assessed for impact — be submitted in advance.

**RWE** has its own established series across drugs and devices: general considerations for RWD/RWE, registry fitness, data standards, EHR and claims fitness, and, finalized in December 2025, RWE for device regulatory decisions (replacing the 2017 document), which asks that RWD be assessed for relevance, reliability, and traceability.

> **Position:** FDA frames AI as a problem of **model credibility for a declared context of use**. It acknowledges the AI–RWE intersection but leaves the concrete validation requirements to be set by purpose and regulatory risk.

### 🇪🇺 European Union — EMA, EU, MDCG

Legal layers must be kept distinct here: the EU AI Act is a statute; EMA's reflection papers are scientific and regulatory perspectives; ICH M14 is regulatory methodology for RWD studies; the MDCG FAQ is non-binding practical interpretation.

**Drug lifecycle AI.** EMA's *Reflection Paper on the Use of Artificial Intelligence in the Medicinal Product Lifecycle* (CHMP 9 Sep 2024; CVMP 11 Sep 2024) spans R&D, clinical trials, authorization, manufacturing, pharmacovigilance, and post-market activity. Its principles: a risk-based and human-centric approach; data and models fit for the intended purpose; data integrity and traceability; control of leakage, overfitting, and bias; proper separation of training, validation, and test data; generalizability and external validation; monitoring for model change and performance degradation; data and algorithm governance; human oversight and accountability.

EMA prefers transparent, interpretable models **as a matter of principle**. It does not categorically exclude black-box models, but the conditions are specific: the developer must demonstrate that an interpretable model's performance or robustness would be insufficient, and must present adequate validation, monitoring, and risk management. Summarizing this as "black boxes are allowed in low-risk settings" is inaccurate.

**Where AI and RWE meet directly.** EMA's *Reflection Paper on Use of Real-World Data in Non-interventional Studies to Generate Real-World Evidence for Regulatory Purposes* (adopted March 2025) is the most explicit document in any jurisdiction on this intersection. Where AI is used to collect or process RWD, the protocol must describe: how AI performance was assessed; what biases AI may introduce; and the potential impact of those biases on study results.

This is a real requirement, and it is more concrete than anything on the US side. What it still does not supply: an acceptable accuracy threshold, the required scope of external validation, or any quantitative sensitivity analysis for error propagation.

**ICH M14** reached Step 4 on 4 September 2025, was adopted by EMA on 18 September 2025, and applies from 18 March 2026. Its scope — general principles for the planning, design, analysis, and reporting of non-interventional studies using RWD **for drug safety assessment** — excludes effectiveness RWE, AI-enabled devices, and any detailed standard for AI-generated variables.

**The AI Act and medical devices.** In force since 1 August 2024, applying in phases. Medical device AI may fall under both the AI Act and MDR/IVDR. MDCG published an FAQ on the interplay in June 2025; the document itself states that it does not carry the legal weight of an official Commission interpretation.

> **Position:** EMA frames AI broadly, as a **data and model governance problem across the product lifecycle** — and, uniquely, has begun to require that AI-based RWD processing be documented for performance and bias inside the study protocol.

### 🇯🇵 Japan — MHLW, PMDA

Japan has not produced a single document covering AI across the drug lifecycle. Two separate systems have developed instead: **reliability assurance for registries and medical information databases**, and **development, approval, and change management for AI/programme medical devices**.

**RWD and registries.** In 2021, MHLW and PMDA issued basic principles for using registries in marketing applications, together with considerations for ensuring the reliability of registry data used in such applications. These center on data generation, collection, management, transformation, and traceability. Japan subsequently elaborated considerations for using registry data in partial change applications and revisions to electronic package inserts.

This should not be read as "Japan generally permits indication or formulation changes without conventional trials." What was established is the **set of conditions and considerations required when registry data are used in such regulatory decisions**.

**AI-enabled devices.** The PMDA Science Board's 2023 *Report on Programme Medical Devices Using AI* addresses machine learning bias, management of training/validation/test data, post-market continued learning, reuse of evaluation data, simulation data, and use of clinical information databases. It is an expert report on scientific and regulatory challenges — not a guideline.

**The Action Plan is frequently miscategorized.** The *Action Plan for the Use of AI in Operations at the PMDA* (September 2025) governs how PMDA uses AI in **its own** review, consultation, and safety operations. It is not a guideline on how sponsors may use AI in regulatory submissions. PMDA held symposia on SaMD and RWD in early 2026 — a signal that the two topics are converging in the Japanese conversation, but not a formal integrated guideline.

> **Position:** Japan has built **RWD reliability** and **AI/SaMD regulation** as parallel systems. Within the publicly available official documents, an integrated standard connecting the two remains limited.

### 🇰🇷 Korea — MFDS, HIRA

Korea's documents are distributed across agencies and product categories: drug AI, AI medical devices, device RWE, and pharmaceutical outcomes assessment each sit in different places.

**Drug AI.** MFDS published an advisory note on the use of AI in drug development (28 June 2024) — reference material for developers rather than settled regulatory principle. It raises explainability, reliability, privacy, safety and security, bias mitigation, and impact assessment from early development. A casebook of applied examples followed in December 2024.

**AI and digital medical devices.** The Digital Medical Products Act took effect in its first phase on 24 January 2025 — phased, not wholesale. The same day, MFDS issued a review guideline for generative-AI medical devices, which the agency's own press release described as a world first; that claim should be attributed to MFDS rather than asserted independently. Review criteria for change control plans for AI digital medical devices followed in June 2026.

**Device RWE.** MFDS established a guideline on applying RWE to medical devices in 2019 and revised it in 2023, covering the use of real-world data and evidence in device approval and safety management.

**HIRA's RWE.** The *Guideline on Real-World Evidence Generation for Pharmaceutical Outcomes Assessment* (11 June 2026) sits in an entirely different decision context: not MFDS product approval, but the effectiveness, safety, cost-effectiveness, and post-listing performance management of drugs reimbursed under national health insurance. Classifying it as Korea's general RWE approval guideline is a category error. In Korea the division is clean — **MFDS: approval and safety; HIRA: reimbursement and outcomes assessment.**

> **Position:** Korea has moved quickly on **AI medical device** law and guidance. Drug AI, device RWE, and reimbursement RWE remain **distributed across products and decision stages.**

---

## 3. Comparison

| | Drug AI | AI devices | RWE | The AI × RWE intersection |
|---|---|---|---|---|
| **US** | FDA draft guidance | Lifecycle draft; PCCP final | Multiple final guidances, drugs and devices | RWD processing, endpoint evaluation, and post-market pharmacovigilance named as in-scope AI uses; requirements set per context of use |
| **EU** | EMA final reflection paper | AI Act + MDR/IVDR | EMA RWE reflection paper; ICH M14 | **Most explicit:** protocol must describe AI performance, bias, and impact on results |
| **JP** | Comparatively limited | PMDA expert report; change management | Registry/database reliability notifications | SaMD × RWD under discussion; no integrated guideline |
| **KR** | Advisory note + casebook | Digital Medical Products Act; generative-AI review; change control | MFDS device RWE; HIRA outcomes RWE | Distributed across approval/reimbursement and drug/device |

A single ranking of "RWE maturity" across these jurisdictions should be resisted. Electronic submission mandates, data standardization, methodological guidance, submissibility, and actual approval precedents are different dimensions and do not move together.

---

## 4. What the jurisdictions agree on

Across all four, the same six commitments recur:

1. The purpose and specific context of use of the AI must be clearly defined.
2. Data used for training, validation, and evaluation must be fit for that purpose.
3. The generation, processing, and modification of data and models must be traceable.
4. Bias, misclassification, lack of representativeness, and generalizability must be assessed.
5. When the model changes or the deployment environment changes, re-evaluation is required.
6. Using AI does not dissolve the accountability of the developer, sponsor, marketing authorization holder, or user.

FDA expresses this as **context-of-use-based credibility assessment**; EMA as **lifecycle-based risk and governance**. The emphases differ; the approaches are not mutually exclusive. The January 2026 FDA–EMA joint principles are best read as an attempt to fix a shared vocabulary across the two.

---

## 5. What regulation has not yet answered

This is the substantive core of the map. Five questions remain open in every jurisdiction.

### 5.1 How accurate must an AI-extracted variable be?

Suppose NLP extracts smoking status or disease severity from unstructured clinical notes for use as a **confounder**. Sensitivity, specificity, and PPV can be computed for the classifier. But in an RWE study, what matters more is the **direction and magnitude of bias that this error induces in the final treatment effect estimate**.

Current documents require that performance and bias be assessed. None sets a common standard for what performance is sufficient for a regulatory purpose.

### 5.2 How does model error propagate into the causal estimate?

Two AI models with identical accuracy can have entirely different consequences depending on where the extracted variable sits in the causal structure:

- cohort selection
- exposure definition
- outcome definition
- confounding adjustment
- subgroup classification

Applying FDA's context-of-use framework to RWE therefore requires more than model performance. It requires reasoning about **the variable's role in the causal model and the effect of its error on the estimand.** No current document supplies the vocabulary for this.

### 5.3 How far must external validation go?

A model validated at one hospital, in one period, in one country, guarantees nothing elsewhere. Performance can shift with institution, data source, patient mix, documentation practice, language, country, and model version. **What level of revalidation is required when these change is not harmonized anywhere.**

This is the gap I consider most consequential for RWE, and it has no name in the current documents. It is not *data drift* — drift is temporal, the same population changing over time. It is not *generalizability* as EMA and the FDA–EMA principles use the term — that is named as an aspiration, without a method. It is a **spatial** problem: an extractor built on one population, applied to a structurally different target population, where the induced measurement error is neither random nor stable across the two.

### 5.4 If the model changes, can the study be reproduced?

AI models get updated. The same source data, processed with a different model version, can yield different variables and different results. Reproducibility therefore requires: model and training-data versions; the software environment at inference; preprocessing rules; thresholds; a change history; and a reproducible audit trail.

Change management principles for AI devices are maturing. How to apply them to an ordinary RWE analysis pipeline is unresolved.

### 5.5 Can approval and reimbursement use the same standard?

Regulators assess safety, efficacy, and quality. HTA bodies and payers assess comparative effectiveness, cost-effectiveness, and budget impact. The same AI-derived variable serves different decisions, with different costs of being wrong. A single validation standard may not transfer cleanly between them — a question Korea's split between MFDS and HIRA makes concrete.

---

## 6. Where this leaves us

AI and RWE regulation are no longer two separate worlds. FDA includes AI-based RWD analysis and post-market information processing within the scope of its draft guidance. EMA requires that AI-based RWD processing be documented for performance and bias inside the study protocol.

But the documents that exist mostly say **what must be assessed**. They do not say how much error is tolerable in an AI-generated variable used in an RWE study, how that error propagates into a causal effect estimate, or what external validation and sensitivity analysis are required.

The next question is therefore not whether to use AI.

> **It is: under what conditions will data and variables generated by AI be accepted as evidence for a regulatory decision?**

That is the question this repository exists to track.

---

## 7. Watchlist

- Finalization of FDA's drug AI draft guidance
- Finalization of FDA's AI-enabled device lifecycle draft guidance
- Korea's official implementation timeline and approach for ICH M14
- Whether Japan issues AI guidance covering the drug lifecycle broadly
- Phased application of the EU AI Act and its detailed relationship to device and drug regulation
- Validation precedents for AI-extracted RWD variables, by regulator
- Actual cases where AI-based RWE has been submitted for approval, post-market safety, or HTA

---

## Changelog

- 2026-07-14 — Analysis created. Timeline current as of this date.

---

*Compiled from official agency publications, with draft, final, statutory, and internal-operational documents distinguished throughout. Interpretation is my own and does not constitute regulatory advice.*
