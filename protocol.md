# NeoMundi / ASRO — Round 2 Protocol

**Version:** v0.3 (sections 1–4 sealed)
**Status:** Sections 1–3 sealed at role-boundary level (carried forward from v0.2, unchanged). Section 4 (witness constraints) integrated and sealed at procedural level following ASRO boundary review of §4 draft-0.1 and amendment of §4.3.4 per Q4.5 decision. Sections 5–7 deferred; structural skeleton maintained in `sections-4-7-skeleton.md` and not part of v0.3's sealed scope.
**Canonical source:** This Git repository. Tagged commits constitute the pre-registration trace.

---

## Preamble

This document is the canonical methodological protocol for Round 2 of the joint NeoMundi / ASRO collaboration. It is versioned in Git.

**v0.3 covers sections 1–4.** Sections 1–3 are carried forward unchanged from v0.2. Section 4 (witness constraints) is added in v0.3 following ASRO boundary review, with the controlling phrase agreed during skeleton review:

> **ASRO witnesses reviewability conditions; it does not validate runtime behavior.**

That phrase governs §4 throughout and refines, without contradicting, the boundary crystallization in Annex A.

Sections 5–7 (admissible evidence categories; comparison procedure; formal freeze and signature) are deferred. A minimal structural skeleton for sections 5–7 is maintained in `sections-4-7-skeleton.md` and is **not** part of v0.3's sealed scope. Procedural drafting of §5 begins only after v0.3 is tagged.

### Changelog
- **v0.3** — Section 4 (witness constraints) added and sealed at procedural level. Controlling phrase placed in §4.1. §4.3.4 specifies that ASRO may not be the custody-continuity witness of its own attestation output; a third-party witness, named in the protocol log before Phase B opening, is mandatory. §4.4 addresses timestamp circularity (default Git timestamp admitted only where the canonical repository is outside the witnessed system; otherwise a named external timestamping authority is required).
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

The following artefact classes are recognised by the protocol. Their precise format and sealing procedure are specified in Section 4 (witness constraints).

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

To be specified in v0.4 alongside admissible evidence categories (Section 5).

---

## Section 4 — Witness constraints

### 4.1 Controlling principle

This section is governed throughout by the following controlling phrase, agreed upon during boundary review of the §4–7 skeleton:

> **ASRO witnesses reviewability conditions; it does not validate runtime behavior.**

This phrase refines, without contradicting, the boundary crystallization in Annex A. It narrows the scope of "reviewability conditions" by making explicit that ASRO does not attest to the **truth** of any runtime measurement, only to the **conditions** under which that measurement is independently reviewable. Any procedural rule in §4 that could be read as making ASRO a runtime-content attester is to be reinterpreted, or struck, in favour of the controlling phrase.

Symmetrically, no procedural rule in §4 may be read as authorising NeoMundi to produce or co-sign witness output. NeoMundi remains the exclusive producer of runtime measurement output; it does not witness, attest, or co-attest.

### 4.2 General witness requirements

The following requirements apply to every witnessing event under this protocol, regardless of artefact class or phase.

#### 4.2.1 Operational separation
The witness (ASRO) and the measurement operator (NeoMundi) must be operationally separated during the entire duration of any witnessing event, per §3.3. Communication between the two layers during a witnessing event is restricted to the protocol log.

#### 4.2.2 Form of a witness output
A witness output, to be admissible under this protocol, must:

- (a) name the witness identity (functional role and, if applicable, the individual or group acting in that role);
- (b) name the artefact or artefact class witnessed, by reference to §2.3;
- (c) state explicitly the **reviewability condition** the witness output asserts (e.g., custody-chain continuity over a stated interval; observer separation over a stated interval; declared system configuration at a stated moment);
- (d) carry a cryptographic signature by the witness, over (a)–(c) plus a timestamp;
- (e) include a reference to the protocol version under which the witness output was produced (e.g., `protocol.md` v0.3 at commit hash).

#### 4.2.3 What a witness output is not
A witness output is **not**:

- a claim that the witnessed artefact is correct, true, or accurate as to its substantive content;
- a claim about the validity of Law E or of any other measurement framework;
- a claim about the actual runtime behavior of any model or system;
- a claim that any NeoMundi measurement output is reliable, well-formed, or fit for any purpose.

A witness output asserts only that the reviewability conditions named in (c) above held over the stated interval, to the best of the witness's knowledge and within the operational constraints recorded in the protocol log.

#### 4.2.4 Witness output is not measurement output
A witness output and a measurement output are evidence of distinct facts. The protocol does not authorise the fusion of witness output and measurement output into a single judgement at any phase. The treatment of these two classes of output as evidence is specified in §5.

### 4.3 Per-artefact witness constraints

For each artefact class enumerated in §2.3, the following constraints apply. In every case, the witness output asserts only the reviewability condition stated, never the content of the artefact.

#### 4.3.1 Prompt set
- **Witnessed condition.** Sealing of the prompt set at the close of Phase A, and continuity of custody from sealing to disclosure at Phase C.
- **Witness identity.** Attestation witness (ASRO), per §3.2.
- **Not witnessed.** The substantive content of the prompts; their representativeness; their fitness for any downstream purpose.

#### 4.3.2 Response set
- **Witnessed condition.** Custody-chain continuity of the response set from generation during Phase B to sealing at Phase B closure.
- **Witness identity.** Attestation witness (ASRO).
- **Not witnessed.** The correctness, quality, or behavioral interpretation of the responses.

#### 4.3.3 NeoMundi measurement output
- **Witnessed condition.** That a NeoMundi measurement output was produced during Phase B under the operational separation declared in the protocol log, and that custody of the output was sealed at Phase B closure.
- **Witness identity.** Attestation witness (ASRO).
- **Not witnessed.** The correctness, calibration, or reliability of the measurement. ASRO does not interpret NeoMundi measurement results (per §3.2). The substantive correctness of the measurement output is outside the scope of any witness output under this protocol.

#### 4.3.4 ASRO attestation output
- **Principle.** ASRO may produce the attestation output. ASRO may not be the independent custody-continuity witness for its own attestation output inside this protocol. Self-witnessing of ASRO attestation output is excluded, to preserve the witness surface of the protocol from any loop in which the producer of an evidentiary object is also the witness of its custody continuity.
- **Witnessed condition.** That the ASRO attestation output was produced during Phase B under the operational separation declared in the protocol log, and that its custody was sealed at Phase B closure.
- **Witness identity.** A **third-party witness**, mandatory under this protocol, named in the protocol log **before Phase B opening** and operationally separated from both NeoMundi and the ASRO operator. The third-party witness is bound by the same general requirements as any witness under §4.2.
- **Excluded.** NeoMundi (per §4.1). The ASRO operator itself (per the principle above).
- **Not witnessed.** The substantive validity of ASRO's attestation conclusions.

#### 4.3.5 Protocol log
- **Witnessed condition.** Append-only continuity of the protocol log across Phases A, B, and C; absence of post-hoc modification of sealed entries.
- **Witness identity.** Attestation witness (ASRO), as a structural property of the log infrastructure rather than as content attestation.
- **Not witnessed.** The substantive correctness of any entry recorded in the log.

#### 4.3.6 Pre-registration commit hash
- **Witnessed condition.** That the Git commit hash declared as the pre-registration trace at the opening of Phase A was already published in the canonical repository at a moment strictly prior to Phase A opening, as evidenced by the Git timestamp on the tagged commit.
- **Witness identity.** No additional witness is required beyond the cryptographic Git timestamp itself, provided that the canonical repository is hosted under an infrastructure declared in the protocol log prior to Phase A opening and stable through Phase C closure. If that condition does not hold, an external witness must be named in the protocol log prior to Phase A.
- **Not witnessed.** The substantive correctness of any content in the pre-registered protocol document.

### 4.4 Timestamping mechanism

#### 4.4.1 Default timestamping
The default timestamping mechanism for all witness outputs under this protocol is the Git commit timestamp produced by the canonical repository hosting `protocol.md`, combined with the cryptographic signature on the tag at pre-registration.

#### 4.4.2 Constraint on the default mechanism
The default timestamping mechanism is admissible **only if** the canonical repository's hosting infrastructure is **not part of the system whose reviewability conditions ASRO is witnessing**. In other words: ASRO must not be simultaneously (i) witnessing the timestamping infrastructure and (ii) relying on that same timestamping infrastructure to date its own witness outputs.

#### 4.4.3 Fallback mechanism
Where the constraint in §4.4.2 cannot be satisfied — for example, if the canonical repository sits within the system under measurement — an external timestamping authority must be named in the protocol log prior to Phase A opening, and used in place of (or in addition to) the Git timestamp for all witness outputs produced during Phase B.

#### 4.4.4 Declaration in the protocol log
Whichever mechanism is in force, it must be declared in the protocol log at Phase A opening and remain unchanged through Phase C closure. Any change to the timestamping mechanism between Phase A opening and Phase C closure invalidates the witness outputs produced under the prior mechanism for the purposes of this protocol.

### 4.5 What §4 does not establish

This section defines **how** witnessing events occur. It does not define:

- what counts as admissible evidence in Phase C review (§5);
- how sealed artefacts are compared in Phase C (§6);
- the act by which the protocol becomes formally binding (§7).

A witness output produced under §4 has no evidential weight in Phase C beyond what §5 admits, and no comparative use beyond what §6 specifies. A protocol that has produced compliant witness outputs under §4 is not, by that fact alone, frozen or signed; §7 governs that.

---

## Open boundary questions — status

The boundary questions carried forward from v0.1 / v0.2 and from the §4 review:

1. **Q1 — ASRO scope.** *Addressed in v0.2 via narrowed definition + symmetric disclaimer + boundary crystallization. Reinforced in §4 via controlling phrase.*
2. **Q2 — NeoMundi scope.** *Addressed in v0.2 via symmetric disclaimer. Reinforced in §4.1 by closing NeoMundi out of witnessing.*
3. **Q3 — Non-circularity.** *Partially addressed in §4.4 for the timestamping case. Custody structure review continues into §5.*
4. **Q4 — Claim-limit strength.** Are the explicit non-conclusions in §1.2 strong enough to prevent over-generalisation from a positive outcome — including in third-party communication after execution? *Open. Re-examined at v0.4 alongside §5.*
5. **Q5 — Independent reviewability.** Would the evidence record produced under §1–4 (once extended by §5–7) be independently reviewable by a third party with no operational role in Round 2? *Open. Cannot be answered before §5–7.*
6. **Q4.1, Q4.2, Q4.3, Q4.4 (§4 review).** *Addressed in §4.1–§4.4 as documented therein.*
7. **Q4.5 (§4 review, resolved).** Witness of ASRO attestation output's custody continuity. *Resolved: self-attestation by ASRO is excluded; third-party witness mandatory per §4.3.4.*

---

## Annex A — Boundary crystallization

The asymmetry between NeoMundi and ASRO is binding for the entire protocol. It is stated here in canonical form:

> — NeoMundi measures runtime behavior.
> — ASRO witnesses the reviewability conditions around the measurement process.
> — Neither layer absorbs the other.

For §4 and downstream, the controlling phrase agreed during boundary review further specifies:

> **ASRO witnesses reviewability conditions; it does not validate runtime behavior.**

Any reading of this protocol that absorbs one layer into the other, or that infers from a positive outcome any claim beyond the explicit non-conclusions in §1.2, is outside the scope of Round 2 and is not supported by this document.

---

**End of v0.3.** Sections 5–7 maintained as a separate structural skeleton in `sections-4-7-skeleton.md`, pending procedural drafting subsequent to v0.3 tagging.
