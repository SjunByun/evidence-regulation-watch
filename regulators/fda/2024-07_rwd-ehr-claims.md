---
title: "Real-World Data: Assessing Electronic Health Records and Medical Claims Data To Support Regulatory Decision-Making for Drug and Biological Products"
issuer: FDA
domain: [rwe, ai]
doc_type: final-guidance
published: 2024-07
legal_status: non-binding final guidance
jurisdiction: US
source_url: "https://www.fda.gov/media/152503/download"
tags: [rwe, ehr, medical-claims, validation, data-provenance, misclassification, quantitative-bias-analysis, cdm, unstructured-data, ai-derived-variables]
note_status: published
last_reviewed: 2026-07-14
---

# FDA — Assessing EHR and Medical Claims Data for Regulatory Decision-Making (July 2024)

## TL;DR

- **This is one of FDA’s most operationally detailed RWE guidances on data fitness and variable validation.** It provides specific recommendations on data-source assessment, conceptual and operational definitions, validation, misclassification, quantitative bias analysis, traceability, and data quality across the data life cycle.
- **It already contains an explicit AI section.** Section IV.B.5 describes what should be documented when AI, natural language processing, machine learning, or other computerized methods are used to derive study variables from unstructured data.
- **For study-variable ascertainment, an AI extractor functions as, or forms part of, an operational definition.** AI-derived variables therefore remain subject to established expectations for conceptual definition, reference-standard validation, performance assessment, and evaluation of misclassification.
- **Performance is use- and setting-dependent.** FDA states that the performance of an operational definition depends on factors including the data source, study population, study time frame, and reference standard. Prior validation evidence should therefore be assessed for applicability to the proposed study.
- **For AI-derived variables in regulatory RWE studies, this guidance supplies more specific measurement and validation expectations than high-level AI principles alone.** It does not, however, replace AI-specific expectations concerning model development, governance, human–AI interaction, change management, and life-cycle oversight.

## The argument, in four moves

> **Interpretive summary.** The source document is summarized in [Section 2](#2-what-the-document-says). The arguments below are developed in [Section 3](#3-what-it-means-in-practice--an-evidence-generation-reading).

1. **For study-variable ascertainment, an AI extractor is part of the operational definition.**  
   AI does not place a study variable outside the established measurement framework. The variable still requires a clear conceptual definition, an operationalization strategy, appropriate validation, and an assessment of how error could affect study inference.

2. **The RWE framework operationalizes concepts that high-level AI documents express more generally.**  
   Broad concerns such as fitness for use and generalizability become data-source-specific questions about sensitivity, specificity, predictive values, reference standards, population similarity, and implications for bias.

3. **Misclassification is a structural concern in secondary healthcare data.**  
   FDA asks sponsors to consider its degree, whether it is differential or non-differential, whether errors in different variables are dependent or independent, and the direction in which the exposure–outcome association may be biased.

4. **AI may change the mechanism of measurement error rather than eliminate it.**  
   NLP and other computerized methods can recover information that is not available in structured fields, but their errors may vary by site, documentation practice, patient characteristics, treatment group, time, language, or deployment environment. Those errors should be assessed in relation to the downstream evidentiary use.

## 1. Document profile

| | |
|---|---|
| Issuer | FDA — CDER, in cooperation with CBER and the Oncology Center of Excellence |
| Published | July 2024 |
| Legal status | Final guidance containing non-binding recommendations. In FDA guidance, “should” means suggested or recommended, not legally required, unless a specific statutory or regulatory requirement is cited. |
| Length | 34 numbered guidance pages; 39 PDF pages including covers and table of contents |
| Scope | Use of **electronic health records and medical claims data** in clinical studies supporting an FDA regulatory decision on the **effectiveness or safety** of a drug or biological product |
| Study designs covered | FDA uses “clinical studies” broadly to include interventional and non-interventional designs, including studies using RWD as an external control |
| Not covered | Medical devices; recommendations on the choice of study design or statistical analysis; methods for addressing misclassified or missing information; methods for achieving covariate balance |
| Organizing concepts | Data **relevance** and **reliability**, including accuracy, completeness, and traceability |
| Relationship to prior FDA work | Issued as part of FDA’s RWE Program and complements the 2013 guidance on pharmacoepidemiologic safety studies using electronic healthcare data |

## 2. What the document says

### 2.1 Scope and organizing frame: relevance and reliability

The guidance focuses on whether EHR and medical claims data are fit to support a regulatory decision on the effectiveness or safety of a drug or biological product.

FDA organizes this assessment around two broad properties:

- **Relevance**: whether the data contain the key study variables and sufficient numbers of representative patients for the study question.
- **Reliability**: whether the data are accurate, complete, and traceable.

The guidance does not endorse a specific data source or study methodology. Instead, each proposed source should be assessed for the particular study question.

A central procedural recommendation appears in Section III: for studies intended to support an FDA regulatory decision, sponsors should submit the protocol and statistical analysis plan before conducting the study. Essential elements of design, analysis, conduct, and reporting should be predefined, and the protocol and final report should describe how each study element was ascertained from the selected RWD source, including applicable validation studies.

### 2.2 Data sources and their built-in limitations

FDA emphasizes that EHR and medical claims data were generally not developed for research or regulatory submission.

#### Medical claims data

Claims are generated to support payment for care. Potential limitations include:

- diagnoses or procedures may not accurately represent the disease or its comprehensive management;
- coding and transcription practices may differ;
- relevant conditions may be absent or incompletely reflected;
- records can change during run-off and adjudication as claims are adjusted or corrected;
- dispensing and billing information do not necessarily establish actual medication consumption.

#### EHR data

EHR data are generated primarily for clinical care and may also support billing and quality auditing. Their content depends on:

- local clinical and documentation practices;
- EHR functionality and configuration;
- whether care occurs within the contributing healthcare system;
- whether information is recorded in structured or unstructured form;
- whether outside-system care, medication use, or outcomes are captured.

FDA therefore recommends documenting the data source’s prior research use, its ability to capture key study variables, and how those variables can be validated for the proposed research activity.

### 2.3 Relevance across healthcare systems and populations

Healthcare systems and payer environments can differ in medical practice, patient characteristics, formulary restrictions, coverage, out-of-pocket costs, coding systems, and treatment access.

FDA recommends that the protocol explain:

- why the data source and time frame were selected;
- relevant characteristics of the healthcare system;
- prescribing and utilization practices that may affect feasibility or interpretation;
- how healthcare-system factors may affect the generalizability of study findings;
- for non-U.S. sources, why findings are relevant to the U.S. population.

This section concerns the relevance of the data source and the generalizability of the study findings. It should not be conflated with the narrower question of whether a particular operational definition retains the same measurement performance across data sources or populations.

### 2.4 Data capture, linkage, distributed networks, and CDMs

#### Continuity of coverage and care

The capture of patient information depends on interaction with the healthcare system.

- For claims, continuity of coverage should be defined and documented.
- For EHRs, continuity of care within the contributing system or network should be discussed.
- The protocol should describe when patient information is and is not expected to be available.

#### Data linkage

For new linkages within or across sources, the protocol should describe:

- each source and the information contributed;
- linkage methods;
- linkage accuracy and completeness over time;
- the potential effects of probabilistic match quality;
- duplication and fragmentation;
- how linked data are integrated.

When probabilistic linkage is used, the analysis plan should assess the impact of match degree and the robustness of findings.

#### Distributed data networks and common data models

FDA recognizes that a common data model can support standardized queries across sites, but identifies several limitations:

- a CDM generally does not contain all information present in the source systems;
- a CDM may be optimized for particular research purposes;
- some elements may be optional and therefore inconsistently populated across sites;
- mapping and transformation can introduce additional data-quality concerns;
- suitability should be assessed for the proposed study before use.

This is best understood as a warning against assuming that standardization guarantees completeness, semantic equivalence, or fitness for every use.

### 2.5 Computable phenotypes

A computable phenotype identifies a clinical condition or characteristic through a computerized query using defined data elements and logical expressions.

FDA recommends that a computable phenotype include:

- metadata and supporting information;
- the intended use;
- clinical rationale or research justification;
- validation evidence from relevant healthcare settings;
- a protocol and study-report description;
- a computer-processable representation;
- clinical validation information.

A computable phenotype may identify a study population, outcome, or another study variable. Its use does not remove the need for a conceptual definition or validation.

### 2.6 Unstructured data and the explicit AI section (§IV.B.5)

FDA notes that substantial clinical information in EHRs is unstructured, including free-text notes and non-standardized documents such as PDF radiology reports.

The guidance identifies AI-related methods including:

- natural language processing;
- machine learning;
- deep learning;
- computerized extraction of data elements from text;
- algorithms for identifying outcomes;
- evaluation of images or laboratory results.

FDA does not endorse a specific AI technology.

When a protocol proposes AI or another derivation method, FDA recommends specifying:

- assumptions and parameters of the algorithms;
- the data source from which information used to build the algorithm was drawn;
- whether the algorithm was supervised or unsupervised;
- the validation metrics associated with the method.

FDA also states that these methods can involve substantial human-aided curation and decision-making, adding variability and data-quality considerations to the final study-specific dataset. Relevant effects of AI or computerized extraction on data quality should be documented in the protocol and analysis plan.

This section is operational but brief. It does not establish:

- minimum acceptable performance thresholds;
- a mandatory set of validation metrics;
- a required external-validation design;
- model change-control procedures;
- detailed subgroup-performance criteria;
- a prescribed method for propagating extraction error into the final effect estimate.

Those questions must be addressed through the broader validation and data-quality framework in the guidance, other FDA AI documents, applicable standards, and study-specific scientific justification.

### 2.7 Missing information

FDA distinguishes two broad scenarios:

1. information was intended to be collected but is absent — traditional missing data;
2. information was not intended to be collected and is therefore absent — a problem of data-source relevance.

For example, an absent laboratory result may mean:

- the test was not ordered;
- it was ordered but not performed;
- it was performed but not stored or captured;
- it was stored but inaccessible;
- it was lost during curation or transformation.

These mechanisms can have different implications for study validity. Their interpretation may also depend on patient characteristics and clinical decision-making.

### 2.8 The validation framework (§IV.D)

#### Conceptual definition

A conceptual definition reflects current medical and scientific understanding of the variable of interest.

Examples include:

- clinical criteria for a disease or outcome;
- criteria defining inclusion or exclusion;
- the intended construct for a covariate;
- the meaning of exposure, such as drug intake rather than prescription issuance alone.

#### Operational definition

An operational definition specifies how the conceptual variable is obtained from the available data.

It may consist of:

- a code-based algorithm using structured data;
- extraction from unstructured data;
- an algorithm combining structured and unstructured elements;
- additional data collection, such as a patient survey.

#### Implications of imperfection

FDA states that operational definitions are usually imperfect. Misclassification may occur in exposures, outcomes, or covariates and can affect study inference.

Sponsors should consider:

1. the degree of misclassification;
2. differential versus non-differential misclassification;
3. dependent versus independent misclassification;
4. the direction in which the exposure–outcome association may be biased.

For categorical variables, relevant indices may include sensitivity, specificity, positive predictive value, and negative predictive value. For continuous variables, evaluation may use correlation with or pairwise comparison against a reference standard.

### 2.9 Validation approaches

FDA describes several approaches:

- complete verification for all subjects;
- verification of all operationally identified positives or negatives;
- performance assessment in a sample of the proposed study population;
- use of external performance evidence from a prior study.

The appropriate extent of validation depends on:

- the necessary level of certainty;
- feasibility;
- the role of the variable;
- the likely implications of misclassification for study inference.

FDA considers complete verification the most rigorous approach but recognizes that it may not be feasible. A justified sampling strategy and performance assessment may be sufficient in some settings.

### 2.10 Applicability of prior validation evidence

The performance of an operational definition depends on factors including:

- data source;
- study population;
- study time frame;
- reference standard;
- disease, diagnosis, and coding trends.

FDA recommends assessing operational definitions in an adequately large and representative sample of the proposed study population using a justified sampling method.

When prior validation evidence is used:

- the definition should ideally have been assessed in the same data source and a similar population;
- the quality of the prior study should be evaluated;
- compatibility between the prior case definition and the proposed conceptual definition should be assessed;
- the applicability of prior performance measures should be justified;
- newer validation data may be needed when secular changes have occurred;
- sensitivity analyses may be considered.

The guidance does not state that every operational definition must always be revalidated from the beginning. It requires a study-specific justification of whether existing evidence is applicable and whether additional validation is needed.

### 2.11 Quantitative bias analysis

FDA recommends or encourages quantitative approaches, including quantitative bias analysis, to evaluate whether and how misclassification could affect study findings.

This appears in relation to:

- inclusion and exclusion criteria;
- exposure;
- outcomes;
- key covariates, including confounders and effect modifiers.

FDA states that QBA may be used:

- a priori for feasibility assessment;
- to facilitate interpretation of results;
- for both purposes.

The protocol should pre-specify the indices used to quantify bias, such as sensitivity and specificity, and describe how those indices will be measured during validation.

Because this is non-binding guidance, the text does not make QBA legally mandatory in every study. The strength and feasibility of the analysis should be interpreted in relation to the importance of the variable, the likely degree and structure of error, and its implications for study inference.

### 2.12 Application to major study elements

The guidance applies the conceptual-definition → operational-definition → validation logic to:

- study-population selection;
- exposure;
- outcomes;
- covariates and effect modifiers;
- relevant time periods.

#### Exposure

Electronic healthcare data commonly capture prescribing, administration, or dispensing rather than actual medication consumption. Important gaps can include:

- prescriptions filled outside the recorded system;
- low-cost or non-reimbursed products;
- samples;
- nonprescription products;
- dose changes that are not recorded;
- refill gaps and stockpiling;
- uncertainty regarding dose, duration, and adherence.

#### Outcomes

FDA emphasizes:

- whether the outcome is likely to be captured in the data source;
- the tradeoff between false positives and false negatives;
- the need to align the operational definition with the conceptual case definition;
- the inadequacy of PPV alone for some common outcomes;
- the possibility that differential misclassification may bias estimates in either direction;
- the possibility that dependent exposure and outcome errors may produce unexpected bias.

FDA notes that non-differential misclassification often tends toward the null, but cautions against assuming this when multiple error processes are dependent or when actual data-generation mechanisms may produce differential error.

#### Covariates and effect modifiers

Potential confounders that may be absent or imperfectly captured, especially in claims, include:

- race and ethnicity;
- family history;
- smoking, alcohol use, nutrition, and physical activity;
- body mass index;
- drugs obtained without insurance;
- indication for treatment.

The protocol should disclose known unmeasured confounders and effect modifiers, describe any supplemental data strategy, and justify proxies.

For key covariates, FDA recommends providing and justifying the validity of operational definitions. QBA is encouraged where misclassification of key covariates could affect study findings.

### 2.13 Data quality across the data life cycle

FDA treats data quality as an ongoing process rather than a one-time assessment.

The data life cycle may include:

1. accrual from original source data;
2. curation into a repository;
3. transformation and de-identification;
4. warehouse construction;
5. creation of the final study-specific dataset.

The protocol and analysis plan should describe:

- traceability across curation and transformation;
- how those processes may affect data integrity and study validity;
- completeness, conformance, and plausibility;
- QA/QC procedures;
- duplicate and fragmented records;
- changes in coding and data-holder practices;
- structured and unstructured data processing;
- mapping accuracy;
- harmonization across systems;
- modifications from the source to the final analytic dataset.

For AI-derived variables, this means that validation of the extraction model is only one part of the evidence chain. The path from source text or image to the final analysis variable should also be traceable.

## 3. What it means in practice — an evidence-generation reading

> **Interpretive note:** This section is my professional reading of the guidance from an RWE and AI-assisted evidence-generation perspective. It is not language formally stated by FDA.

### 3.1 An AI extractor functions as part of an operational definition

For purposes of study-variable ascertainment, an NLP or machine-learning extractor can be understood as an operational definition, or as one component of a broader operational definition.

For example, an AI-derived smoking variable may depend on:

- the conceptual definition of smoking status;
- source-note eligibility;
- preprocessing;
- the extraction model;
- model version and threshold;
- temporal rules;
- conflict-resolution rules across notes;
- human review or adjudication;
- transformation into the analysis dataset.

The model alone is therefore not the complete operational definition. It is one component in the process that maps source data to the variable used in the study.

This framing is useful because it prevents an AI-derived variable from being treated as a special category exempt from established measurement principles. It still requires:

- a clear target construct;
- documented data provenance;
- an appropriate reference standard;
- validation in a relevant setting;
- fit-for-use performance metrics;
- assessment of error consequences.

At the same time, the operational-definition framework does not replace AI-specific governance. Model-development practices, software controls, versioning, human–AI interaction, security, monitoring, and change management remain relevant.

### 3.2 The RWE guidance adds use-specific measurement detail

High-level AI principles typically use broad concepts such as context of use, risk-based validation, generalizability, robustness, and life-cycle management.

This guidance addresses a narrower but more operational question: whether variables derived from EHR or claims data are sufficiently valid for a particular regulatory study.

It converts broad concerns into study-specific questions:

- What is the conceptual definition?
- How is it operationalized?
- What reference standard is appropriate?
- What are sensitivity, specificity, predictive values, agreement, or measurement error?
- In which data source, population, and time period were these estimated?
- Are those estimates applicable to the proposed study?
- Could error differ across treatment groups?
- Could errors in multiple variables be dependent?
- How could the error change the estimated association?

The two frameworks are complementary. The AI framework addresses the technology and system; the RWE framework addresses the validity of the variable and its role in study inference.

### 3.3 Measurement portability is not identical to causal transportability

The guidance states that operational-definition performance may vary by data source, population, time frame, and reference standard. This is closely related to the question of whether a measurement procedure remains valid after transfer to a new environment.

It is useful to call this **measurement portability** or **measurement transportability**, but it should not be confused with causal transportability.

- **Measurement transportability** asks whether a variable is measured with comparable meaning and error properties in another setting or population.
- **Causal transportability** asks whether an estimated treatment effect can be generalized or transported from a source population to a target population under assumptions about effect modifiers, selection, and exchangeability.

The first can affect the second. If an AI-derived confounder or effect modifier is measured differently in the source and target populations, the downstream transport analysis may be biased even when the causal transportability method is otherwise correctly specified.

The guidance does not provide a formal transportability framework. It does, however, provide measurement-level questions that should be answered before assuming that a validated operational definition can be carried unchanged into another database, site, country, or population.

### 3.4 Misclassification is a structural concern, not an exceptional failure

In traditional trials, protocolized exposure assignment, scheduled assessments, and prespecified data collection can reduce some sources of measurement variability. Randomization addresses confounding, however; it does not by itself prevent exposure, outcome, or covariate misclassification.

In studies using secondary healthcare data, ascertainment is not generally imposed by a research protocol. Study variables must be constructed from information generated during care, billing, documentation, and data transformation.

As a result, the validity of the operational definition is central to internal validity. The relevant question is not whether error exists, but:

- how much error exists;
- how it was measured;
- whether it differs by exposure, outcome, site, or patient characteristics;
- whether errors in different variables are related;
- whether the resulting bias could change the study conclusion.

This is why FDA’s repeated discussion of QBA is important. The guidance does not mandate QBA in every study, but it makes clear that qualitative acknowledgment alone may be insufficient when misclassification of a key variable could materially affect inference.

### 3.5 AI may alter rather than remove measurement error

Claims, EHRs, CDMs, and AI-derived variables have different error mechanisms.

#### Claims

Because claims are generated for payment and administration rather than research, recorded codes may reflect billing rules, coding practices, and operational processes as well as clinical status.

Depending on how those practices relate to treatment, site, severity, or intensity of care, error may be systematic and could become differential.

#### EHRs

EHRs may contain richer clinical information, but capture depends on:

- whether the patient receives care within the system;
- what clinicians choose or are able to document;
- workflow and EHR configuration;
- testing and follow-up intensity;
- care setting and specialty;
- billing and quality-reporting practices.

EHR data are therefore not free from systematic measurement processes.

#### Common data models

CDM transformation can improve standardization and reproducibility but may:

- omit source detail;
- leave optional elements unpopulated;
- alter granularity;
- introduce mapping error;
- remove context needed for interpretation.

A blank or absent field may reflect true absence, non-collection, non-mapping, or loss during transformation. These mechanisms should not be treated as interchangeable.

#### AI extraction

NLP and other AI methods may reduce reliance on billing codes and recover clinical detail from notes, reports, images, or laboratory information.

They may also introduce errors associated with:

- documentation density;
- site-specific language and templates;
- disease severity;
- clinician specialty;
- treatment-related monitoring;
- population or language differences;
- model thresholds and version changes;
- annotation and reference-standard quality;
- human review and adjudication.

Therefore, AI-derived variables do not lessen the need for misclassification analysis. In some settings, they may make the relevant error structure more difficult to characterize.

It is not generally correct to assume that AI-derived variables are more or less valid than code-based definitions. The comparison is empirical and use-specific.

### 3.6 What should be validated for an AI-derived variable

A regulatory RWE protocol using an AI-derived study variable should consider documenting at least the following.

#### Construct and use

- conceptual definition;
- role in the study: eligibility, exposure, outcome, covariate, effect modifier, censoring, or other use;
- intended context of use;
- consequences of false positives, false negatives, and continuous measurement error.

#### Source and derivation

- source-data type and provenance;
- inclusion and exclusion of notes, reports, images, or records;
- preprocessing;
- algorithm assumptions and parameters;
- training and development source;
- supervised or unsupervised approach;
- annotation and adjudication process;
- model version, threshold, and decision rules;
- human involvement.

#### Validation

- reference standard and its limitations;
- sampling design;
- sample size and representativeness;
- sensitivity, specificity, PPV, NPV, calibration, agreement, or continuous-error measures as appropriate;
- subgroup and site-level performance where relevant;
- performance by exposure or outcome status when differential misclassification is plausible;
- applicability of prior validation evidence;
- temporal validity and revalidation triggers.

#### Downstream inference

- how the AI-derived variable enters the estimand and analysis;
- whether its error could differ across treatment groups or sites;
- whether its error is related to error in other variables;
- sensitivity analyses or QBA;
- assumptions used to parameterize the bias analysis;
- interpretation of results under plausible error scenarios.

#### Traceability and change control

- transfer of model outputs into the study-specific dataset;
- handling of missing, conflicting, or uncertain outputs;
- software and model versioning;
- updates during the study;
- reprocessing rules;
- audit trail;
- QA/QC and reproducibility.

### 3.7 What satisfying the AI principles would not establish by itself

A sponsor could follow high-level AI principles on context of use, risk-based validation, provenance, transparency, and life-cycle monitoring without fully addressing the study-variable questions in this RWE guidance.

For an AI-derived variable, the RWE-specific questions remain:

- What clinical or scientific construct is being measured?
- How is the construct operationalized?
- What is the reference standard?
- Where and in whom was performance assessed?
- Are the performance estimates applicable to the proposed study?
- Could error be differential or dependent?
- How might it affect the exposure–outcome association?
- What quantitative indices or sensitivity analyses will be prespecified?

This does not make the RWE guidance legally or hierarchically “stricter” than the AI documents. The documents operate at different levels and address overlapping but distinct objects:

- the **AI system and its governance**;
- the **study variable and its evidentiary consequences**.

A team using AI-derived variables in regulatory RWE should therefore read both document families.


## 4. Cross-references

- **[FDA–EMA — Guiding Principles of Good AI Practice in Drug Development (January 2026)](2026-01_fda-ema-good-ai-practice.md)** — high-level AI principles covering context of use, risk, performance assessment, data governance, and life-cycle management.
- **FDA — Considerations for the Use of Artificial Intelligence To Support Regulatory Decision-Making for Drug and Biological Products (January 2025, draft)** — FDA’s AI credibility framework for drug and biological product regulatory decision-making. *(note pending)*
- **ICH M14** — international guidance for non-interventional studies of the safety of medicines; relevant to protocol design, data fitness, variable definitions, and validation. *(note pending)*
- **FDA — Real-World Data: Assessing Registries to Support Regulatory Decision-Making for Drug and Biological Products (December 2023)** — parallel guidance for registry data sources. *(note pending)*
- **FDA — Considerations for the Design and Conduct of Externally Controlled Trials for Drug and Biological Products (February 2023, draft)** — related considerations where RWD are used as external controls. *(note pending)*

## 5. Changelog

- **2026-07-14** — Initial note created.
- **2026-07-14** — Revised against the July 2024 final guidance to distinguish FDA recommendations from professional interpretation; removed legally suggestive language such as “binding constraint”; clarified that AI extraction forms part of an operational definition rather than exhausting it; distinguished measurement portability from causal transportability; moderated claims about claims, CDMs, and NLP; and expanded the protocol checklist.
