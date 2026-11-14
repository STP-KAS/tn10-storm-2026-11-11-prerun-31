> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value.

# Predictions (written before any submit)

Pre-run 30's 840-input rejection said transient mass 1,814,984. That matches `4 × (146 + 540 × inputs)` for this script: each input's estimated size is 540 bytes (36-byte outpoint, 8-byte script length, 488-byte signature script, 8-byte sequence) and the rest of the transaction is 146 bytes. Transient mass in v2.1.0 is that estimated size times 4. The mempool refuses transient mass over 1,000,000.

| Inputs | Estimated size, bytes | Transient mass | Guess |
|---:|---:|---:|---|
| 462 | 249,626 | 998,504 | accepted |
| 463 | 250,166 | 1,000,664 | rejected, and the node's error names 1000664 |

If the node names a different mass, the size model is wrong and the count file says so. We do not edit this page after the submits. A wrong row is the lesson.
