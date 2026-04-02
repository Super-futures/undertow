# Undertow

Live: https://super-futures.github.io/undertow/

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
is lagging or running ahead). When that gap becomes significant, the 
system makes it visible.

The system is designed to surface moments of misalignment — when decisions 
are being made under conditions that are not yet widely understood.

When a gap becomes significant, the system provides a two-line reading: 
a structural classification of the configuration, followed by a brief 
indication of how that condition typically becomes visible in everyday 
experience (e.g. through prices, delays, or availability).

## What it shows

At any given moment, the three registers at each chokepoint may be 
aligned, diverging, or moving in opposite directions. The system encodes 
both the magnitude of that divergence and its rate of change — a small 
gap widening quickly is an earlier signal than a large gap that has been 
stable over time.

These conditions are also expressed in a minimal textual form to support 
rapid interpretation without requiring prior knowledge of the system.

## Current state

Hormuz is currently in a near-closure state following recent regional 
escalation. Physical flow is significantly reduced, market signals are 
elevated, and collective sentiment is rising but still lagging the 
physical reality. The gap is wide and the system shows it.

Suez is experiencing secondary pressure as vessels reroute, creating 
delays that propagate through shipping and retail systems. Market and 
sentiment signals are elevated but uneven.

Panama represents a slower constraint. Environmental limits on capacity 
have persisted over time, with markets adjusted but public awareness 
remaining low. The disruption is gradual and less visible.

## Technical

Single HTML file. Canvas rendering. Live data via Yahoo Finance 
(Brent crude) and GDELT (news sentiment). Falls back to a calibrated 
model when data is unavailable. No server required — deploy anywhere 
that serves static files.
