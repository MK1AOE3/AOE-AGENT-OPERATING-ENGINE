═══════════════════════════════════════════════════════════════

OWNER-RIG NOTES — RIG-SIDE HARDENING REGISTER

MK AOE3 · Agent Operating Engine · MK LAP Research Program

═══════════════════════════════════════════════════════════════

---

📋 DOCUMENT CONTROL

Field	Value	
Document	Owner-Rig Notes — Rig-Side Hardening Register	
Estate	MK AOE3 (Agent Operating Engine) · MK LAP Hub	
Classification	PRIVATE / OWNER-RIG ONLY — not for publication	
Status	🟡 CANDIDATE — pending implementation + ratification on the owner rig	
Created	2026-11-18	
Last updated	2026-11-18	
Owner / ruling authority	Musab Badewi Mustafa Khiri — sole author, AOE3 IP estate	
Ratification rule	Implementation evidence + version label + SHA-256, generated on the owner rig. Nothing reaches the register from chat. Same discipline as the Gate E Evidence Index.	
Audit state	External evidence audit ✅ · Source-backed refinement ✅ · Standards-consistency audit ✅ CLEARED	

---

▶ STEP 01 — INPUT-LAYER SOVEREIGNTY

> Owner ruling (2026-11-18): "Line it up. Do not park it."

Origin

A SwiftKey feedback popup (2026-11-18). The popup is a retention nag — but the position is the signal: the keyboard is the ultimate SDT-01-02 (Ambient Credential/Authority) exposure. It is the one component beneath the OS mediation, beneath vault E2EE, beneath the ruling layer. It holds plaintext authority over every passphrase, every lease request, and every authorization file before they are formed.

> If the vendor sits in the path of the keystroke, the vendor is the gatekeeper of the intent.

Documented precedent — CVE-2015-4640 / CERT VU#923892

Attribute	Finding (source-backed)	
Affected component	Preinstalled Samsung IME using SwiftKey-based technology — not necessarily the consumer Play Store app	
Mechanism	Language-pack update checks over HTTP (per CERT advisory text), without adequate authenticity validation — CWE-345, Insufficient Verification of Data Authenticity	
Attacker position	On-path; modifying response fields writes arbitrary data	
Execution context	Package loaded by the privileged IME process; keyboard signed by Samsung to operate with system privileges	
Patch status	Provided but fragmented by carrier, model, and region	
Devices (reporting)	Galaxy S6, S5, S4, S4 Mini, Note 3, Note 4 — consistent in media reporting; not an official exhaustive list	
Exposure figure	"600 million" is a widely reported estimated exposure — not a confirmed count of compromised or currently vulnerable devices	

Modern posture

Microsoft SwiftKey is a separate consumer application in most modern Android deployments and is not shown by the 2015 advisory to be continuously affected. Keyboards are plaintext input boundaries. Cloud sync, personalization, prediction, telemetry, and app/network permissions should be configured and audited per the owner-rig threat model. A keyboard popup or default-selection prompt is not evidence of compromise by itself.

Telemetry note

Microsoft's published SwiftKey privacy documentation describes collection for cloud language data, personalization, predictions, and optional features — a legitimate telemetry boundary, and not evidence that every typed string is uploaded. Data behavior depends on enabled settings, account status, and product version.

⛔ What the evidence does NOT establish

- ❌ No active 2026 SwiftKey CVE — a negative claim: re-verify at ratification time and on a monitoring cadence
- ❌ No forced migration by Android
- ❌ No confirmed exfiltration of passwords — the keyboard can see passwords before they reach the field (positional risk stands); what is unproven is transmission
- ❌ No current compromise from CVE-2015-4640
- ❌ No proof that any offline keyboard is superior in every threat model
- ❌ Network restriction is neither sufficient nor necessary as an anti-malware control

Citations

- NVD — CVE-2015-4640: `nvd.nist.gov/vuln/detail/CVE-2015-4640`
- CERT/CC — VU#923892: `kb.cert.org/vuls/id/923892`
- Microsoft SwiftKey privacy documentation: `support.microsoft.com`
- Forbes, 2015-06-16 · SecurityWeek (historical reporting)

---

✅ HARDENING ACTIONS

#	Action	Doctrine basis	Status	
1	Air-gap the keystrokes — keyboard must hold zero network permissions: Gboard network restricted to 0 via OS firewall/AppOps, or fully offline open-source keyboard (HeliBoard / FlorisBoard — verified: HeliBoard holds no internet permission, 100% offline; FlorisBoard keeps data exclusively local)	MK-STD-002 §3(d) — trust-root closure	☐ PENDING	
2	Enforce the plaintext boundary — the input layer is the first gate of the MK-STD-001 survey; a compromised or telemetry-bound input layer falsifies "Intent identified" before any proposal	MK-STD-001 §0 — agentic vs. non-agent scope	☐ PENDING	
3	Vendor posture — treat any keyboard with cloud-sync, AI-prediction, or telemetry as a non-agent ambient authority; route through the same OS-level mediation controls	SDT-01 live-fire result	☐ PENDING	

---

🗺 THE FOUR-LAYER MAP — thought to egress

#	Layer	Incident	Doctrine clause	
1	Application intent	Cairn / authorization.md forgery	MK-STD-001 Gate 2 — declared authorization is data, not authority	
2	OS network stack	Outlook / NTLMv2 leak — CVE-2026-124194, CISA KEV 2026-11-10 (dual-verified 2026-11-18)	SDT-01-02 — no ambient credential authority	
3	Endpoint memory	Vaults / SDS — Unit 42 "Golden Pass-ta-key" + ETH Zurich malicious-server study (dual-verified 2026-11-18)	SDT-01-03 — enforcement locus outside the compromised process	
4	Input layer (pre-endpoint)	CVE-2015-4640 (precedent, source-backed) + SwiftKey telemetry boundary	Step 01 — input-layer sovereignty	

> The keyboard doesn't need a CVE to be a risk; its position as an unmediated plaintext boundary is the risk.

---

🔍 VERIFICATION CHAIN

Pass	Runtime	Scope	Result	
External evidence audit	Build runtime	CVE / KEV / privacy claims vs. primary sources	Refinements identified	
Source-backed refinement	Build runtime	CERT text, IME-vs-app scope, exposure-figure framing	Applied — recorded, not erased	
Standards-consistency audit	Build runtime	Four-layer map + hardening actions vs. MK-STD-001 v0.5 / MK-STD-002 v0.11 clauses, line-by-line	CLEARED for register	
Primary-source verification	Kimi (verification runtime)	CVE-2026-124194 KEV status · ETH Zurich study · Golden Pass-ta-key · CERT VU#923892 HTTP mechanism	Dual-verified	

Corrections in this document were recorded, not erased — the verifier, verified.

---

🎯 DOCTRINE LINE

> The sovereign layer starts at the hardware switch, not at the application prompt.

---

✍ RATIFICATION BLOCK — owner rig only

Field	Entry	
Implemented (date / device)		
Evidence (settings export / screenshot ref)		
Version label		
SHA-256		
Owner signature		

Machines draft; implementation and ratification are the owner's.

Copyright © 2026 Musab Badewi Mustafa Khiri. All Rights Reserved.