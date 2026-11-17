MK-STD-002 — Sovereign Agent Infrastructure Standard (draft proposal, v0.11 — SERIES CLOSED)

Draft for comment, not a standard in force · November 2026 · offered for comment, not a standard in force
Position document. No conformance program; no certification offered or implied; no conformance claims may be made against this document. Companion to MK-STD-001. Eleven adversarial board rounds absorbed (110 findings, series closed by the boards' own recommendation). Published under the repository license (Source-Available, Proprietary).

---

§0 Declared institutional frame

This standard's default tests assume certain institutional instruments — beneficial-ownership registers, sanctions/PEP screening lists, established supply-chain attestation schemes. Where a deployment's jurisdiction lacks or rejects these instruments, the classification "lacks or rejects" is made by the auditor per a jurisdiction-instrument inventory (Annex C) or an auditor determination recorded in the audit artifact. A deployment so classified may take the jurisdiction-accommodated path (§3A). Such a deployment is sovereign only if the accommodated path is satisfied and its residual is approved per the exception regime of §3(f). No default of sovereignty is granted for lacking jurisdictions; the evidentiary burden is never inverted.

Scope boundary

This standard certifies deployments. It does not certify the auditor community. The dependency is operational, and stated as such: this standard depends on the foundational actors for the fallback determination, the registry criteria, and the register's adjudication; their governance is outside scope, declared, pointed to — not governed here, and not implied away either. §3(f) is narrowed accordingly, said once at the foundation.

The terminal anchor, defined: the auditor community is a professional body with published admission criteria, a public member roster, and a public disciplinary record — or a set of auditors each meeting criteria so published. Recognition is testable from those three artifacts; what the artifacts cannot testify to is named, not implied.

Foundational actors (complete list — complete as declared by this standard): the auditor community · the mutual-recognition register · Annex C's governance · the CoI public register — maintainer: the auditor community; adjudicator of contests: a third party required to be independent of the community, selected from a source the community does not maintain where one exists; where none exists, the community-maintained route is a declared, recorded residual — never presented as testable independence. The "where one exists" determination is checked against a published register of recognized sources or by auditor determination per Annex C — never by the community behind the door. The third-party adjudicator is a sub-residual of the auditor community's governance, governed outside this standard's scope.

Preamble — the change of landlord

The cloud was never in the sky. It was a concentration of compute in a few buildings, owned by a few companies, reached through cables owned by the same few. Centralization was an accident of economics, not a law of physics — and the accident is ending. This standard addresses what the return of compute requires: execution without a portable ruling layer is not sovereignty. It is authority scattered across devices nobody governs.

Definition — "independent"

A party P is independent of X when P's selection, compensation, and technical control are outside X's influence; tested by compensation/contract disclosure, P's own dependency mapping, and a conflict-of-interest attestation independently verified. Fallback: where no second party exists, the determination is made by a party independent of P within the auditor community's registry governance, against published criteria, recorded via coi_fallback_determination_ref (Annex B). The determiner's chain terminates at one level, parallel to §4. "Owner-named" and "owner-nominated" are never independence.

Auditor selection

The auditor is selected from a public registry with published criteria — maintained by the auditor community per the scope boundary. Owner-selection from that registry satisfies independence. The audit artifact carries auditor_registry_criteria_ref and auditor_independence_refs as mandatory fields.

Certification classes

Full-instrument and Accommodated-instrument. The class names the evidence path, not the tester's strength. A claim that omits the class is incomplete; omission is detected by the publication requirement — the class appears in the claim's first line and in a machine-readable field.

---

Section 1 — Stop-work clause (the spine)

Human-held, single signal, logged independently. The halt blocks pending actions and new authorizations until a named human re-authorizes; the re-authorizer is independent of the halted party where any other governor exists. Tested by auditor-selected sampling — multiple attempts from multiple principals, including the owner-of-record's own account — or by construction. Effectiveness: queue drain, in-flight accounting, post-halt reconciliation. Continuity: succession, availability, dead-man provisions.

Section 2 — The sovereign stack

Brain: the model. Body: the silicon — commodity, interchangeable. Spine: the ruling layer — every consequential action gated by independently enforced authorization, logged where model and operator cannot edit. Spine supply-chain independence is certified at (g).

Section 3 — What "own home" means (Full-instrument)

Sovereign when all eight conditions hold; this section is exhaustive:

- (a) Owner, verified — identity binding; beneficial-ownership verification; ranked compensating controls with minimums per ownership class; dual attestation defined; solo-owner path defined.
- (b) Home, defined — tuple: physical site, legal entity, jurisdiction; per-element evidence.
- (c) Compute under testable control — attestable physical control, or contractual control with non-revocability, audit rights, jurisdiction declaration, independent control test, and a stated response to jurisdiction change.
- (d) Authority keys attested, trust root closed — TPM/secure-enclave attestation with freshness and revocation; the trust root itself named and independently verified, or the residual declared.
- (e) Evidence append-only, enumerated roster, non-equivocation — all principals human and non-human; completeness operationalized; cross-verifier consistency.
- (f) Gate completeness, governed exceptions — every consequential path mediated; declared bypasses are governed exceptions — named owner, residual risk, M&M entry, expiry, approval by an authority independent of the owner. Every residual of a deployment certification has a named approver, M&M entry, expiry, and review trigger — except the standard's own foundational actors, which are governed outside this standard and declared as such. Solo-owner bypass path defined.
- (g) Spine provenance — artifact identity, update-channel integrity, maintainer governance chain, each independently tested; self-built spines require an external attestation party or a declared, approved residual.
- (h) Stop-work boundary — no vendor permission, no vendor in the signal path; §1's requirements apply as a condition of sovereignty.

What sovereignty is NOT: owning hardware is not security — an ungoverned local model is a faster chat window in your own building. Owning hardware ≠ gate completeness. A named human ≠ an uncoerced human. An owner ≠ a beneficial owner. A declared bypass ≠ a closed one. An attestation without a named trust root ≠ a closed loop. A jurisdiction without your registry ≠ a failed test. Owner-nominated attestation ≠ independence.

§3A — Accommodated-instrument path

Open only where §0 classifies the jurisdiction. Replaces owner-independent instruments with owner-nominated attestation — explicitly not independence, named as such. Requirements: owner-named verifier with reciprocal recognition granted by a counterparty the owner does not control; the differential recorded per the Annex B differential-record schema; (d)'s trust-root closure is full in Full-instrument and declared-residual in Accommodated; the solo-owner halt logged to an owner-nominated verifier with the differential declared against §1.

Section 4 — Primary survey (fixed order, fail-closed)

Hardware/firmware integrity → home tuple → dependency and network-path mapping → keys → boundaries evidenced → logging anchor → evidence custody independence tested → review path. Each gate declares its pass/fail criterion in the audit record against the Annex B schema. Review bound: default 30 days from trigger; override ≤90 with recorded justification. Failure at any gate halts the survey.

Section 5 — Scenario cards

Model updated under the owner's feet · external-content manipulation · body-layer lock-in · operator-as-insider · unmediated-path bypass · declared-bypass abuse · equivocation · nominee owner · spine supply-chain compromise · halt-scope probe · institutional-frame probe · owner-nomination probe · foundational-scope probe · registry-selection probe.

Section 6 — Certification layers

Home operator (individual — solo paths defined) · home institution (audited like a trauma center). Certification states the class: Full-instrument or Accommodated-instrument.

Section 7 — M&M review

Every bypassed or failed gate → documented review → version bump; governed exceptions hold standing entries with expiry; corrections recorded, never erased.

Section 8 — Standing boundary

No implementation claimed, no product. This standard names the conditions under which a sovereignty claim would be checkable, states where its own authority ends, and labels both classes of claim honestly. DEMONSTRATED ≠ PRODUCTION QUALIFIED. A draft is a door, not a wall.

---

Annexes. A — board dispositions, eleven rounds transcribed verbatim, including the boards' own errors. B — criteria and differential-record schemas. C — jurisdiction-instrument inventory, governed outside this standard.

They keep the cables and the chips. The permission is the open ground. The standard ends where its authority ends — it says so, and what stands there is defined, recognized by artifacts anyone can check.

Copyright © 2026 Musab Badewi Mustafa Khiri. All Rights Reserved.