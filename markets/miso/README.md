# MISO

Part of the [public track record](../../README.md). By Connor Slattery.

**Market:** MISO (Midwest and South, Minnesota to Louisiana). Average of MISO's 8 hubs.

**What is tested:** each day in winter (December to February), a locked rule decides whether to
take a 1 MW paper position between this market's day-ahead and real-time prices for the next day,
or stay out. No real money. Results are per MW after a $0.75/MWh trading cost. How the rule
decides, and which way it trades, is private.

**When:** Decided each morning by 8:45 am Central, before MISO's day-ahead deadline. Days the decision computer missed are logged as missed, not filled in later.

**Rules tracked here:** MISO v4. Locked for the whole 2026-27 winter. This market is decided and
scored on its own: no other market's data or results feed into it.

**Proof:** 0 decisions sealed so far, listed in [`commitments.csv`](commitments.csv) with their
SHA-256 fingerprints. Each one is timestamped in the Bitcoin blockchain through OpenTimestamps
(proofs in the main [`timestamps/`](../../timestamps/) folder). Season totals are posted
here and in the main README after each season ends (March 1, 2027).
