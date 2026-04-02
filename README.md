# Undertow

Undertow tracks three registers simultaneously at the world's major 
shipping chokepoints — Hormuz, Suez, Panama — and surfaces the 
relationship between them.

**Flow** — what is physically moving. Vessels, oil, grain.  
**Market** — what price signals say. Futures, freight rates, 
war-risk insurance.  
**Felt** — what people collectively register. News volume, 
narrative spread.

The primary signal is the gap between physical reality and collective 
felt experience. When that gap is significant, the system shows its 
configuration — whether physical reality is running ahead of collective 
awareness or behind it, and whether the gap is widening or closing — 
alongside the channel through which it is most likely to become visible 
in daily life.

## What it shows

At any given moment, the three registers at each chokepoint may be 
aligned, diverging, or moving in opposite directions. The system encodes 
both the magnitude of that divergence and its rate of change — a small 
gap widening fast is an earlier signal than a large gap that has been 
stable for months.

Ghost traces show where each register was in recent intervals, making 
trajectory legible without charts. The gap line between physical and 
felt experience weights and animates in proportion to divergence speed.

## Current state

Hormuz is near-total closure following the 2026 US-Israel strikes on 
Iran. Physical flow is at approximately 6% of normal. Market signal is 
extreme. Collective sentiment is rising but still lagging the physical 
reality. The gap is wide and widening.

Suez is elevated — receiving rerouting pressure from Hormuz and residual 
Houthi risk on the Red Sea approach. Panama carries ongoing 
drought-related draught restrictions with very low public awareness.

## Signal layer

When a gap is significant, the system surfaces a two-line entry:

- **Line 1** — configuration: what kind of gap this is and whether it 
is widening or closing
- **Line 2** — transmission: where this would become visible in 
everyday life — fuel prices, delivery times, food costs

No historical citations. No forecasts. The signal describes current 
structure and its likely transmission into lived experience.

## Technical

Single HTML file. Canvas 2D rendering. Live data via Yahoo Finance 
(Brent crude) and GDELT (news sentiment), polled every 10 minutes. 
Falls back to a calibrated model when data is unavailable. No server 
required — deploy anywhere that serves static files.
