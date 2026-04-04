# Undertow

Undertow tracks three registers simultaneously at the world's major shipping chokepoints — Hormuz, Suez, Panama — and surfaces the relationship between them.

**Flow** — what is physically moving. Vessels, oil, grain.  
**Market** — what price signals say. Futures, freight rates, war-risk insurance.  
**Felt** — what people collectively register. News volume, narrative spread.

The primary signal is the gap between physical reality and collective felt experience. When that gap is significant, the system shows its configuration — whether physical reality is running ahead of collective awareness or behind it, and whether the gap is widening or closing — alongside the channel through which it is most likely to become visible in daily life.

## What it shows

At any given moment, the three registers at each chokepoint may be aligned, diverging, or moving in opposite directions. The system encodes both the magnitude of that divergence and its rate of change — a small gap widening fast is an earlier signal than a large gap that has been stable for months.

Ghost traces show where each register was over the past three 90-second intervals, making trajectory legible without charts. The gap line between physical flow and felt experience weights and animates in proportion to divergence speed — faster dash movement when widening, slower when closing.

Each node breathes independently: the three visual layers (flow circle, market rect, sentiment glow) oscillate at their own rates and phases, so the field is never fully at rest.

## Current state (April 2026)

**Hormuz** is near-total closure following the 2026 US-Israel strikes on Iran. Physical flow is approximately 6% of normal — around 1–2 million barrels per day moving via the IRGC toll route through Larak Island, compared to 20 million barrels per day in normal conditions. Market signal is extreme. Collective sentiment is rising but still lagging the physical reality significantly. The gap is wide.

**Suez** is operating at roughly 48% of its 2023 peak — around 29 vessels per day against a normal 60. Houthi risk on the Red Sea approach and major carrier withdrawals (Maersk, CMA CGM) remain the structural constraint. Some recovery from Hormuz-displaced container traffic partially offsets this.

**Panama** has recovered from the 2023–2024 drought. The canal is operating at approximately 78% of normal capacity — around 31 vessels per day — with 50ft draught maintained. Ongoing post-drought structural residual: LNG traffic has not returned to pre-drought levels.

## Signal layer

When a gap is significant (>10% magnitude), the system surfaces a two-line entry at the base of the field:

- **Line 1** — configuration: what kind of gap this is and whether it is widening or closing
- **Line 2** — transmission: where this would become visible in everyday life — fuel prices, delivery times, food costs

The signal shows for the node with the largest current gap. Clicking a node or its panel locks the signal to that node.

No historical citations. No forecasts. The signal describes current structure and its likely transmission into lived experience.

## Flow model

Flow at each node is a derived value — never set directly from external data:

```
Flow = clamp(1 − constraint − event, floor, ceiling)
```

**Constraint** encodes structural restriction: geopolitics, insurance reclassification, permanent rerouting. It hardens slowly under sustained disruption and softens three times more slowly than it hardened.

**Event** encodes acute disruption. It decays using plateau logic — above a node-specific threshold, decay is 85% slower (conflict self-sustains); below it, 80% faster (minor incidents resolve). During active decay, there is a small probability of re-spiking, preventing clean monotonic resolution.

**Physical calibration (v1.3):**

| Node | Flow = 1.0 | Flow = 0.5 | Floor |
|------|-----------|-----------|-------|
| Hormuz | 20 mb/d, 138 vessels/day | ~10 mb/d | 0.05 (~1 mb/d shadow fleet) |
| Suez | ~60 vessels/day, 1.6 Bn t/yr | ~30 vessels/day | 0.28 (~17 vessels/day) |
| Panama | 38 vessels/day, 50ft draught | ~19 vessels/day | 0.47 (Feb 2024 drought worst) |

External data adjusts model components (constraint, event), not flow directly. Confidence in the model decays exponentially with time since last anchoring signal (48-hour halflife, floor 0.2), encoded in the visual weight of the physical flow layer.

**Tension dynamics:** values resist settling — they hold near a position, then shift more abruptly than smooth interpolation would suggest. Sentiment accumulates pressure before snapping. Market and sentiment carry biased noise that self-reinforces current trends. Cross-node tension propagates probabilistically: Hormuz events occasionally spike Suez sentiment; sustained Suez constraint ripples into Panama market.

## Data sources

**Live (no key required):**
- Yahoo Finance — Brent Crude (BZ=F) → Hormuz and Suez market signal
- Yahoo Finance — Baltic Dry Index (^BDI) → Suez and Panama market signal
- GDELT 2.0 — news sentiment per chokepoint (120-minute window, keyword-filtered)
- Panama Canal Authority — Gatun Lake water level CSV → Panama constraint anchoring

**Keyed (add API key to activate):**
- MarineTraffic — vessel density at chokepoint bounding boxes → flow anchoring (confidence 0.85)
- Freightos FBX — container freight rates FBX13/FBX11 (Suez), FBX01 (Panama) → market signal

Data sources poll every 10 minutes. Active sources shown in the header data indicator. The system falls back to the calibrated model when live data is unavailable — model confidence is visible in the rendering (softer, wider halo when unanchored; crisper when freshly anchored).

## Technical

Single HTML file. Canvas 2D rendering. No build step, no server required — deploy anywhere that serves static files.

```
https://super-futures.github.io/undertow/
```

Fonts: Libre Baskerville (serif) + DM Mono. Colour system: warm parchment ground, three semantic register colours (physical green, market blue, sentiment sienna), divergence red.

## Lineage

Undertow is a project in the Animal Spirits lineage — which maps collective affect and economic behaviour across regions. The extension is the material substrate: the physical flows of oil, grain, and goods that sentiment and markets are ultimately entangled with.

The name comes from what the system tracks — the force beneath the visible surface that determines where things are actually heading, regardless of what's visible above it.
