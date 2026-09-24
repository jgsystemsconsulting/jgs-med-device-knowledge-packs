# Capability to Knowledge-Pack Map

Working artifact mapping sector technical capabilities to the pack chapters that provide
reference depth for each capability. Empty-tree template seed: no content packs yet.

Rules of construction:
- Every chapter in every pack under `packs/<slug>/chapters/` is assigned to exactly one capability cluster (best fit).
- Signpost packs contain no chapters and are not mapped.
- Machine-readable version: `docs/capability-pack-map.json`.
- Machine-readable classification rules: `docs/classification-rules.json`.
- Changelog (v0.1.0): empty-tree template seed.

## Summary

| Cluster | Entries |
|---|---|
| 1. Regulatory Landscape & Pathways | 5 |
| 2. Premarket Software Documentation | 2 |
| 3. Software Validation & Assurance | 2 |
| 4. Quality Management System | 1 |
| 5. Cybersecurity | 2 |
| 6. Software Function Scope | 2 |
| **Total** | **14** |

## 1. Regulatory Landscape & Pathways

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| fda-med-device | ch01-regulatory-landscape.md | FDA device pathways overview: 510(k), De Novo, PMA and where software functions fit |
| fda-med-device | ch10-software-changes-510k.md | Decision framework for when a software change triggers a new 510(k) |
| fda-med-device | ch12-submissions-estar.md | eSTAR template structure and mandatory electronic-submission dates |
| fda-med-device | glossary.md (support file) | Shared FDA device-software terms used across the pack |
| fda-med-device | cheatsheet.md (support file) | Cross-chapter decision checklists for device software questions |

## 2. Premarket Software Documentation

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| fda-med-device | ch02-premarket-software-documentation.md | Basic vs Enhanced documentation levels and premarket software content |
| fda-med-device | ch09-premarket-cyber-documentation.md | Assembling the cybersecurity section of a premarket submission |

## 3. Software Validation & Assurance

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| fda-med-device | ch03-software-validation.md | GPSV validation principles minus the CSA-superseded section 6 |
| fda-med-device | ch04-computer-software-assurance.md | Risk-based CSA for production and quality-system software |

## 4. Quality Management System

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| fda-med-device | ch05-qmsr-quality-management.md | QMSR obligations under 21 CFR 820 after the 2026-02-02 transition |

## 5. Cybersecurity

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| fda-med-device | ch06-cybersecurity-qms.md | Secure product development framework and postmarket cyber QMS processes |
| fda-med-device | ch07-cybersecurity-premarket.md | Premarket cyber content: threat modelling, SBOM, security requirements, labelling |

## 6. Software Function Scope

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| fda-med-device | ch08-software-function-scope.md | OTS/SOUP expectations and MDDS software-function device boundaries |
| fda-med-device | ch11-clinical-decision-support.md | CDS device vs non-device criteria and the four-criteria test |
