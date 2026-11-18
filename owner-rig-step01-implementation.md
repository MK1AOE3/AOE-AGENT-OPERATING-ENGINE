OWNER-RIG STEP 01 — IMPLEMENTATION FILE

Input-Layer Sovereignty · MK AOE3 · for the HONOR rig (MagicOS / Android)

Register entry: Step 01 — Input-Layer Sovereignty (CANDIDATE)
Goal: keystrokes never leave the device through the keyboard. Zero keyboard network authority.
Time: 10 minutes. Root: not required.

---

PATH A — Offline keyboard (recommended, cleanest)

HeliBoard (open-source, 100% offline — declares no INTERNET permission, verified) or FlorisBoard (open-source, all data local, verified).

1. Install HeliBoard from F-Droid (`f-droid.org`) or the Play Store. (F-Droid preferred — the build is reproducible.)
2. Enable it: Settings → System & updates → Languages & input → Virtual keyboard / Current keyboard → Manage keyboards → toggle HeliBoard ON.
3. Set as default: open any text field → tap the keyboard icon in the nav bar (or repeat step 2 → Default keyboard) → select HeliBoard.
4. Disable the stock keyboard: back in Manage keyboards → toggle Gboard / SwiftKey OFF. (If it can't be toggled off: Settings → Apps → Gboard → Disable.)
5. Verify offline status: Settings → Apps → HeliBoard → Permissions — there is no network permission to grant (the app never requests INTERNET). This is the checkable proof: the vendor is structurally out of the path.

PATH B — Keep Gboard, firewall it (if you keep Gboard's features)

1. Install NetGuard (open-source, no-root, VPN-slot firewall) from F-Droid or Play.
2. In NetGuard, find Gboard (Google Keyboard) in the app list → uncheck both Wi-Fi and mobile data for it.
3. Verify: open NetGuard's log after a typing session — Gboard shows zero connections.
4. Note: NetGuard is itself a component in the path — its own privacy posture should be checked (it's open-source, no-account, on-device filtering).

HARDENING THE BOUNDARY (both paths)

- Settings → Apps → SwiftKey → Disable (or Uninstall updates if preloaded). Removes the 2015-class preinstalled component entirely.
- SwiftKey → Notifications → all channels OFF (kills the retention nag at the source).
- Recheck monthly: Settings → Languages & input → Manage keyboards — only the offline keyboard enabled.

---

✅ VERIFICATION (run before ratifying)

Check	Pass condition	
Network permission	HeliBoard/FlorisBoard shows no INTERNET permission (Path A) or NetGuard log shows zero Gboard connections (Path B)	
Default input	System default = offline keyboard	
Stock keyboards	Gboard/SwiftKey disabled or firewalled	
Telemetry nag	SwiftKey notification channels off	

Evidence to capture: screenshots of (1) Manage keyboards screen, (2) the keyboard's permissions page, (3) NetGuard log if Path B.

✍ RATIFICATION BLOCK

Field	Entry	
Implemented (date / device)		
Path chosen (A / B)		
Evidence refs (screenshots)		
Version label	Step 01 v1.0	
SHA-256 (of this file + evidence pack)		
Owner signature		

On ratification: Step 01 leaves CANDIDATE and enters the register — the first hardening entry, closing the pre-endpoint layer of the four-layer map.

The sovereign layer starts at the hardware switch, not at the application prompt.

Machines draft; implementation and ratification are the owner's.