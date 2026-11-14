> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value.

# Edges

Our own desk node, kaspad 2.1.0, Testnet-10, synced. One script shape, the same as pre-run 30: a 485-byte redeem, a 488-byte signature script, one output back to the sender. No public send. The fee formula was not changed: twice the SDK mass, in sompi per gram, plus 1,000 sompi.

The size model, written before any submit, is 146 bytes plus 540 bytes an input, and transient mass is that size times 4. The prediction page is unchanged.

| Label | When (UTC) | Inputs | SDK mass | Transient mass (our model) | What the node said | Fee, tKAS | Where it is |
|---|---|---:|---:|---:|---|---:|---|
| cross-463 | 2026-11-14T11:00:11Z | 463 | 281,084 | 1,000,664 | rejected: `transaction transient (storage) mass of 1000664 is larger than max allowed size of 1000000` | 0 | not accepted |
| cross-462, first | 2026-11-14T11:00:11Z | 462 | 280,478 | 998,504 | rejected: `one of the transaction sequence locks conditions was not met` | 0 | not accepted |
| cross-462, retry | 2026-11-14T11:02:07Z | 462 | 280,478 | 998,504 | accepted | 0.560966 | one output in the sender's UTXO set, block DAA 623179244; not in the mempool |
| recover | 2026-11-14T11:04:29Z | 38 | 23,534 | 82,664 | accepted | 0.047078 | one output in the sender's UTXO set, block DAA 623180725; not in the mempool |

The fund was 25 transactions, 500 coins of 1 tKAS, fees 5.02912 tKAS. The 463-input rejection did not spend them. The accepted 462-input spend and the 38-coin return used all 500. At the close read, script coins left were 0, the mempool was 0, and the virtual DAA score was 623181977 (2026-11-14T11:06:36Z).

Fees paid: 5.637164 tKAS (fund 5.02912, the accepted 462-input spend 0.560966, the return 0.047078). The two rejections paid nothing.

The node's own number, 1000664, is the number in the prediction table. SDK mass of the accepted spend was 280,478, under the 500,000 compute limit. The limit that bound was transient mass.
