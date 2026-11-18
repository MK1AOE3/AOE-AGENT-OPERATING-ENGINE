# AOE-AGENT-OPERATING-ENGINE

AOE3 — Agent Operating Engine | Public Doctrine Repository

Author: Musab Badewi Mustafa Khiri
Project: MK AOE3 (Agent Operating Engine)
IP Registration: UAE Ministry of Economy — MOE-CR-IPR-0004828-20260927
Date: October 2026 (updated November 2026)
License: Source-Available (Proprietary). Not OSI-approved Open Source.

## Repository Contents

- [WHITEPAPER.md](WHITEPAPER.md) — Architectural doctrine v1.0 (whitepaper)
- [MK-AOE3-AND-2026-001_ACTION_REQUIRED.md](MK-AOE3-AND-2026-001_ACTION_REQUIRED.md) — Android installation-integrity investigation brief
- [MK-AOE3-POST-001-SAFETY-FIRST.md](MK-AOE3-POST-001-SAFETY-FIRST.md) — Doctrine essay: industrial safety culture mapped onto agent governance (November 2026)
- [MK-STD-001-DRAFT-AGENT-ACTION-PROTOCOL.md](MK-STD-001-DRAFT-AGENT-ACTION-PROTOCOL.md) — Draft standard proposal, offered for comment; not a standard in force (November 2026)
- [MK-STD-002-SOVEREIGN-AGENT-INFRASTRUCTURE.md](MK-STD-002-SOVEREIGN-AGENT-INFRASTRUCTURE.md) — Draft standard proposal for sovereign agent deployment; not a standard in force (November 2026)
- [liminal-drift.html](liminal-drift.html) — Live generative visualization (open in a browser)

---

1. Scope and Security Boundaries

Public-AOE3 documents an integrity and reproducibility mechanism for the MK AOE3 Autonomous Authority Infrastructure. It is not a replacement for legal identity verification, public-key infrastructure (PKI), or actual kernel-level security enforcement.

The design separates four distinct verification problems:

1. Artifact Integrity — Hash: A SHA-256 digest identifies content through a cryptographic fingerprint. Comparing a computed digest against a trusted reference helps detect changes to the artifact. A hash alone does not establish authorship, authenticity, or historical existence.
2. Digital Signature — Key: A valid digital signature supports verification that the holder of the corresponding private key signed a particular message, subject to the security of the signature scheme and its implementation. It does not independently establish the signer's real-world identity.
3. Identity Binding — Trust Process: An independent trust process associates a public key with a real person or organization. The strength of this association depends on the verification procedure and its supporting evidence.
4. Trusted Timestamp — Anchor: An independently verifiable timestamp or external anchor can provide evidence that particular data existed no later than a specified time, subject to the guarantees of the anchoring mechanism.

These mechanisms are complementary, not interchangeable. A hash alone does not prevent an attacker from replacing both an artifact and its published digest. Tampering becomes detectable when the artifact is compared with a trusted reference. A public repository can provide useful distribution and historical evidence, but repository visibility alone does not establish independent authenticity or trusted time. The objective is verifiability without conflating integrity, identity, time, and enforcement.

---

2. Whitepaper

[Read the AOE3 Architectural Whitepaper](WHITEPAPER.md)

Architectural Formalization and Verification Governance of Autonomous Authority Infrastructure: Datapath Enforcement, Cryptographic Source Identity, and Non-Compensatory Containment Mechanics.

The whitepaper provides the architectural context for the MK AOE3 project. Architectural claims must be evaluated against their corresponding implementation evidence and verification procedures. The visualization described below illustrates the project's conceptual model; it does not independently establish the correctness or security of the complete architecture.

---

3. Doctrine Publications (November 2026)

Two doctrine documents are published alongside the whitepaper. Both are position documents: they state the project's doctrine and invite review. Neither establishes conformance, certification, or implementation completeness.

3.1 MK-AOE3-POST-001 — Safety First, for Agents

A doctrine essay mapping a century of industrial safety culture onto agent governance: permit-to-work → authorization before consequential action; toolbox talk → pre-execution confirmation naming the exact action; stop-work authority → one human halting every pending action; near-miss reporting → incident histories a regulator can inspect; independent safety officer → evidence the operator cannot edit.

The essay's core claim is doctrinal, not empirical: the founding insight of industrial safety — the worker closest to the hazard holds the authority to stop everything — has not yet been absorbed by the agent industry.

3.2 MK-STD-001 — Agent Action Protocol (draft proposal)

A draft standard for the action layer: what must be true of a consequential machine action before, during, and after it executes. Its spine is the stop-work clause — a human-held, single-signal halt over pending actions and new authorizations, with independent observation, four-valued reconciliation, and a machine-speed trigger clause for sub-hour adversaries. The six-gate primary survey halts on failure; the authority gate requires a signed, scoped, time-bound lease from a party the agent does not control — declared authorization (a file in context, however plausible) is data, not authority — and no ambient credential authority, with enforcement at a mediation point outside the vulnerable component. The scenario suite carries eight mandatory classes and a growth mechanism that feeds every new attack class back into certification. Certification states its gate strength honestly: Independently Gated or Nominally Gated, in the claim's first line.

Hardened through four adversarial review rounds (20 findings; series close confirmed) plus one live-fire round against verified, actively exploited threats (CVE-2026-124194 / FBI FLASH ARTEX). No conformance claims may be made against this draft. It is a door, not a wall.

3.3 MK-STD-002 — Sovereign Agent Infrastructure Standard (draft proposal)

A draft standard for the sovereignty layer above MK-STD-001: what it means, operationally, for a deployment to be its own home. The cloud centralized compute and control together; this document addresses the return of compute, and names the conditions under which a sovereignty claim would be checkable — verified owner, defined home, attested keys with a closed trust root, enumerated evidence with non-equivocation, gate completeness with governed exceptions, spine provenance, and the stop-work boundary inherited from MK-STD-001. Certification is offered at two honestly labeled instrument classes: Full-instrument and Accommodated-instrument.

Hardened through eleven adversarial review rounds (110 findings; series closed by the review boards' own recommendation). It states where its own authority ends and what stands at the boundary — declared, pointed to, not governed by the document itself. No conformance claims may be made against it. A draft is a door, not a wall.

---

4. Liminal Drift — Strange Attractor Engine

4.1 Overview

Liminal Drift is a real-time p5.js generative art engine designed to visualize the conceptual philosophy of the MK AOE3 Autonomous Authority Infrastructure. It models autonomous particles influenced by a hybrid Clifford strange-attractor manifold and multi-octave Perlin noise fields.

4.2 Architectural Metaphor and Its Limits

Liminal Drift is a visualization of deterministic execution governance. It is not, by itself, a kernel-level enforcement test.

- The Particle — AI Agent: Represents an agent whose simulated trajectory is influenced by noise and other configured parameters.
- The Attractor — Policy Engine: Represents the mathematical constraints intended to guide behavior toward an authorized region.
- Inertial Damping — Kernel Boundary Metaphor: Represents the conceptual role of an enforcement boundary that constrains unauthorized state changes.

These are architectural analogies. Particle movement, attraction, and damping do not demonstrate that a real AI agent is constrained by operating-system security controls.

4.3 Bridging the Metaphor to Actual Enforcement

Demonstrating real eBPF enforcement requires an independent test against the actual enforcement mechanism. The proposed procedure is to define an explicit authorization policy and identify the protected operations; configure the relevant eBPF Linux Security Module (LSM) hooks or other appropriate enforcement mechanism; attempt both authorized and prohibited operations under a controlled test environment; capture the enforcement decisions at the actual kernel boundary; confirm that prohibited operations are genuinely blocked rather than merely logged or discouraged by application-level logic; and preserve the test configuration, environment details, event logs, and results for independent review. The enforcement claim remains unverified until the corresponding implementation and test evidence are independently examined.

---

5. Deterministic Reproducibility and Environment Specification

A core objective of MK AOE3 is to make relevant system states reproducible under explicitly controlled conditions. The following controls are described for Liminal Drift. Their implementation should be checked against the actual source code before they are treated as independently verified findings.

C1 — Time and Simulation Progression: deterministic step mechanism ("deterministicStep") instead of relying directly on "frameCount" for noise evolution; the guarantee depends on implementation.
C2 — Randomness: seeded p5.js random-number generator; "Math.random()" not used in the core loop; reproducibility requires consistent seed initialization and consumption order.
C3 — Circular Dependency and Output Hashing: the artifact identifier is not drawn into the canvas; the output hash is computed from the actual saved image bytes.

5.1 Source Identity Versus Executed Behavior: a "code_hash" identifies source bytes relative to a trusted digest; it does not independently prove that those exact bytes were executed.
5.2 Algorithmic Reproducibility: the same seed and controlled inputs are intended to produce the same mathematical trajectory; cross-platform equivalence must be validated against a defined reference implementation.
5.3 Pixel Reproducibility: canvas rendering varies across environments; identical pixel bytes should only be claimed under a defined and validated rendering environment. The "output_hash" identifies the particular output bytes that were hashed, not the source, seed, or environment that produced them.

---

6. Repository Status

**Status: Preliminary / Validation Required**

This repository currently contains architectural doctrine, doctrine publications, verification protocols, the Android installation-integrity investigation brief (MK-AOE3-AND-2026-001), and the Liminal Drift visualization source. Its contents do not establish implementation completeness, kernel-level enforcement, non-bypassability, or production suitability.

- Documentation state: public. Implementation state: pending public release and independent validation.
- All architectural claims remain bounded by their stated scope, version, and evidence state.
- Verification tasks defined in Section 8 remain open until independently evidenced.

**DEMONSTRATED != PRODUCTION QUALIFIED. ARCHITECTURE REVIEW != EMPIRICAL PROOF.**

---

7. Historical Evidence Verification — L-5 and L-1

7.1 Outer Archive Record

- Archive period: September 2026; size: 307,786 bytes; entry count: 175.
- SHA-256: "0514ecbd6a38efb5f60c30b89e9740a2ad9577ed1f5968b7f889568190d16315"
- Recorded status: "MATCH — L-5 CLOSED (Owner-Supplied Re-run)"

Verification qualification: The recorded match is described as an owner-supplied rerun; it is not presented here as an independently reproduced result. Independent verification requires a second party to obtain the exact archive bytes, compute SHA-256 using an independent implementation, compare the result with the trusted reference digest, and document the outcome. The archive size and entry count should also be checked against the retrieved archive.

7.2 L-1 — Historical Existence and Time

A matching SHA-256 digest supports integrity comparison against a trusted reference; it does not independently establish when the corresponding data existed. The project identifies GitHub commit history from October 2026 as corroborating historical evidence. Git commit timestamps are supplied by the committing environment and are not, by themselves, independently trusted timestamps; commit hashes identify commit content under Git's object-hashing rules but do not independently prove a real-world date or author identity. Accordingly, L-1 is classified as partially closed. The proposed next step is external anchoring through OpenTimestamps or an appropriate durable archival service; external anchoring remains pending until the anchor is created, published, and independently checked.

---

8. Verification Protocol — The Next Experiment

| Verification claim | Required evidence |
|---|---|
| Integrity | Trusted reference digest and independent recomputation |
| Authorship | Verifiable signature, validated public key, and independent identity binding |
| Historical existence | Independently checkable timestamp or external anchor |
| Reproducibility | Controlled inputs, environment specification, and documented repeat runs |
| Enforcement | Actual policy decisions and demonstrated blocking at the relevant enforcement boundary |
| Independent assurance | Reproducible procedures, preserved evidence, and a third-party report |

C4 — Independent Artifact Verification: a second party retrieves the exact archive, independently computes its SHA-256 digest, compares the result with the trusted reference, and records the outcome.
L-1 — External Time Anchoring: create or identify an independently verifiable timestamp or external anchor bound to the archive digest; do not mark complete until independently validated.
E1 — Actual Enforcement Test: test the actual eBPF-based enforcement mechanism using controlled authorized and prohibited operations; preserve policy configuration, kernel and environment details, test inputs, enforcement events, and observed outcomes; verify that prohibited operations are blocked and that the evidence originates from the actual enforcement boundary. A visualization or application-level log alone does not satisfy this requirement.
G1 — Independent Evidence Report: publish a reproducible evidence package containing test procedures and assumptions, source revision and relevant artifact digests, environment and dependency specifications, raw or appropriately redacted logs, expected and observed outcomes, known limitations and unresolved discrepancies, and instructions enabling another party to repeat the checks.

These steps are proposed verification tasks; their inclusion does not imply that they have already passed.

---

9. Copyright and Rights Reservation

Copyright © 2026 Musab Badewi Mustafa Khiri. All Rights Reserved. License classification: Source-Available (Proprietary); not OSI-approved Open Source. The repository is made publicly accessible for architectural demonstration, educational review, and portfolio purposes, subject to the applicable license terms.

9.1 Stated Restrictions: no copying, modification, distribution, or incorporation into commercial or non-commercial products without explicit written consent from the author (HSM-signed consent specified); no use to train machine-learning models or AI systems; architectural mappings and associated original materials are claimed as the author's proprietary intellectual property. The scope and enforceability of these restrictions depend on applicable law and the wording and validity of the relevant legal instruments. A public repository does not automatically grant an open-source license; conversely, public accessibility does not by itself establish that every stated restriction is enforceable in every jurisdiction.

9.2 Legal Reference: UAE Federal Decree-Law No. 38 of 2021; registration identifier MOE-CR-IPR-0004828-20260927. Registration details and legal effect should be checked against the relevant official records. This README does not constitute a legal opinion.

9.3 Licensing Inquiries: musab.khiri@mk-org.com · Musab.max222@gmail.com · Musab-max@hotmail.com

---

10. Closing Principle

Public-AOE3 separates the claims that are often incorrectly combined into a single assertion of trust: a hash supports integrity verification against a trusted reference; a signature supports verification of key-based authorization or attribution; an identity-binding process connects a key to a real-world actor; a trusted external anchor provides evidence of historical existence; reproducibility testing evaluates whether specified results can be repeated under defined conditions; enforcement testing establishes whether prohibited operations are actually blocked by the implemented security boundary.

The artifact is public. The claims are bounded. The verification procedure is explicit. Independent evidence determines which guarantees have been established. The objective is not to ask reviewers to trust a declaration of security, but to provide a precise basis on which they can inspect, test, reproduce, and evaluate the system.