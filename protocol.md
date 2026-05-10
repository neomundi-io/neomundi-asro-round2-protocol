# NeoMundi / ASRO — Round 2 Protocol

**Version:** v0.1 (skeleton, sections 1–3)
**Status:** Draft — under boundary review by ASRO before extension to sections 4–7.
**Canonical source:** This Git repository. Tagged commits constitute the pre-registration trace.

---

## Preamble

This document is the canonical methodological protocol for Round 2 of the joint NeoMundi / ASRO collaboration. It is versioned in Git.

v0.1 covers sections 1–3 only:

- Section 1 — Claim limits and explicit non-conclusions
- Section 2 — Custody structure
- Section 3 — Observer roles

Sections 4–7 (witness constraints; admissible evidence categories; comparison procedure; formal freeze and signature) are deferred to v0.2 and beyond, pending boundary review on this skeleton.

---

## Definitions

- **NeoMundi.** Runtime behavioral measurement layer. Produces stability metrics on model outputs (drift, variation, profile classification) without access to model internals.
- **ASRO.** Independently reviewable infrastructure / governance-state attestation layer. Witnesses and attests to system configuration, custody chains, and execution conditions.
- **Round 2.** The second joint exercise between NeoMundi and ASRO, framed as a constrained methodology test rather than an outcome-validation exercise.
- **Protocol.** This document (`protocol.md`), versioned in Git.
- **Pre-registration trace.** The Git timestamp of the commit tagged at formal freeze (defined in section 7, deferred).

---

## Section 1 — Claim limits and explicit non-conclusions

### 1.1 What Round 2 tests

Round 2 does not adjudicate the full theoretical validity of Law E as a measurement instrument. It tests whether a Law E-based runtime measurement process can be made independently reviewable under strong observer-separation and evidence-custody constraints.

### 1.2 Explicit non-conclusions

The following are explicitly **outside** the scope of what Round 2 can establish, regardless of outcome:

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

The following artefact classes are recognised by the protocol. Their precise format and sealing procedure are specified in section 4 (witness constraints), deferred to v0.2.

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

- **Prompt curator.** Formulates and seals the prompt set during Phase A. Has no access to NeoMundi or ASRO outputs during Phase B.
- **Measurement operator (NeoMundi).** Executes runtime behavioral measurement during Phase B. Has access to the prompt set and response set; produces measurement output. Does not produce attestation output.
- **Attestation witness (ASRO).** Witnesses execution conditions and produces attestation output during Phase B. Operates independently of the measurement operator. Does not produce runtime behavioral measurement.
- **Reviewer.** Conducts post-hoc comparison during Phase C. Has access to all sealed artefacts after Phase B closure.

### 3.3 Separation constraints

- The prompt curator and the reviewer may be the same party, provided they hold no operational role during Phase B.
- The measurement operator and the attestation witness must be operationally separated during Phase B; they may communicate only through the protocol log.
- No party may modify any artefact after its custody event marks it as sealed.

### 3.4 Phase access matrix

To be specified in v0.2 alongside witness constraints (section 4).

---

## Open boundary questions for v0.1 review

The following questions are intentionally left open at v0.1 and are explicitly within scope of the boundary review:

1. **ASRO scope.** Is ASRO described in section 3.2 ("attestation witness") in a way that does not collapse it into runtime behavioral instrumentation? Is the asymmetry with NeoMundi's role made explicit enough?
2. **NeoMundi scope.** Is NeoMundi's measurement role described in a way that does not implicitly absorb attestation duties that belong to ASRO?
3. **Non-circularity.** Does the custody structure in section 2 introduce any implicit point of circularity (e.g., a single party producing both prompts and review criteria; or a measurement output feeding back into an attestation it should be witnessed by)?
4. **Claim-limit strength.** Are the explicit non-conclusions in section 1.2 strong enough to prevent over-generalisation from a positive outcome — including in third-party communication after execution?

A fifth question, beyond the four agreed criteria, is also welcomed:

5. **Independent reviewability.** Would the evidence record produced under sections 1–3 (once extended by sections 4–7) be independently reviewable by a third party with no operational role in Round 2?

---

*End of v0.1. Sections 4–7 deferred pending boundary review.*
