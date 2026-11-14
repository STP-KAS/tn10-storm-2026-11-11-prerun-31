> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value.

# Lock (pre-run 31)

Locked before the first submit.

- Network: Testnet-10. Desk node only. The desk node is not restarted.
- Script: the pre-run 30 P2SH redeem, unchanged.
- Knob: input count. The two submits are 463, then 462.
- Fee: twice the SDK mass, sompi per gram, plus 1,000 sompi.
- Funding: about 500 outputs of 1 tKAS from key 0, then the leftovers return to key 0.
- No public send. No Mini. No families. No guest.
- Disk line: abort if the desk is under 150 GB free. It was 340.3 GB when this was written.
- A miss is a retry with the fix written first. This page is not rewritten to match the result.
