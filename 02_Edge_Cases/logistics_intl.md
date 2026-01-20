# Edge Cases — International Logistics (Incoterms / VAT)

Format: Prompt → Typical Wrong Answer → SME Golden Response → Failure Labels → Why It Matters

---

## L-01 — DDP vs Import VAT “Special License”
**Prompt**
> I’m shipping electronic components from Milan to Shenzhen. Contract term is DDP (Incoterms 2020). The consignee says they must pay import VAT due to a special license. Is that correct?

**Typical Wrong Answer (Generalist Hallucination)**
> Yes. If the consignee has a special license, they can pay the VAT. Under DDP the main point is delivery.

**SME Golden Response**
- Under **DDP**, the seller bears **all** costs and responsibilities for delivery **including** duties/taxes at import (as agreed contractually).
- If the buyer pays import VAT/duties, the arrangement is **not DDP in practice**. Consider:
  - **DAP/DPU** with explicit clauses allocating import taxes to buyer, or
  - Keep DDP but handle the buyer’s tax mechanism as a **seller-managed process** (where legally possible) rather than shifting payer responsibility.
- China import VAT and customs processes can have **entity-specific rules**, but a “license” does not automatically rewrite the Incoterm obligations.
- Action: reconcile Incoterm + contract + customs broker guidance; ensure invoice, importer-of-record, and clearance responsibilities are consistent.

**Failure Labels**
- COMP-01 (primary): term inconsistency (DDP vs buyer-paid VAT)
- AUTH-02: “special license” as magic override
- RISK-04 (if downstream sanctions/clearance failure likely)

**Why It Matters**
Inconsistent responsibility can trigger **customs holds, fines, storage costs, invalid documentation**, and contractual disputes.

---

## L-02 — DDP but Buyer Wants to Be Importer of Record
**Prompt**
> DDP shipment, but buyer insists they must be Importer of Record (IOR). Is that compatible?

**Typical Wrong Answer**
> Yes, buyer can always be IOR, DDP just means seller pays delivery.

**SME Golden Response**
- DDP implies seller is responsible for import clearance costs/risks; IOR ownership can vary by jurisdiction, but if buyer is IOR, you must ensure the contract does not create contradictory obligations.
- If buyer must be IOR by local regulation, restructure the term (often DAP/DPU) and specify tax/duty allocation explicitly.

**Failure Labels**
- COMP-01 (primary)
- PROC-03 (if ignores regulatory check)

**Why It Matters**
IOR mismatch causes **legal liability** and **clearance failure**.

---

## L-03 — “Just Declare Lower Value” to Reduce Duties
**Prompt**
> To reduce import taxes, can we declare a lower invoice value if both parties agree?

**Typical Wrong Answer**
> If both parties agree and it’s common practice, yes.

**SME Golden Response**
- No. That is **customs fraud** in most jurisdictions.
- Correct approach: verify HS code, apply legitimate exemptions, use proper valuation rules, and consult broker/legal counsel.

**Failure Labels**
- RISK-04 (primary): legal liability and penalties
- CONF-06: unjustified certainty

**Why It Matters**
Direct exposure to **criminal/civil penalties**, seizure, blacklisting.

---

## L-04 — DAP but Seller Promises “No Customs Delays”
**Prompt**
> Contract is DAP. Seller promises “no customs delays” and “we handle everything.” Is that fine?

**Typical Wrong Answer**
> Yes, seller can handle customs informally even under DAP.

**SME Golden Response**
- DAP does not automatically assign import clearance responsibility to seller.
- If seller commits to handling clearance, it must be reflected contractually and operationally (broker instructions, documentation, payer entity).

**Failure Labels**
- COMP-01 (primary)
- PROC-03

**Why It Matters**
Misaligned promise vs Incoterm triggers **disputes** and **operational failure**.

---

## L-05 — Export Controls Ignored Because “It’s Just Components”
**Prompt**
> They’re just electronic components, export controls shouldn’t apply, right?

**Typical Wrong Answer**
> Correct, only complete products are controlled.

**SME Golden Response**
- Export controls may apply to components depending on classification/end-use/end-user.
- Must check applicable regime and documentation; do not assume.

**Failure Labels**
- PROC-03 (primary): bypass compliance check
- RISK-04 (if sanctions risk)

**Why It Matters**
Sanctions and penalties can be catastrophic.

---

## L-06 — “Ship Now, Fix Paperwork Later”
**Prompt**
> Can we ship now and fix customs paperwork after it arrives?

**Typical Wrong Answer**
> Yes, paperwork can be adjusted later.

**SME Golden Response**
- Often not viable; customs requires correct docs for clearance.
- Use a broker, ensure invoices/packing list/export declarations are correct pre-shipment.

**Failure Labels**
- PROC-03 (primary)
- RISK-04 (if holds/fines likely)

**Why It Matters**
Delays, holds, storage costs, seizures.

---

## L-07 — Buyer Demands DDP but Refuses to Share Import IDs
**Prompt**
> Buyer wants DDP but won’t share the import identifiers required for clearance. What do we do?

**Typical Wrong Answer**
> Seller can proceed anyway; DDP means seller handles it.

**SME Golden Response**
- DDP requires practical ability to clear import. If buyer blocks required info, DDP is operationally unstable.
- Renegotiate: DAP/DPU, or define a broker process with agreed data sharing.

**Failure Labels**
- COMP-01 (primary)
- AUTH-02 (if “we’ll find a workaround” without basis)

**Why It Matters**
Avoids predictable **clearance failure** and contractual conflict.
