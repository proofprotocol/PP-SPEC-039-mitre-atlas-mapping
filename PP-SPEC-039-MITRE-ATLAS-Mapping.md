# PP-SPEC-039: Proof of Efficacy Mapping to MITRE ATLAS

| Field | Value |
|---|---|
| Status | DRAFT v0.1 |
| Author | Craig Ellrod, Nebulonium, Inc. (dba HACKERverse®) |
| Date | October 1, 2026 |
| License | CC BY 4.0 |
| Maps to | MITRE ATLAS |
| Series | Proof Protocol Framework Mapping Specifications |

---

## 1. Purpose

This specification defines how MITRE ATLAS adversarial AI tactics, techniques, case context, and related threat information can be bound to Proof Protocol test cases, evidence, and efficacy results.

MITRE ATLAS remains authoritative for its own terminology, identifiers, content, and architecture. This document defines a **Proof Protocol mapping** and does not supersede or modify ATLAS.

## 2. Scope

ATLAS supplies adversarial AI threat context that can identify what should be exercised. Proof Protocol supplies an independent evidence model for determining what happened during a test and whether a selected defensive control performed as claimed.

Independent witnessing and evidence-capture implementation are defined elsewhere in the Proof Protocol specification family.

## 3. Core Question

Proof of efficacy asks:

> **Was there a control, and did it work?**

An ATLAS technique can identify adversarial behavior. A defensive control can claim to prevent or detect that behavior. Proof Protocol binds the technique, test case, control, observed behavior, downstream outcome, and evidence into a result that can be independently examined.

## 4. Metric Definitions

Against a defined adversarial corpus, each case is recorded as **blocked**, **detected**, **missed**, or **INVALID**.

Relevant measurements include:

- containment rate;
- detection rate;
- miss rate;
- false-positive rate against paired benign cases;
- robustness against variants, bypass, suppression, manipulation, or evasion;
- version-level results; and
- INVALID status when required evidence is incomplete or broken.

Target levels are engagement- and risk-specific rather than imposed by this mapping.

## 5. Evidence Produced

Mapped tests can produce:

- **Proof records** binding ATLAS context, test case, control, system/version, verdict, timestamp, and evidence references;
- **ProofStamp™** trusted timestamps bound to evidence/verdict objects;
- **ProofBundle™** packages containing proof records, metrics, corpus manifests, and environment/context;
- **ProofRegister™** records for issued proof artifacts; and
- corpus and environment manifests identifying the tested adversarial conditions.

## 6. Mapping to MITRE ATLAS

| MITRE ATLAS context | Proof Protocol treatment | Evidence |
|---|---|---|
| Tactic | Record the adversary objective as test context. | Corpus/test metadata |
| Technique | Bind the ATLAS technique identifier to one or more reproducible test cases. | Proof record; corpus manifest |
| Sub-technique or variant | Represent the specific adversarial variant exercised. | Test-case evidence |
| Procedure/case context | Use as threat context for independently authored test conditions where applicable. | Corpus metadata |
| Defensive control claim | Record the asserted prevention, detection, or response behavior separately from observed effect. | Control descriptor |
| Technique execution | Capture evidence that the adversarial condition was actually exercised. | Execution evidence |
| Detection outcome | Record whether the control identified the exercised condition. | Detection result |
| Prevention/containment outcome | Determine whether the adversarial objective reached the protected target. | Target/outcome evidence |
| Evasion/bypass variant | Exercise variants intended to defeat or manipulate the control. | Robustness evidence |
| System/version context | Bind material model, control, policy, application, and environment versions to the result. | Environment descriptor |

## 7. Interoperability Rules

1. The relevant ATLAS tactic, technique, sub-technique, or other identifier SHOULD be recorded when applicable.
2. ATLAS identifiers and terminology MUST NOT be silently redefined.
3. Proof Protocol verdicts are Proof Protocol results; they are not MITRE scores, certifications, or endorsements.
4. A control alert or trigger does not by itself establish efficacy when the claim concerns protection of a downstream target.
5. Target, application, SIEM, vendor, or equivalent outcome evidence SHOULD complete the evidence round trip when required to establish the result.
6. Missing required evidence MUST yield **INVALID**, not PASS.
7. Material changes to the tested system, model, control, policy, environment, ATLAS mapping, or corpus SHOULD trigger retesting where they can affect the result.

## 8. Framework-Agnostic Architecture

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks can identify **what to test**: threats, vulnerabilities, techniques, controls, design assertions, identity claims, or risk conditions. Proof Protocol independently establishes **whether the control worked and what evidence proves that result**.

No external framework is required for Proof Protocol to operate. A Proof Protocol implementation MAY use MITRE ATLAS, MAESTRO, OWASP, AIVSS, AAGATE, a proprietary threat model, another recognized framework, or no external framework at all when the test condition is otherwise sufficiently defined.

Adding, replacing, muting, or removing a framework mapping does not alter the Proof Protocol architecture, evidence model, Proof of Efficacy determination, ProofBundle™, ProofStamp™, ProofRegister™, or independent corroboration requirements.

A framework mapping therefore establishes **interoperability**, not architectural dependency.

## 9. Relationship to Proof Protocol

This mapping is part of the Proof Protocol specification family maintained by Nebulonium, Inc.

The relationship is intentionally asymmetric:

> **MITRE ATLAS supplies adversarial AI threat and technique context. Proof Protocol supplies the evidence model for determining whether a selected defensive control performed as claimed.**

No affiliation, endorsement, certification, or sponsorship by MITRE is implied.

## 10. Source Framework, Attribution, and License

MITRE ATLAS is external work maintained by MITRE. MITRE names, ATLAS names, identifiers, trademarks, and expressive framework content remain subject to MITRE's applicable terms.

The public ATLAS data repository has been distributed under the **Apache License 2.0**. Specific MITRE content, marks, websites, or other materials may carry additional or different terms and SHOULD be checked at their authoritative source before reuse.

This Proof Protocol mapping is independently authored and licensed under **CC BY 4.0**. It references ATLAS identifiers and concepts for interoperability and does not relicense MITRE material.

## 11. Versioning

This mapping is versioned independently of MITRE ATLAS. Material upstream changes SHOULD trigger a mapping review and, where necessary, a new version identifying the ATLAS revision mapped.

---

*Proof Protocol · proofprotocol.io · CC BY 4.0*
