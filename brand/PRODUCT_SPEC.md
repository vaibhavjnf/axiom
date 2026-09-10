# Axiom Product Specification

**Status:** Locked for launch package (engineering target, not a certified production BOM)  
**Form factor:** Ø78 × 28 mm matte aluminum puck  
**Tagline:** Always-on agent. Desk to pocket.

---

## 1. Mechanical

| Spec | Value |
|------|--------|
| Outer diameter | 78.0 mm |
| Height | 28.0 mm |
| Mass (target) | ~180–220 g (TBD after DFM) |
| Housing | Matte aluminum (CNC billet **or** MIM + anodize) |
| Finish | Fine bead / soft-touch anodize; near-neutral gray |
| Underside | MagSafe-compatible magnet ring, Ø55 mm pitch class |
| Charge port | Flush USB-C (no protruding collar) |
| Top | Acoustic mesh / LED window (warm white status) — minimal |

### MagSafe underside
- Magnet ring sized for desk docking and magnetic hold on MagSafe-compatible mounts
- Electrical charging remains **USB-C** in v1 (MagSafe ring = mechanical/magnetic dock; inductive MagSafe power is out of scope unless BOM revises)
- Ring diameter class: **55 mm** (Apple MagSafe alignment class for phone-scale accessories — verify fixture with production magnets)

---

## 2. Electronics (BOM — part *classes*, not vendor SKUs)

| Domain | Class / target | Notes |
|--------|----------------|-------|
| SoC / radio | **nRF5340** (dual-core Cortex-M33) + Wi-Fi/BT combo module | BT Classic/LE + Wi-Fi for agent uplink and HFP |
| Mics | **4× MEMS** ICS-43434 class (or equivalent I²S digital MEMS) | Circular array for beamforming / AEC |
| Speaker | **20 mm** dynamic speaker, sealed cavity | Voice playback + call audio |
| Magnets | MagSafe-compatible ring magnets + steel return path | Ø55 mm class |
| Battery | **LiPo ~4000 mAh / ~15 Wh** | See battery math |
| Charge | USB-C PD or USB-C 5 V charge IC + fuel gauge | Flush receptacle |
| LED | Warm-white indicator (diffused) | Status only |
| Buttons | Optional capacitive or single haptic — TBD; voice-first | Prefer zero clutter |

Exact manufacturer PNs to be locked during EVT with CM.

---

## 3. Battery math (12 h design target)

**Cell:** ~4000 mAh nominal, ~3.7 V → **~14.8–15 Wh** usable class.

**Rough power budget (engineering estimate, not lab measurement):**

| Mode | Assumed average | Notes |
|------|-----------------|-------|
| Always-on listen (DSP + mics + BLE keep-alive) | ~0.8–1.2 W | Duty-cycled radios |
| Wi-Fi agent sessions (bursts) | peaks higher; average folded into day mix | |
| Call / speaker (HFP + amp) | ~1.5–2.5 W while active | Intermittent |
| Idle docked / USB powered | N/A (mains) | Desk use |

**12-hour claim framing (honest):**  
At a blended average of **~1.2 W**, 15 Wh ≈ **12.5 h**. Marketing language: **“about half a day”** / **“designed for ~12 hours of mixed use”** — charge overnight. Do **not** claim multi-day life without a measured EVT power report.

Thermal: aluminum housing as heat path; avoid continuous max TX + full speaker for hours without derating.

---

## 4. Bluetooth call path

1. User’s phone is paired to Axiom over **Bluetooth HFP** (Hands-Free Profile).
2. When a call is active on the phone, Axiom can bridge mic/speaker as the HFP audio endpoint (joins the call as the headset).
3. Agent uplink (Wi-Fi/cloud or on-device assist) is a **separate** data path from HFP audio; do not conflate “agent hears call” with illegal call recording — privacy UX and local consent UI required in iOS companion.
4. Classic BT + LE coexistence on combo module; validate multipoint and iOS quirks early (iPhone HFP behavior).

---

## 5. iOS companion scope (v1)

- Pairing, firmware update, battery, LED preferences
- Account / agent session linking (API keys / OAuth — TBD product policy)
- Permissions: microphone (device-side), Bluetooth, notifications
- Call bridging controls and clear “Axiom is on this call” status
- Waitlist / Kickstarter deep link (marketing)
- **Not** in v1 scope unless resourced: Android, cellular modem, inductive MagSafe charge, multi-user household accounts

---

## 6. Acoustic design notes

- 4-mic array geometry locked to Ø78 footprint (board-edge placement)
- Sealed rear chamber for 20 mm speaker; mesh for dust/IP TBD (IP54 stretch goal)
- AEC / NS / beamforming on nRF5340 + optional offload — EVT decides DSP split

---

## 7. Manufacturing notes

| Stage | Approach |
|-------|----------|
| Housing | **CNC aluminum** for EVT/DVT; evaluate **MIM + anodize** or forged blank + CNC finish for volume |
| PCBA | SMT (0402/0201 mix as needed), double-sided as density requires; nRF5340 + Wi-Fi/BT module footprint |
| Battery | UN38.3 certified pack from qualified cell vendor; protection PCB; shipping compliance |
| Magnets | Supplier with MagSafe-compatible ring experience; fixture for pull-force QC |
| Final assembly | CM: magnet press-fit, battery, speaker, mesh, torque USB-C, seal, functional test (BT HFP, Wi-Fi, mics, charge) |
| Compliance | FCC / CE / (India WPC as needed); battery + wireless + EMC labs |

**CM tier:** Shenzhen / Foxconn-tier *mid* volume partner (not necessarily Foxconn brand) — see `outreach/SUPPLIERS.md`.

---

## 8. What this spec is / isn’t

- **Is:** Locked product definition for brand, Kickstarter, pitch, and supplier outreach.
- **Isn’t:** A certified production BOM, regulatory approval, or measured battery report. Update after EVT.
