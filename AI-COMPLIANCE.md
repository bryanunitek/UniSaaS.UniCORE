# AI Compliance

**What this document covers:** the UniCORE AI compliance infrastructure — the architectural posture, the EU AI Act Annex III alignment, and the governance primitives that any Vertical CORE built on UniCORE inherits.

**What this document does not cover:** jurisdiction-specific AI regulatory filings, national supervisory authority registrations, or Vertical CORE-specific AI compliance business processes. Those live with the Vertical CORE and its operating jurisdiction.

---

## Status

This document describes the **Tier-3 AI Compliance** infrastructure as implemented in the UniCORE substrate. The eight EU AI Act service modules (Articles 11, 12, 13, 14, 15, 17, 72, and Annex IV technical documentation) are implemented and registered in the substrate. They are available to every Vertical CORE built on UniCORE.

The 2026-08-02 date for Annex III §8(a) obligations is noted below.

---

## EU AI Act context

The EU AI Act classifies AI systems used in **law firms and legal practice** as **high-risk** under **Annex III §8(a)**:

> AI systems intended to be used in the context of the administration of justice and democratic processes.

The classification activates the following obligations for any AI system operating in support of legal practice within EU jurisdiction or for EU-affected persons:

| Article | Obligation | UniCORE status |
|---|---|---|
| Art. 9 | Risk management system | ✅ Substrate implemented |
| Art. 10 | Data governance | ✅ Substrate implemented |
| Art. 11 | Technical documentation | ✅ Substrate implemented |
| Art. 12 | Records of operation | ✅ Substrate implemented |
| Art. 13 | Transparency | ✅ Substrate implemented |
| Art. 14 | Human oversight | ✅ Substrate implemented |
| Art. 15 | Accuracy, robustness, cybersecurity | ✅ Substrate implemented |
| Art. 17 | Quality management system | ✅ Substrate implemented |
| Art. 72 | Post-market monitoring | ✅ Substrate implemented |
| Annex IV | Technical documentation | ✅ Substrate implemented |

The **Annex III §8(a) obligations come into Force on 2026-08-02**. Systems deployed in support of legal practice must be compliant from that date.

---

## The eight AI compliance service modules

Each module is implemented as a `Default*` class registered via `AddAiComplianceServices()`. Hosts can replace any module with a custom implementation before calling this method.

### Article 11 — Risk Management System

```
IArticle11RiskManagementSystem.RunCycle(inputs) → Article11RiskManagementCycleEnvelope
```

Runs the four-step iterative risk management cycle required by Art. 11:

1. Identification and analysis of known and foreseeable risks to health, safety, and fundamental rights.
2. Estimation and evaluation of risks arising from intended use and reasonably foreseeable misuse.
3. Evaluation of risks based on post-market monitoring data (Art. 72).
4. Adoption of targeted risk management measures.

The cycle envelope captures each run's state for downstream attestation and Annex IV §3 inclusion.

### Article 12 — Records of Operation

```
IArticle12OperationsLogValidator.Validate(logEntries) → Article12ValidationResult
```

Validates that operation logs contain the minimum required data points specified by Art. 12(1): purpose of the AI system, the categories of data processed, tracing the system's behaviour against inputs and outputs, and the key parameters of the system's functioning.

The validator does not store logs — it validates log completeness against the required schema. Log storage is the host's responsibility.

### Article 13 — Transparency

```
IArticle13TransparencyDocumentBuilder.Build(inputs) → Article13TransparencyDocument
```

Produces the transparency disclosure document required by Art. 13. The document covers: provider identity, system characteristics, intended purpose, input data specifications, output interpretability measures, human oversight mechanisms, and any predetermined changes to the system.

Transparency documents are consumed by the bill renderer and the audit trail.

### Article 14 — Human Oversight

```
IArticle14HumanOversightAssessment.Assess(inputs) → Article14OversightAssessmentResult
```

Evaluates whether the human oversight measures designed into the system are sufficient for the system's risk profile. Assesses: technical measures for human oversight, the clarity and actionability of the override-and-explain UI, the designation and training of oversight roles, and the escalation paths for high-severity outputs.

### Article 15 — Accuracy, Robustness, and Cybersecurity

```
IArticle15AccuracyRobustnessCybersecuritySubstrate.Validate(inputs) → Article15ValidationResult
```

Validates that the system meets the accuracy, robustness, and cybersecurity standards specified by Art. 15. Addresses: accuracy metrics and their measurement methodology, robustness to adversarial inputs and distribution shift, cybersecurity controls, and incident response procedures.

### Article 17 — Quality Management System

```
IArticle17QualityManagementSystem.Validate(qmsInputs) → Article17QmsResult
```

Evaluates the quality management system against Art. 17 requirements. Covers: documented procedures, change management, incident reporting, and continuous improvement processes.

### Article 72 — Post-Market Monitoring

```
IArticle72PostMarketMonitoring.Evaluate(marketData) → Article72MonitoringReport
```

Evaluates post-market data to identify new or changed risks, update the risk management system (Art. 11), and trigger the Article 9 cycle update. The report is consumed by the Art. 11 cycle envelope.

### Annex IV — Technical Documentation

```
IAnnexIvTechnicalDocumentationBuilder.Build(articleEnvelopes) → AnnexIvTechnicalDocumentation
```

Produces the complete technical documentation package required by Annex IV. The documentation is assembled from the outputs of Articles 11 through 17 and is the deliverable that regulators may request.

---

## The compliance envelope pattern

All eight modules produce structured envelopes (`*Envelope`, `*Document`, `*Result`) rather than unstructured strings. This means:

- Every compliance output is **machine-readable** and **attestable**.
- The outputs can be assembled into the Annex IV technical documentation package automatically.
- The attestation surface (`IBadgeConformanceCheck`) can reference compliance state without re-executing the full module suite.
- Compliance evidence is **versioned with the substrate** — the exact inputs and outputs for each compliance run are preserved.

---

## Relationship to the badge certification

The badge certification check (`IBadgeConformanceCheck`) verifies five criteria. The AI compliance infrastructure provides the **evidence** that the badge claim is honest:

- The compile-time floor (`UniCoreLawClawCompileTimeFloor`) proves the AI governance substrate was compiled into the system.
- The nine invariants prove the governance architecture is in place.
- The AI compliance service modules prove the regulatory obligations are covered by the substrate.

A system that asserts the UniCORE badge but does not wire the AI compliance services would fail the badge conformance check — because the conformance check requires `ITrueAiAttributionService` to be resolvable, and that service's `ProgrammeDescription` must reference the Nine Invariants.

---

## Relationship to EU AI Act obligations

UniCORE provides the **substrate infrastructure** for AI compliance. It does not provide:

- Registration with a national supervisory authority.
- A legal opinion that a specific deployment is compliant.
- Jurisdiction-specific interpretation of "high-risk" classification outside Annex III §8(a).

Those are matters for the Vertical CORE producer, the host operator, and their legal counsel.

The substrate is designed so that a Vertical CORE producer operating under different jurisdictional regimes can replace any module with a jurisdiction-specific implementation without affecting the other seven.

---

## Version

| Version | Date | Change |
|---|---|---|
| 1.0 | June 2026 | First publication. Describes Tier-3 AI Compliance as implemented in the UniCORE substrate, covering all eight EU AI Act service modules and the 2026-08-02 Annex III §8(a) in-force date. |
