# Axiom — Investor Pitch

**Format:** 10–12 slide markdown deck  
**Founder:** Vaibhav Sharma (vaibhavjnf / hackdomland@gmail.com)  
**Ask context:** Raise + Kickstarter · India + global  
**Traction note:** Pre-campaign. No fabricated users, revenue, or LOIs.

---

## Slide 1 — Title

**axiom**  
Always-on agent. Desk to pocket.

Matte aluminum · Voice-first · MagSafe underside · Bluetooth call bridging · iOS companion  

Coming to Kickstarter · Raise in parallel  

Vaibhav Sharma · hackdomland@gmail.com

---

## Slide 2 — Problem

**Agents got good. The interface didn’t leave the phone.**

- Pro ChatGPT / agent era: models can plan, draft, and assist — but they still live behind unlock → app → tab.
- Desk work and calls are physical contexts; the best assistant shouldn’t disappear when you stand up or put the phone face-down.
- Speakers and earbuds are audio endpoints, not an *agent harness* with presence, array mics, and continuous identity.

**Honest framing:** This is a UX and form-factor gap in a world where software agents are already useful — not a claim that “AI doesn’t exist yet.”

---

## Slide 3 — Solution

**Axiom — a physical always-on agent.**

- Ø78 × 28 mm matte aluminum puck
- Voice-first: 4× MEMS mics + 20 mm speaker
- Desk dock via MagSafe-compatible underside (55 mm ring class); charge via flush USB-C
- Pocketable; ~½ day battery (~4000 mAh / ~15 Wh, ~12 h mixed-use design target)
- Bluetooth HFP bridges into the user’s phone calls
- iOS companion for pairing, status, privacy controls

**Tagline:** Always-on agent. Desk to pocket.

---

## Slide 4 — Product

**What you buy is an object — not a prompt.**

| | |
|--|--|
| Housing | Matte aluminum puck |
| Magnets | MagSafe-compatible ring |
| Port | Flush USB-C |
| Audio | 4-mic array + 20 mm speaker |
| Radio | nRF5340 + Wi-Fi/BT combo |
| App | iOS companion |

Visuals: `assets/axiom-hero.png`, `assets/axiom-exploded.png`  
Brand: lowercase wordmark, `#F5F5F7` / `#1D1D1F` / `#A1A1A6`

---

## Slide 5 — Tech

**Stack chosen for shippable v1, not demo theater.**

- **nRF5340** + Wi-Fi/BT combo — dual-core for audio DSP + connectivity
- **ICS-43434-class** digital MEMS ×4 — beamforming / AEC path
- **HFP call path** — Axiom as headset endpoint on the user’s phone call; agent data path separate; consent UX in iOS app
- **Battery math:** ~15 Wh → ~12 h at ~1.2 W blended average (EVT will measure; market as “about half a day”)
- **MFG:** CNC Al for EVT; MIM/anodize or CNC finish for volume; SMT + final assembly at mid-tier CM

No fake AI holograms. No cellular in v1. No inductive MagSafe power in v1 unless BOM revises.

---

## Slide 6 — Why hardware (moat thesis)

**Software agents are abundant; trusted physical presence is not.**

1. **Form factor lock-in** — desk object + pocket continuity is hard to copy with “just an app.”
2. **Audio + call path** — array + HFP bridging is an integration moat (iOS quirks, acoustic DFM, RF coexistence).
3. **Brand restraint** — Apple-level minimal in a noisy AI accessory market; trust via honesty (battery, Kickstarter timing).
4. **Supply chain learning** — enclosure, UN38.3 battery, MagSafe magnets, FCC/CE — compounds with each build.

**Not claimed:** patents filed, exclusive silicon, or network effects yet. Moat starts as execution + design taste + vertical integration of agent UX into hardware.

---

## Slide 7 — Market

**Category:** Consumer AI hardware / voice agent accessories / desk-pocket electronics.

**Beachhead:** Knowledge workers and founders already paying for Pro ChatGPT / agent tools who want a *physical* always-available endpoint.

**Expansion (later):** Android companion, accessories (desk mount SKUs), workplace variants — only after v1 ships.

**Honesty:** No TAM slide with invented billions. Market size to be diligenced with investor using public consumer electronics + AI subscription spend data. Thesis: if agent software ARPU is real, a premium hardware harness at Kickstarter/DTC price points can clear early demand *if* industrial design and call UX land.

---

## Slide 8 — GTM

**Kickstarter → DTC**

1. **Pre-launch** — landing waitlist, brand-consistent content, founder-led demo videos (real hardware when EVT exists)
2. **Kickstarter** — Early Bird / Standard / Duo / Founder tiers (see `kickstarter/CAMPAIGN.md`)
3. **Fulfillment** — CM + logistics; communicate risks honestly
4. **DTC** — axiom site post-campaign; iterate firmware + iOS
5. **India + global** — founder base in India; ship globally with compliance sequencing (FCC/CE/WPC as needed)

No “viral loop” fiction. Distribution = crowdfunding + founder network + organic product films.

---

## Slide 9 — Team

**Vaibhav Sharma** — Founder  
Handles: vaibhavjnf · Email: hackdomland@gmail.com  

Building Axiom end-to-end: product definition, brand, campaign, supplier outreach, raise.

**Hiring plan (use of funds):** hardware EE / FW, acoustic / RF consultant, iOS, DFM/CM liaison, ops for Kickstarter fulfillment.

**Advisory / full team:** open — not named here without commitments.

---

## Slide 10 — Ask

**Raise + Kickstarter in parallel.**

- Kickstarter validates demand and funds early production units.
- Equity/angel raise funds EVT→DVT, certifications, and team so campaign risk is reduced.

**Exact round size / valuation:** TBD in conversations — not invented in this deck.

**What we need from partners:** consumer hardware angels, AI×hardware investors, India deeptech, SF consumer electronics networks (see `outreach/INVESTORS.md`).

---

## Slide 11 — Use of funds (indicative)

| Bucket | Purpose |
|--------|---------|
| EVT / DVT hardware | Tooling, spins, acoustic & power characterization |
| Certifications | FCC / CE / battery UN38.3 / wireless |
| CM deposits & NRE | Enclosure, PCBA, magnets, assembly fixtures |
| iOS + firmware | Companion app, HFP reliability, OTA |
| Campaign & ops | Kickstarter creative, fulfillment buffer |
| Runway | Founder + early hires |

Percent splits locked with lead after diligence — table is directional only.

---

## Slide 12 — Close

**axiom** — Always-on agent. Desk to pocket.

Coming to Kickstarter. Honest engineering. No fake traction.

Vaibhav Sharma · hackdomland@gmail.com · vaibhavjnf

*Assets:* `site/` · `brand/` · `kickstarter/CAMPAIGN.md`
