# NeoMundi / ASRO — Round 2 Protocol

**Version:** v0.2 (skeleton, sections 1–3, with boundary integrations)
**Status:** Sealed at role-boundary level. Extension to sections 4–7 proceeds via a separate skeleton file (`sections-4-7-skeleton.md`), to be reviewed before any procedural hardening.
**Canonical source:** This Git repository. Tagged commits constitute the pre-registration trace.

---

## Preamble

This document is the canonical methodological protocol for Round 2 of the joint NeoMundi / ASRO collaboration. It is versioned in Git.

**v0.2 covers sections 1–3 only**, with the role boundary between NeoMundi and ASRO crystallized in symmetric form (see Annex A — Boundary crystallization, referenced from Section 3.2).

Sections 4–7 (witness constraints; admissible evidence categories; comparison procedure; formal freeze and signature) are deferred. A minimal structural skeleton for sections 4–7 is maintained in `sections-4-7-skeleton.md` and is **not** part of v0.2's sealed scope.

### Changelog
- **v0.2** — ASRO role definition narrowed (removed ambiguous "execution conditions"); symmetric NeoMundi disclaimer added; three-line boundary crystallization inserted at head of Section 3.2 and reproduced in Annex A; "Independent reviewability" renumbered Q5.
- **v0.1** — Initial skeleton, sections 1–3.

---

## Definitions

**NeoMundi.** Runtime behavioral measurement layer. Produces stability metrics on model outputs (drift, variation, profile classification) without access to model internals. NeoMundi does not provide independent governance attestation, does not perform custody-chain verification, and does not certify infrastructure conditions.

**ASRO.** Independently reviewable infrastructure / governance-state attestation layer. Witnesses and attests to declared system configuration, custody-chain continuity, observer separation, and governance-state conditions relevant to the protocol. ASRO does not measure runtime behavior, does not validate Law E, and does not resolve the correctness of NeoMundi outputs.

**Round 2.** The second joint exercise between NeoMundi and ASRO, framed as a constrained methodology test rather than an outcome-validation exercise.

**Protocol.** This document (`protocol.md`), versioned in Git.

**Pre-registration trace.** The Git timestamp of the commit tagged at formal freeze (defined in section 7, deferred).

---

## Section 1 — Claim limits and explicit non-conclusions

### 1.1 What Round 2 tests

Round 2 does not adjudicate the full theoretical validity of Law E as a measurement instrument. It tests whether a Law E-based runtime measurement process can be made independently reviewable under strong observer-separation and evidence-custody constraints.

### 1.2 Explicit non-conclusions

The following are explicitly outside the scope of what Round 2 can establish, regardless of outcome:

- The general validity of Law E across all model architectures, domains, or input distributions.
- Any claim that NeoMundi's runtime measurement is more or less reliable than alternative measurement frameworks not tested in this round.
- Any claim about ASRO's attestation infrastructure beyond its functioning under the conditions of this protocol.
- Any commercial qualification of NeoMundi or of ASRO (e.g., "rating agency", "certifier", "auditor").
- Generalisation from Round 2 results to runtime behavior under conditions not exercised by the protocol.

### 1.3 What a positive outcome would mean

A positive outcome in Round 2 establishes only that, under the protocol's specific constraints, a Law E-based runtime measurement process and an ASRO-based attestation process can co-exist as independently reviewable evidence layers, with documented observer separation and custody integrity.

### 1.4 What a negative outcome would mean

A negative outcome establishes only that the specific protocol as executed did not satisfy independent reviewability under the stated constraints. It does not falsify Law E, does not invalidate ASRO's attestation infrastructure, and does not preclude a redesigned subsequent round.

---

## Section 2 — Custody structure

### 2.1 Principle

Each artefact (prompt, response, metadata, signature, timestamp) has a defined custodian at each phase of the protocol. No artefact crosses a custodial boundary without an explicit handover event recorded in the protocol log.

### 2.2 Phases

The protocol has three phases:

- **Phase A — Pre-execution.** Artefact preparation, sealing, pre-registration.
- **Phase B — Execution.** Runtime measurement and attestation under frozen conditions.
- **Phase C — Post-execution.** Disclosure, comparison, and review.

### 2.3 Artefact classes

The following artefact classes are recognised by the protocol. Their precise format and sealing procedure are specified in section 4 (witness constraints), deferred.

- Prompt set
- Response set
- NeoMundi measurement output
- ASRO attestation output
- Protocol log
- Pre-registration commit hash

### 2.4 Custody transitions

Each transition between phases produces a custody event recorded in the protocol log. No artefact may be modified after its custody event marks it as sealed.

---

## Section 3 — Observer roles

### 3.1 Principle

The protocol enforces observer separation: no single party holds simultaneous access to all artefacts at any phase. Roles are defined functionally and may be filled by individuals or groups, provided the separation principle is preserved.

### 3.2 Defined roles

> **Boundary crystallization (binding for this section):**
> — NeoMundi measures runtime behavior.
> — ASRO witnesses the reviewability conditions around the measurement process.
> — Neither layer absorbs the other.
>
> This three-line statement governs the interpretation of all role definitions in Section 3.2 and is reproduced in Annex A. Any apparent ambiguity in the role definitions below is to be resolved in favour of this crystallization.

**Prompt curator.** Formulates and seals the prompt set during Phase A. Has no access to NeoMundi or ASRO outputs during Phase B.

**Measurement operator (NeoMundi).** Executes runtime behavioral measurement during Phase B. Has access to the prompt set and response set; produces measurement output. Does not produce attestation output. Does not perform custody-chain verification. Does not certify infrastructure conditions. Does not provide independent governance attestation.

**Attestation witness (ASRO).** Witnesses protocol-defined execution-context and governance-state conditions during Phase B and produces attestation output. Operates independently of the measurement operator. Does not produce runtime behavioral measurement, does not validate Law E, and does not interpret NeoMundi measurement results.

**Reviewer.** Conducts post-hoc comparison during Phase C. Has access to all sealed artefacts after Phase B closure.

### 3.3 Separation constraints

- The prompt curator and the reviewer may be the same party, provided they hold no operational role during Phase B.
- The measurement operator and the attestation witness must be operationally separated during Phase B; they may communicate only through the protocol log.
- No party may modify any artefact after its custody event marks it as sealed.

### 3.4 Phase access matrix

To be specified in v0.3 alongside witness constraints (section 4).

---

## Open boundary questions for v0.2 review

The following questions remain explicitly within scope of the boundary review carried forward from v0.1. Q1 and Q2 are considered addressed by the v0.2 integrations; Q3, Q4, Q5 remain open for review prior to sections 4–7.

1. **ASRO scope.** Is ASRO described in section 3.2 ("attestation witness") in a way that does not collapse it into runtime behavioral instrumentation? Is the asymmetry with NeoMundi's role made explicit enough? *(Addressed in v0.2 via narrowed definition + symmetric disclaimer + boundary crystallization.)*
2. **NeoMundi scope.** Is NeoMundi's measurement role described in a way that does not implicitly absorb attestation duties that belong to ASRO? *(Addressed in v0.2 via symmetric disclaimer in Definitions and Section 3.2.)*
3. **Non-circularity.** Does the custody structure in section 2 introduce any implicit point of circularity (e.g., a single party producing both prompts and review criteria; or a measurement output feeding back into an attestation it should be witnessed by)?
4. **Claim-limit strength.** Are the explicit non-conclusions in section 1.2 strong enough to prevent over-generalisation from a positive outcome — including in third-party communication after execution?
5. **Independent reviewability.** Would the evidence record produced under sections 1–3 (once extended by sections 4–7) be independently reviewable by a third party with no operational role in Round 2?

---

## Annex A — Boundary crystallization

The asymmetry between NeoMundi and ASRO is binding for the entire protocol. It is stated here in canonical form:

> — NeoMundi measures runtime behavior.
> — ASRO witnesses the reviewability conditions around the measurement process.
> — Neither layer absorbs the other.

Any reading of this protocol that absorbs one layer into the other, or that infers from a positive outcome any claim beyond the explicit non-conclusions in Section 1.2, is outside the scope of Round 2 and is not supported by this document.

---

**End of v0.2.** Sections 4–7 maintained as a separate structural skeleton in `sections-4-7-skeleton.md`, pending boundary review.
