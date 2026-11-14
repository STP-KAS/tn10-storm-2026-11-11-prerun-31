> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value.

# Lessons

Both rows on the prediction page held. We do not edit that page.

- 463 inputs were rejected, and the node named transient mass 1000664 against a limit of 1000000. That is the mass the size model named before the submit.
- 462 inputs were accepted on the retry and landed. SDK mass was 280,478. The node's transient-mass check had already passed: a mass failure would have been the error, as it was for 463.
- The first 462-input submit was our timing. The coins had just been accepted, and the transaction we built had sequence 0, so the relative lock was on with a relative lock of 0. The node rejected it with `one of the transaction sequence locks conditions was not met`. About two minutes later the same input count, the same coins and the same fee were accepted. Mass was not the reason. Next time we wait until the coins' block DAA is behind the tip before the first spend.
- The mass check is reported before the sequence check. 463, submitted in the same second as the first 462, reported the mass error and did not mention a sequence lock.
- All 500 script coins came back: 462 in the accepted spend, 38 in one return batch. Script coins left at the close read: 0.
- The desk node was not restarted. Nothing was sent to a public node.
