# PP-SPEC-039: Proof of Efficacy Mapping to MITRE ATLAS

**Status:** DRAFT v0.1  
**Author:** Craig Ellrod / Nebulonium, Inc. / HACKERverse®  
**License:** CC BY 4.0

**Normative specification:** [`PP-SPEC-039-MITRE-ATLAS-Mapping.md`](./PP-SPEC-039-MITRE-ATLAS-Mapping.md)

## Purpose

This repository defines a Proof Protocol mapping between MITRE ATLAS and Proof Protocol evidence, efficacy, and proof semantics.

MITRE ATLAS is treated as a pluggable source of adversarial AI threat and technique context. Proof Protocol remains framework-agnostic and independently establishes whether a selected control performed as claimed.

## Repository contents

- `PP-SPEC-039-MITRE-ATLAS-Mapping.md` — normative mapping specification
- `README.md` — repository overview
- `LICENSE` — license for original Proof Protocol material
- `CONTRIBUTING.md` — contribution guidance
- `CITATION.cff` — citation metadata

## Architectural principle

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks identify what may be tested. Proof Protocol independently establishes whether a control worked and what evidence proves the result.

## Ownership and external-framework notice

The Proof Protocol mapping is independently authored. MITRE, ATLAS, associated names, identifiers, trademarks, and upstream materials remain subject to their respective ownership and licensing. Mapping establishes interoperability, not dependency, endorsement, or transfer of ownership.
