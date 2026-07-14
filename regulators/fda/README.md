# FDA — The Document Landscape

FDA does not regulate AI and real-world evidence in one place. It runs parallel document families, and they have different levels of methodological maturity. Reading one without the other gives a misleading picture of what is actually required.

This page maps the families. Notes in this folder go deep on individual documents.

> **Scope note:** This is a curated map of documents most relevant to the intersection of AI, RWD/RWE, and regulatory evidence generation. It is not intended to be an exhaustive list of all FDA guidance documents involving AI or RWE.

---

## Document families

### AI

| Document                                                                                                                                   | Status             | Published | Note                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------ | --------: | -------------------------------------------------- |
| Considerations for the Use of Artificial Intelligence To Support Regulatory Decision-Making for Drug and Biological Products               | Draft guidance     |   2025-01 | ⚪ planned                                          |
| Artificial Intelligence-Enabled Device Software Functions: Lifecycle Management and Marketing Submission Recommendations                   | Draft guidance     |   2025-01 | ⚪ planned                                          |
| Marketing Submission Recommendations for a Predetermined Change Control Plan for Artificial Intelligence-Enabled Device Software Functions | **Final guidance** |   2025-08 | ⚪ planned                                          |
| **Guiding Principles of Good AI Practice in Drug Development** — FDA and EMA                                                               | Joint principles   |   2026-01 | 🟢 **[note](2026-01_fda-ema-good-ai-practice.md)** |

### RWE — drugs and biological products

| Document                                                                                                                                                | Status             | Published | Note                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------ | --------: | ---------------------------------------- |
| Framework for FDA’s Real-World Evidence Program                                                                                                         | Program framework  |   2018-12 | ⚪ planned                                |
| Submitting Documents Using Real-World Data and Real-World Evidence to FDA for Drug and Biological Products                                              | **Final guidance** |   2022-09 | — primarily administrative               |
| Considerations for the Design and Conduct of Externally Controlled Trials for Drug and Biological Products                                              | Draft guidance     |   2023-02 | ⚪ planned                                |
| Considerations for the Use of Real-World Data and Real-World Evidence to Support Regulatory Decision-Making for Drug and Biological Products            | **Final guidance** |   2023-08 | ⚪ planned — cross-cutting document       |
| Real-World Data: Assessing Registries to Support Regulatory Decision-Making for Drug and Biological Products                                            | **Final guidance** |   2023-12 | ⚪ planned                                |
| Real-World Evidence: Considerations Regarding Non-Interventional Studies for Drug and Biological Products                                               | Draft guidance     |   2024-03 | ⚪ planned next                           |
| **Real-World Data: Assessing Electronic Health Records and Medical Claims Data To Support Regulatory Decision-Making for Drug and Biological Products** | **Final guidance** |   2024-07 | 🟢 **[note](2024-07_rwd-ehr-claims.md)** |

### RWE — medical devices

| Document                                                                             | Status             | Published | Note                                     |
| ------------------------------------------------------------------------------------ | ------------------ | --------: | ---------------------------------------- |
| Use of Real-World Evidence to Support Regulatory Decision-Making for Medical Devices | **Final guidance** |   2025-12 | ⚪ planned — supersedes the 2017 guidance |

**Status:** 🟢 note published · 🟡 in progress · ⚪ planned

---

## Why the distinction matters

The AI and RWE document families address related but different parts of the regulatory evidence chain.

The **AI documents** focus primarily on the credibility and management of AI models and systems. Their recurring concepts include:

* context of use;
* model risk;
* risk-proportionate credibility assessment;
* data fitness;
* model development and evaluation;
* documentation and traceability;
* human–AI interaction;
* life-cycle monitoring and change management.

The **RWE documents** focus primarily on whether data sources and study variables are fit for a particular regulatory evidence-generation purpose. Their recurring concepts include:

* data relevance and reliability;
* conceptual and operational definitions;
* validation against an appropriate reference standard;
* sensitivity, specificity, and predictive values;
* differential and non-differential misclassification;
* dependent and independent measurement error;
* quantitative bias analysis;
* traceability from source data to the final analysis dataset.

These document families should be treated as **complementary rather than hierarchical**.

When AI is used to derive a variable for an RWE study:

* the AI documents inform how the model and surrounding system should be developed, evaluated, documented, and maintained;
* the RWE documents inform whether the resulting variable is sufficiently valid for its role in the study and how measurement error could affect the evidentiary conclusion.

For purposes of study-variable ascertainment, an NLP or machine-learning extractor may function as, or form part of, an **operational definition**. It therefore remains subject to established expectations concerning the underlying conceptual definition, validation, measurement error, and study-specific fitness for use.

The July 2024 EHR and medical claims guidance is more operationally specific than the January 2026 joint AI principles on these measurement questions. This does not establish a formal hierarchy between the documents. They address different but overlapping objects:

* the credibility of the **AI model and system**;
* the validity of the **study variable and its downstream evidentiary use**.

This relationship is discussed further in the [EHR and medical claims note](2024-07_rwd-ehr-claims.md#3-what-it-means-in-practice--an-evidence-generation-reading).

---

## Where the document families touch explicitly

### 1. AI-derived variables in the July 2024 EHR and claims guidance

Section IV.B.5 of the July 2024 guidance addresses the use of AI and other computerized methods to derive information from unstructured healthcare data.

Where a protocol proposes AI or another derivation method, FDA recommends that the protocol specify:

* the assumptions and parameters of the computer algorithms;
* the data source from which the information used to build the algorithm was drawn;
* whether the algorithm was supervised or unsupervised;
* the metrics associated with validation of the methods.

Relevant effects of AI or other computerized extraction methods on data quality should also be documented in the protocol and analysis plan.

The same guidance places these AI-derived data elements within a broader framework covering:

* conceptual and operational definitions;
* validation;
* applicability of prior validation evidence;
* misclassification;
* quantitative bias analysis;
* data provenance and traceability.

### 2. RWD use cases in the January 2025 AI draft guidance

The January 2025 AI draft guidance identifies several in-scope examples involving real-world or clinical data, including:

* processing and analyzing large datasets from RWD sources or digital health technologies;
* developing clinical trial endpoints or assessing outcomes;
* identifying, evaluating, and processing postmarketing adverse drug experience information.

The draft guidance establishes a risk-based credibility assessment framework for AI model outputs in a defined context of use.

### 3. Direct cross-reference between the documents

The January 2025 AI draft guidance directly refers readers to the July 2024 EHR and medical claims guidance when discussing AI use involving electronic healthcare and real-world data.

The relationship between the two documents is therefore not only interpretive. FDA’s AI framework itself points to the existing RWE data-fitness framework for additional information.

---

## What remains study-specific

The reviewed documents do not establish a single universal minimum performance threshold for every AI-derived study variable.

They also do not prescribe one mandatory method for evaluating how measurement error in an AI-derived exposure, outcome, covariate, or effect modifier propagates into a treatment-effect estimate.

The appropriate evidence will depend on factors such as:

* the context of use;
* the role of the variable in the study;
* the clinical and regulatory consequences of error;
* the data source and study population;
* the reference standard;
* whether error may be differential or dependent;
* whether prior validation evidence applies to the proposed setting;
* the feasibility and usefulness of sensitivity analysis or quantitative bias analysis.

The absence of a universal threshold should not be read as an absence of validation expectations. It means that the validation strategy and acceptance rationale remain risk-based, use-specific, and scientifically justified.

Related cross-jurisdictional questions are discussed in the [four-jurisdiction AI and RWE map](../../analyses/2026-07_ai-and-rwe-four-jurisdictions.md).

---

## Reading order

For readers approaching the intersection of AI and RWE for the first time, the following order may be useful:

1. **Framework for FDA’s Real-World Evidence Program (2018)**
   Establishes the overall FDA RWE program and policy context.

2. **Considerations for the Use of RWD and RWE to Support Regulatory Decision-Making (2023)**
   Provides cross-cutting considerations for regulatory submissions involving RWD and RWE.

3. **Assessing EHR and Medical Claims Data (2024)**
   Provides detailed recommendations on data-source fitness, variable definition, validation, misclassification, and traceability.

4. **Considerations for the Use of AI to Support Regulatory Decision-Making (2025, draft)**
   Introduces FDA’s risk-based credibility assessment framework for AI model outputs.

5. **Guiding Principles of Good AI Practice in Drug Development (2026)**
   Places the FDA approach within a broader FDA–EMA vocabulary for good AI practice across the drug product life cycle.

---

## Interpretation policy for this repository

Each note distinguishes among:

1. **what the source document explicitly states;**
2. **what can reasonably be inferred from the document;**
3. **the author’s professional interpretation or proposed implication.**

Interpretive sections are labeled and should not be attributed to FDA, EMA, or another regulatory authority unless the source document expressly supports the statement.

Document titles, status, publication dates, scope, and legal status should be checked against the official source at the time each note is reviewed.

---

*FDA guidance documents generally do not establish legally enforceable responsibilities. Unless a specific statutory or regulatory requirement is cited, “should” means suggested or recommended, not required. Draft guidances are not for implementation. Joint principles are identified separately because they are not formal FDA guidance documents.*

*Last reviewed: 2026-07-14.*
