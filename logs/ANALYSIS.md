> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value.

# Analysis

One node, one script shape, two input counts. We are just testing. This is not a claim about TN10 in general.

For this redeem, on our kaspad 2.1.0 desk node, 462 inputs are under the transient-mass limit and 463 inputs are over it. The node's rejection of 463 named 1000664, which is `4 × (146 + 540 × 463)`. The accepted 462-input transaction has transient mass 998,504 on that model, 1,496 under the 1,000,000 limit. Its SDK mass was 280,478. Pre-run 30 had 170 accepted and 840 rejected; this is the input where the same shape crosses.

The first 462-input submit is not a miss on that line. It was rejected for a sequence lock, and the retry of the same count landed. See [LESSONS](LESSONS.md). The count is [EDGES](../counts/EDGES.md).
