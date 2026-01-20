# SME-Alignment-Engine (v0.1.0-alpha)

A text-only framework for reducing **high-criticality silent failures** in reasoning LLMs by grounding outputs in **non-negotiable real-world constraints**.

## Problem
Reasoning models can produce outputs that look coherent and confident while violating:
- **Physical constraints** (reality)
- **Safety protocols** (SDS/HSE procedures)
- **Legal/contractual constraints** (e.g., Incoterms)

These are **silent failures**: they do not look like “errors” to non-experts, but can trigger real harm (injury, liability, financial loss).

## Core Principles
- **Constraint adherence > linguistic quality**
- **SME judgment = operational ground truth**
- Failures are treated as **error classes**, not isolated mistakes
- **Zero tolerance** for severity ≥ 9 failures (binary pass/fail)

## Repository Structure
- `01_Taxonomy/`  
  Universal cross-domain error classes with severity (8–10), tie-breakers, and a fixed constraint hierarchy.
- `02_Edge_Cases/`  
  SME-style edge case prompts and golden responses across:
  - International logistics (Incoterms / VAT)
  - Industrial safety (equipment / procedures)
  - HSE compliance (SDS-driven responses)
- `03_Evaluation_Metrics/`  
  Formal evaluation metrics:
  - **RCHH** (Reduction in Critical Hallucinations, severity ≥ 9)
  - **SME-AS** (SME-Alignment Score, weighted)
  - **FCR** (False Confidence Rate)
- `04_Claims_and_Limits/`  
  Explicit claims and non-claims to prevent scope creep and over-interpretation.

## Intended Use
This repo is designed as a **criterion layer** for:
- Human data pipelines (RLHF/DPO data curation)
- Evaluation suites / regression testing
- Safety-oriented reasoning audits in high-liability domains

No tooling is included in v0.1.0-alpha by design.

## Keywords
LLM safety, reasoning failures, constraint violation, critical hallucination, SME ground truth, safety engineering, evaluation metrics, taxonomy
