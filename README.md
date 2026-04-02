# Undertow

Undertow tracks three registers simultaneously at the world's major 
shipping chokepoints — Hormuz, Suez, Panama — and surfaces the 
relationship between them.

**Flow** — what is physically moving. Vessels, oil, grain.  
**Market** — what price signals say. Futures, freight rates, 
war-risk insurance.  
**Felt** — what people collectively register. News volume, 
narrative spread, and public awareness.

The primary signal is the gap between physical reality and collective 
felt experience — both its magnitude and its direction (whether awareness 
is lagging or running ahead). When that gap is large and widening, the 
system makes it visible. When a gap resembles a historically significant 
configuration, a reference point surfaces — not a forecast, a parallel.

The system is designed to make moments of misalignment visible — when 
decisions are being made under conditions that are not yet widely understood.

## What it shows

At any given moment, the three registers at each chokepoint may be 
aligned, diverging, or moving in opposite directions. The system encodes 
both the magnitude of that divergence and its rate of change — a small 
gap widening fast is an earlier signal than a large gap that has been 
stable for months or years.

## Current state

Hormuz is currently in a near-closure state following recent military 
escalation in the region. Physical flow is at approximately 6% of normal. 
Market signal is extreme. Collective sentiment is rising but still lagging 
the physical reality. The gap is wide and the system shows it.

## Technical

Single HTML file. Canvas rendering. Live data via Yahoo Finance 
(Brent crude) and GDELT (news sentiment). Falls back to a calibrated 
model when data is unavailable. No server required — deploy anywhere 
that serves static files.
