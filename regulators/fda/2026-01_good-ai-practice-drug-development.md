---
title: "Guiding Principles of Good AI Practice in Drug Development"
issuer: [FDA, EMA]
domain: [ai]
doc_type: joint-principles
published: 2026-01-14
legal_status: non-binding (not formal guidance)
jurisdiction: [US, EU]
source_url: "https://www.fda.gov/media/189581/download"
tags: [ai-governance, drug-development, validation, lifecycle-management, data-provenance, context-of-use]
note_status: published
last_reviewed: 2026-07-14
---

# FDA–EMA — Guiding Principles of Good AI Practice in Drug Development (January 2026)

## TL;DR

- **Not an operational rulebook, but a shared regulatory vocabulary.** FDA and EMA jointly set out ten high-level principles that may inform future jurisdiction-specific policies and guidance, international harmonization, and consensus standards.
- **AI is situated within evidence generation.** For this document, AI means system-level technologies used to generate or analyze evidence across the drug product life cycle, including nonclinical, clinical, post-marketing, and manufacturing settings.
- **Regulatory credibility is anchored to context of use, not model performance alone.** The intended role and scope of the AI technology should be defined, with validation, risk mitigation, oversight, data, and performance assessment proportionate to that use.
- **A performance metric is not sufficient on its own.** Performance assessment applies to the complete system, including relevant human–AI interactions, and must use fit-for-use data and metrics appropriate to the intended context.
- **An important RWE gap remains.** The principles mention generalizability and data drift but do not distinguish or operationalize the transportability of AI-derived variables across sites, domains, or target populations—particularly when those variables enter causal analyses as confounders, exposures, or outcomes.

## The argument, in four moves

> My reading, in brief. Evidence for each interpretation is developed in [Section 3](#3-what-it-means-in-practice--an-evidence-generation-reading); the source document itself is summarized in [Section 2](#2-what-the-document-says).

1. **Regulatory credibility attaches to the use of the model, not to the model in isolation.** The document does not prescribe algorithm-level inspection criteria. Instead, it asks developers and users to define the intended purpose, scale scrutiny to the associated risk, assess the complete system against that purpose, and maintain a traceable evidence chain.

2. **Context of use can function as regulatory pre-specification for AI.** Principle 4 provides the reference point against which proportionate validation, risk mitigation, and oversight can be designed. If the intended use is chosen only after favorable performance has been observed, validation risks becoming post-hoc justification rather than an independent assessment of fitness for use.

3. **A performance metric is an observation, not a conclusion about fitness for use.** Principle 8 makes a held-out test-set result insufficient as a stand-alone deliverable. The relevant questions are why the model performs as observed, what signal it relies on, whether the evaluation data represent the intended setting, and under what conditions the result may fail.

4. **The principles raise the generalizability question but do not operationalize evidentiary transportability.** Principle 7 names generalizability, and Principle 9 mentions data drift, but the document does not distinguish temporal drift from cross-site, cross-domain, or cross-population distribution shift. For AI-derived variables used in causal RWE analyses, that gap may allow measurement error to propagate into the effect estimate without being visible in a headline performance metric.

## 1. Document profile

| | |
|---|---|
| Issuer | FDA and EMA, jointly |
| Published | January 2026 |
| Legal status | High-level, non-binding joint principles rather than formal jurisdiction-specific FDA or EMA guidance |
| Length | Approximately 2 pages; 10 principles, each described in a short paragraph |
| Scope | AI used to generate or analyze evidence across the drug product life cycle: **nonclinical, clinical, post-marketing, and manufacturing** |
| Stated purpose | To establish a common foundation for good AI practice and identify areas for collaboration in research, education, international harmonization, and consensus standards |
| Relationship to future regulation | May inform future regulatory policies and guidelines in different jurisdictions, consistent with applicable legal and regulatory frameworks |

## 2. What the document says

### 2.1 How AI is framed

For the purposes of the document, AI refers to system-level technologies used to **generate or analyze evidence** across the drug product life cycle, spanning nonclinical, clinical, post-marketing, and manufacturing phases.

This framing places AI within the existing evidentiary requirements for drug development and regulation. Drugs remain subject to established expectations for quality, efficacy, safety, and a favorable benefit–risk balance. The role of AI is therefore to reinforce those requirements rather than operate outside them.

The document also emphasizes that AI technologies are dynamic systems. Their development, deployment, use, and maintenance require continuing management so that their outputs remain accurate and reliable throughout the relevant life cycle.

### 2.2 The ten principles

The principles are grouped below by function rather than reproduced in their original numerical order.

#### The core validation logic: context of use → risk → performance assessment

| # | Principle | What it says |
|---|---|---|
| 4 | Clear context of use | The AI technology has a well-defined context of use: the role and scope of why it is being used. |
| 2 | Risk-based approach | Development and use follow a risk-based approach, with validation, risk mitigation, and oversight proportionate to the context of use and determined model risk. |
| 8 | Risk-based performance assessment | Assessment covers the complete system, including human–AI interactions, and uses fit-for-use data and metrics appropriate to the intended context of use. Predictive performance is supported by appropriately designed testing and evaluation. |

#### Documentation, governance, and life-cycle control

| # | Principle | What it says |
|---|---|---|
| 6 | Data governance and documentation | Data provenance, processing steps, and analytical decisions are documented in a detailed, traceable, and verifiable manner consistent with GxP. Privacy and protection of sensitive data are maintained throughout the life cycle. |
| 9 | Life cycle management | Risk-based quality management systems support the capture, assessment, and resolution of issues throughout the life cycle. Scheduled monitoring and periodic re-evaluation are used to maintain adequate performance, with data drift given as an example. |

#### Development quality and communication

| # | Principle | What it says |
|---|---|---|
| 7 | Model design and development practices | Development follows best practices in model and system design and software engineering, using fit-for-use data and considering interpretability, explainability, and predictive performance. Good development promotes transparency, reliability, generalizability, and robustness. |
| 10 | Clear, essential information | Clear, accessible, and contextually relevant information is presented in plain language to the intended audience, including users and patients. This includes context of use, performance, limitations, underlying data, updates, and interpretability or explainability. |

#### Foundational commitments

| # | Principle | What it says |
|---|---|---|
| 1 | Human-centric by design | Development and use align with ethical and human-centric values. |
| 3 | Adherence to standards | AI technologies follow relevant legal, ethical, technical, scientific, cybersecurity, and regulatory standards, including GxP. |
| 5 | Multidisciplinary expertise | Expertise covering both the AI technology and its context of use is integrated throughout the technology life cycle. |

### 2.3 What the document does not do

The document does not provide:

- formal risk tiers;
- quantitative performance thresholds;
- required validation artifacts or reporting templates;
- minimum sample-size requirements;
- acceptance criteria for particular AI use cases;
- detailed methods for external validation, generalizability, or transportability;
- jurisdiction-specific compliance procedures.

Instead, it identifies broad areas in which regulators, standards organizations, and collaborative bodies may develop more specific approaches through research, education, international harmonization, consensus standards, and future regulatory guidance.

## 3. What it means in practice — an evidence-generation reading

> **Interpretive note:** The discussion below is my professional reading of the principles from an evidence-generation and RWE perspective. It should not be read as language formally stated by FDA or EMA.

### 3.1 Regulatory credibility is anchored to the use of the model

This principles document does not prescribe algorithm-level inspection criteria. It instead places the model within a broader evidence-generating system defined by its context of use, associated risk, data, human interaction, and intended claim.

The practical sequence is:

1. define what the AI technology is intended to do;
2. determine the risk associated with that use;
3. design validation, mitigation, and oversight proportionate to the risk;
4. assess the complete system using fit-for-use data and context-appropriate metrics;
5. document and monitor the system throughout its life cycle.

This does not mean that the model itself is irrelevant. Principle 7 explicitly addresses model and system design, software engineering, interpretability, explainability, predictive performance, generalizability, and robustness. The point is narrower: **model performance alone does not establish regulatory fitness for use.**

The same extraction model, with the same architecture, weights, and headline metric, can carry very different evidentiary burdens depending on its role. A model used to prioritize literature for human review presents a different risk from one whose output becomes an exposure, outcome, eligibility criterion, or confounder in a study supporting a regulatory decision. The model may be unchanged, but the claim made on the basis of its output is not.

### 3.2 Context of use as regulatory pre-specification

Principle 4 is brief but structurally important. A defined context of use supplies the reference point for the proportionality required by Principle 2 and the performance assessment required by Principle 8.

Operationally, this can function like pre-specification. The intended role of the AI technology should be defined before the validation strategy is interpreted against that role. Otherwise, teams may observe favorable model performance first and only then select a use for which that performance appears persuasive.

The analogy to pre-registration is not exact. The document does not prescribe a formal registration process, nor does it state that context of use must be legally fixed before all model development begins. The relevant similarity is one of evidentiary sequence: a prospectively defined purpose makes it possible to judge whether the validation was designed to test fitness for that purpose rather than rationalize a favorable result after the fact.

If the use is selected after performance is known, the subsequent exercise may still produce technically correct metrics. However, it risks becoming post-hoc justification rather than an independent assessment of whether the system is fit for the intended evidentiary role.

### 3.3 A performance metric is an observation, not a conclusion

Principle 8 effectively makes a held-out test-set metric insufficient as a stand-alone deliverable. Two parts of the principle are especially important:

- assessment covers the **complete system, including human–AI interactions**;
- data and metrics must be appropriate for the **intended context of use**.

An AUC of 0.92 is an observed performance result. It is not, by itself, a conclusion that the technology is fit for a regulatory or evidence-generation purpose.

The next questions are therefore:

- What features, proxies, artifacts, or clinical signals produce the observed discrimination?
- Were the development and validation data generated in a way that resembles the intended deployment setting?
- Does aggregate performance conceal relevant subgroup failures?
- Are the chosen metrics aligned with the consequences of false positives and false negatives in the intended use?
- Does the human–AI workflow introduce additional error, inconsistency, automation bias, or opportunities for correction?
- Under what conditions would the model be expected to fail?

This is where a machine-learning benchmark and a regulatory evidence assessment diverge. In a benchmark setting, a metric often functions as the endpoint of comparison. In an evidentiary setting, the metric is one component of a broader credibility assessment.

Principle 8 also suggests an important role for human expertise. The required human contribution need not always involve reviewing every model output. For batch extraction or large-scale phenotyping, case-level human review may be limited or sample-based. In those settings, the critical human role may lie in interpreting performance in light of the data-generating process, intended use, error consequences, and differences between development and deployment populations.

That role requires the multidisciplinary competence described in Principle 5: expertise in both the AI technology and the clinical, scientific, operational, and regulatory context in which its output will be used.

### 3.4 The unresolved question: does the evidentiary use transport?

Once the reasons for model performance are examined, a further question follows:

> Does the model remain fit for the same evidentiary purpose when it is applied in a different site, health system, data environment, or target population?

The principles do not operationalize that question.

Principle 7 includes **generalizability** among the desired properties of good model and system development. Principle 9 gives **data drift** as an example of a life-cycle issue requiring monitoring. However, the document does not distinguish among:

- temporal drift within an existing deployment environment;
- cross-site or cross-institutional variation;
- differences in coding, documentation, measurement, and clinical workflow;
- domain shift between development and deployment data;
- cross-population differences in case mix, disease spectrum, language, access, or care pathways;
- transportability of the model output for a specific downstream evidentiary use.

These are related but not interchangeable problems.

A model may retain acceptable predictive discrimination after transfer while becoming less useful for a particular scientific purpose. For example, an AI-derived variable used as a confounder does not need only to predict the underlying construct. It must measure that construct with sufficient comparability and error properties to support confounding adjustment in the population and data environment where the causal analysis is performed.

If measurement error differs by treatment group, outcome status, site, language, or population, it may not merely reduce precision. It can alter the direction and magnitude of the estimated treatment effect. A stable overall AUC, F1 score, or agreement statistic may not reveal that downstream bias.

The same concern can apply when AI-derived variables serve as:

- study eligibility criteria;
- exposures or treatment classifications;
- outcomes or safety-event phenotypes;
- confounders and effect modifiers;
- censoring indicators;
- trial-matching variables;
- components of target trial emulation;
- inputs to transportability or generalizability analyses.

This is likely a boundary of the document rather than an omission that could reasonably have been resolved in two pages. The principles establish a common vocabulary; they do not provide a methodological framework for every downstream use.

The open regulatory question is therefore not only whether an AI model generalizes, but whether **the validity of the evidentiary claim supported by its output transports**. Future guidance or consensus standards may need to distinguish model-level generalization from use-specific evidentiary transportability.

## 4. Implications for RWE practice

For RWE teams using AI-derived variables, the principles suggest a practical minimum set of questions.

### 4.1 Define the AI contribution to the estimand and analysis

The context of use should state more than “NLP will extract variables” or “machine learning will identify patients.” It should specify:

- the variable being generated;
- its role in the study design and estimand;
- the population, setting, and data source in which it will be used;
- whether it affects eligibility, exposure, outcome, confounding adjustment, censoring, or subgroup definition;
- the regulatory or scientific decision that may rely on it;
- the consequences of relevant errors.

### 4.2 Match performance assessment to downstream risk

The preferred metric depends on the use.

For example:

- an outcome phenotype may require attention to positive predictive value and differential misclassification;
- a screening tool may place greater weight on sensitivity;
- an AI-derived confounder may require assessment of measurement comparability across exposure groups and sites;
- an effect modifier may require reliable measurement across both source and target populations;
- an automated abstraction workflow may require assessment of both model error and reviewer interaction.

### 4.3 Document the complete evidence chain

Traceability should cover:

- source-data provenance;
- data selection and exclusions;
- labeling or annotation procedures;
- preprocessing and feature construction;
- model version and configuration;
- training, tuning, and validation datasets;
- thresholds and decision rules;
- human review or adjudication;
- changes made after deployment;
- the transfer of model outputs into the statistical analysis dataset;
- sensitivity analyses for model-related measurement error.

### 4.4 Treat external validation as use-specific

External validation should not be reduced to reproducing one aggregate metric in a second dataset. It should examine whether the model remains fit for the same context of use, including:

- population and setting differences;
- coding and documentation practices;
- prevalence and spectrum effects;
- subgroup performance;
- calibration where relevant;
- error dependence on treatment, outcome, site, or time;
- the effect of misclassification on the downstream estimate;
- conditions that trigger re-evaluation or retraining.

### 4.5 Monitor both model performance and evidentiary consequences

Life-cycle monitoring may need to include not only data drift and predictive performance but also changes in:

- clinical workflow;
- documentation behavior;
- coding systems;
- treatment patterns;
- outcome prevalence;
- population composition;
- human override patterns;
- downstream effect estimates or phenotype frequencies.

The relevant monitoring plan should follow from the context of use and the risk of the supported claim.

## 5. Cross-references

- **FDA (January 2025) — Considerations for the Use of Artificial Intelligence To Support Regulatory Decision-Making for Drug and Biological Products**: the more operational US document, organized around context of use, model risk, and credibility assessment. *(note pending)*
- **FDA (January 2025) — Artificial Intelligence-Enabled Device Software Functions: Lifecycle Management and Marketing Submission Recommendations**: the device-side treatment of life-cycle management, useful for comparing drug and device regulatory framings. *(note pending)*
- **ICH M14**: a relevant RWE framework within which the fitness and consequences of AI-derived variables used in non-interventional safety studies would need to be considered. *(note pending)*
- **NIST AI RMF / ISO/IEC 42001**: overlapping frameworks for risk management, governance, documentation, monitoring, and accountability; possible sources of the consensus standards invited by the joint principles. *(note pending)*
- **EU AI Act**: the binding EU legal framework. Its relationship with non-binding FDA–EMA principles and sector-specific medicines regulation warrants separate analysis. *(note pending)*

## 6. Watchlist and open questions

- Which body will operationalize these principles first: FDA or EMA through jurisdiction-specific guidance, an international standards organization, ICH, or another collaborative body?
- Will context of use be linked to a formal or semi-formal AI risk-tiering scheme?
- Where will AI-derived exposures, outcomes, confounders, and effect modifiers used in observational studies fall within such a scheme?
- Will future documents distinguish temporal drift, domain shift, population shift, external validation, generalizability, and transportability?
- What evidence will be expected when an AI-derived variable is reused in a new institution, country, language, or health-data system?
- Will regulators require quantitative assessment of how model-related misclassification affects downstream treatment-effect estimates?
- How will the joint principles interact with GxP expectations, the EU AI Act, data-protection requirements, and existing RWE guidance?
- Will consensus standards emerge for version control, change management, revalidation triggers, and audit-ready traceability of AI-derived variables?

## 7. Changelog

- **2026-07-14** — Initial note created.
- **2026-07-14** — Revised to distinguish source summary from professional interpretation; moderated claims concerning algorithm inspection, pre-registration, held-out performance metrics, and data drift; expanded RWE implications and the distinction between model generalizability and evidentiary transportability.
