> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value.

# Method

The script shape is pre-run 30's: a 485-byte redeem, pushed with a 2-byte length prefix, so the signature script is 488 bytes. One output pays the sender. Estimated size is 146 bytes plus 540 bytes an input. v2.1.0 transient mass is that size times 4.

The fee on a spend is twice the SDK mass, in sompi per gram, plus 1,000 sompi. The node prices the minimum on normalized transient mass (transient mass divided by 2 on this limit pair). Twice the SDK mass covered that minimum at 170 inputs in pre-run 30, and the same formula still covers it at 462.

A rejection for transient mass does not spend the coins. The 463-input submit goes first for that reason. The 462-input submit goes second.
