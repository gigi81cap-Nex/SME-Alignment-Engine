# Claims & Non-Claims (v0.1.0-alpha)

This section prevents over-interpretation and scope creep.

## Claims (Verifiable)
1. The framework targets **high-criticality silent failures** where outputs appear coherent but violate physical/legal/procedural constraints.
2. Provides a **cross-domain error taxonomy** (e.g., COMP-01, RISK-04) for standardized classification.
3. Establishes **Constraint Adherence** as a primary objective over linguistic quality.
4. Defines quantifiable metrics: **RCHH**, **SME-AS**, **FCR**.
5. Uses **error abstraction** to focus on failure classes rather than isolated outputs.
6. Treats SME criteria as **operational ground truth** for evaluation and data curation.
7. Designed to support **human data pipelines** (RLHF/DPO) and evaluation/regression testing.
8. Includes explicit detection of **externalized harm** cases (RISK-04), including downstream consequences.

## Non-Claims (Limitations)
1. Not a prompt engineering guide.
2. Does not claim elimination of all hallucinations.
3. Does not resolve pure knowledge gaps; focuses on constraint-grounding failures.
4. Not an autonomous training system; requires integration into existing pipelines.
5. Not aimed at improving style, fluency, or creativity.
6. Does not replace final SME oversight in high-liability deployments.
7. v0.1.0-alpha is a **protocol definition**, not production-certified tooling.
8. Not generic probabilistic calibration; FCR is scoped to safety-critical triggers.
