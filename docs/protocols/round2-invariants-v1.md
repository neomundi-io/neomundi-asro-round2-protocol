# NeoMundi / ASRO — Round 2 Protocol Invariants

**Version:** invariants-v1
**Status:** Role-boundary freeze candidate
**Scope:** Stable drafting constraints for Round 2 Sections 4–7
**Note:** This file freezes the protocol invariants only. It does not freeze procedural implementation details.

---

## 1. Purpose

This file defines the stable constraints that govern all subsequent drafting of the NeoMundi / ASRO Round 2 protocol.

Sections 4–7 must flow from these invariants. They must not reopen, dilute or extend the role boundary established in the protocol.

---

## 2. Role boundary

The following separation of roles governs Round 2:

* **NeoMundi** measures runtime behavioral signals.
* **ASRO** witnesses the reviewability conditions around the measurement process.
* **The Reviewer** performs a bounded post-hoc examination of sealed artefacts.
* No layer absorbs, certifies or substitutes for another layer.

---

## 3. Explicit non-conclusions

Round 2 does not establish that:

* ASRO certifies NeoMundi;
* ASRO validates the NeoMundi runtime behavioral signal;
* NeoMundi certifies ASRO infrastructure;
* NeoMundi measures governance-state truth;
* ASRO adjudicates runtime behavioral truth;
* the Reviewer extends conclusions beyond the protocol scope;
* the protocol proves regulatory compliance;
* one Round 2 execution constitutes full industrial validation;
* the protocol proves universal validity of the NeoMundi measurement model.

---

## 4. Drafting sequence

Sections 4–7 must be drafted and reviewed in the following order:

1. **Witness constraints**
2. **Admissible evidence categories**
3. **Comparison procedure**
4. **Formal freeze and signature**

Each section depends on the prior section being sufficiently stable. Later sections must not redefine earlier boundaries.

---

## 5. Independence constraint

NeoMundi outputs and ASRO outputs may appear within the same evidence record, but they must remain evidence of distinct facts.

The protocol must not collapse runtime behavioral measurement and governance-state witnessing into a single validation layer.

---

## 6. Reviewer constraint

The Reviewer may compare sealed artefacts only within the bounded scope of the frozen protocol.

The Reviewer must not:

* infer certification;
* extend the protocol claims;
* adjudicate runtime behavior through governance attestation;
* adjudicate governance state through runtime measurement;
* reinterpret an explicit non-conclusion as a conclusion.

---

## 7. Freeze rule

Once the complete Round 2 protocol is formally frozen before execution:

* no substantive amendment may be introduced into the frozen version;
* any corrective change requires a new version;
* the new version must be documented and pre-registered before a subsequent execution;
* the prior version remains preserved as part of the audit trail.

---

## 8. Open implementation questions

The following elements remain intentionally unresolved pending ASRO review:

* timestamping mechanism;
* signature mechanism;
* witness eligibility criteria;
* custody-chain requirements;
* final admissible evidence taxonomy;
* detailed comparison logic;
* response to inconsistency between artefacts;
* operational separation requirements for the final signature event.

---

## 9. Scope of this freeze candidate

This document freezes the drafting boundary only.

It does not freeze:

* procedural logic;
* infrastructure implementation;
* evidence schemas;
* artefact formats;
* operational workflows;
* final signatures;
* execution dates.
