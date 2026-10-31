# Power trading signal: public track record

By Connor Slattery

A daily paper-trading test (no real money) of a signal for day-ahead vs real-time electricity
prices in PJM and New York. The signal and its research are private. This repo is the public,
timestamped proof of what it called, and when.

## Live results (per MW, after a $0.75/MWh trading cost)

0 decisions sealed so far. Decisions and results are revealed together when the season ends (winter 2026-27: March 1, 2027).

Updated 2026-10-31. Every scored trade: [`results.csv`](results.csv).

## How to check it

1. **Every decision is sealed before the market.** Its SHA-256 fingerprint goes into
   [`commitments.csv`](commitments.csv) the day it's made, in a dated commit.
2. **When the season ends, every decision is revealed** in [`decisions/`](decisions/)
   (winter 2026-27: March 1, 2027). Hash each one and compare: `sha256sum decisions/<file>.json` (or `Get-FileHash` on Windows). Each file has a
   random nonce, so the fingerprint can't be guessed ahead of time.
3. **Scores** use the markets' final published prices and are listed in `results.csv`.
4. **The rules are locked** for the whole 2026-27 winter. No changes mid-season.

Paper trading only. Not investment advice. Results are hypothetical and ignore some real
costs (market uplift charges, collateral).
