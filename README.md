# Power trading signal: public track record

By Connor Slattery

A daily paper-trading test (no real money) of a signal for day-ahead vs real-time electricity
prices, run separately in five US power markets. The signal and its research are private. This
repo is the public, timestamped proof that every decision was made before the market, and the
season results.

## Markets

Each market has its own decisions, its own log and its own results. Nothing from one market
is used in another. Each folder has a short explanation and that market's fingerprints.

| Market | Rules | Decisions sealed |
|---|---|---|
| [PJM](markets/pjm/README.md) | PJM v1, PJM v2 | 0 |
| [New York](markets/new-york/README.md) | NY v3 | 0 |
| [SPP](markets/spp/README.md) | SPP v4 | 0 |
| [MISO](markets/miso/README.md) | MISO v4 | 0 |
| [California](markets/california/README.md) | California v4 | 0 |


## Season results (per MW, after a $0.75/MWh trading cost)

0 decisions sealed so far. Season totals are posted when the season ends (winter 2026-27: March 1, 2027).

Updated 2026-11-07.

## How it can be checked

1. **Every decision is sealed before the market.** Its SHA-256 fingerprint goes into
   [`commitments.csv`](commitments.csv) (all markets) and into that market's folder the day it's
   made, in a dated commit. Every in-season
   day gets one, whether it traded or not, and each sealed file has a random nonce, so the
   fingerprint gives nothing away.
2. **Every fingerprint gets an outside timestamp** from [OpenTimestamps](https://opentimestamps.org)
   in [`timestamps/`](timestamps/). It anchors the fingerprint in the Bitcoin blockchain, a public
   record nobody can edit or backdate, including us. Check any of them with the free
   `ots verify` tool.
3. **Season totals are posted when the season ends** (winter 2026-27: March 1, 2027).
4. **Full verification is available privately.** Under NDA, the decision files and per-trade
   scores can be shared. Each file's SHA-256 must match the fingerprint posted here on that day.
5. **The rules are locked** for the whole 2026-27 winter. No changes mid-season.

Paper trading only. Not investment advice. Results are hypothetical and ignore some real
costs (market uplift charges, collateral).
