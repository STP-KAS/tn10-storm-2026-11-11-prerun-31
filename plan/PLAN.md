> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value.

# Plan (pre-run 31)

One question. Pre-run 30 showed a 170-input spend of our P2SH script accepted, and an 840-input spend rejected because its transient mass was over 1,000,000. We want the exact input count where that same script shape crosses the line.

## What we send

- Desk private node only. Testnet-10 only. No public node. No Mini.
- The same redeem script pre-run 30 already used (485 bytes). We do not print it.
- First, our own coins are split into about 500 outputs of 1 tKAS locked to that script.
- Then one spend of 463 of those outputs back to the sender, then one spend of 462. A rejection does not spend the coins. Whatever is left comes back in batches of at most 50.
- The fee is priced the way pre-run 30's retry priced it: twice the SDK mass, in sompi per gram, plus a small pad. The node still decides.

## What we will not do

- No restart of the desk node.
- No families, no heavy lane, no guest, no payment load.
- No compile. No second node. No disk-heavy directory.
- Keys 1 and 2 stay unused.

## Gate, written before the open

- Desk free space was 340.3 GB, above the 150 GB line.
- Key 0, read on the desk node before this file: 8,088 coins, 3,381 of them over 3 tKAS, about 107,420 usable tKAS. Projected end stays above 26,000 usable tKAS and above 2,500 coins over 3 tKAS. This probe moves about 500 tKAS into the script outputs and pays fees on the way back. No refill.
- The free check is a read-only pass on the published names, logged in the private run notes. It does not send.

## Done when

The node's own answer names an accepted input count and the next count rejected for transient mass, and the two counts differ by 1. The numbers in [plan/PREDICTIONS.md](PREDICTIONS.md) are the guess. The count file is what the node said.
