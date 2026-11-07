# PJM

Part of the [public track record](../../README.md). By Connor Slattery.

**Market:** PJM, the largest US power market (13 states and DC, Mid-Atlantic to Chicago). Average of PJM's 12 trading hubs.

**What is tested:** each day in winter (December to February), and for PJM v2 also summer (June to September), a locked rule decides whether to
take a 1 MW paper position between this market's day-ahead and real-time prices for the next day,
or stay out. No real money. Results are per MW after a $0.75/MWh trading cost. How the rule
decides, and which way it trades, is private.

**When:** Decided each morning by 9:45 am Eastern, before PJM's 11 am day-ahead deadline, for the next day. Days the decision computer missed are logged as missed, not filled in later.

**Rules tracked here:** PJM v1, PJM v2. Locked for the whole 2026-27 winter. This market is decided and
scored on its own: no other market's data or results feed into it.

**Proof:** 0 decisions sealed so far, listed in [`commitments.csv`](commitments.csv) with their
SHA-256 fingerprints. Each one is timestamped in the Bitcoin blockchain through OpenTimestamps
(proofs in the main [`timestamps/`](../../timestamps/) folder). Season totals are posted
here and in the main README after each season ends (winter: March 1, 2027; summer: October 1).
