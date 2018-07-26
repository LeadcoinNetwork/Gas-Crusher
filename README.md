# Gas-Crusher

[Read about the gas crusher](https://blog.leadcoin.network/leadcoin-unveils-the-gas-crusher.html)

[https://blog.leadcoin.network/leadcoin-unveils-the-gas-crusher.html](https://blog.leadcoin.network/leadcoin-unveils-the-gas-crusher.html)

## Technical Details:

Each transaction on the blockchain uses gas. For a simple Ethereum token transfer between personal wallets (non-smart contract), the gas needed is 21,000. Then you can specify your gas price. For instance, if you choose 15 Gwei, your transaction will cost the gas needed times the cost per gas unit, meaning 315,000 Gwei or 0.000315 Ether (~$0.15).

This is for a regular Ethereum transfer. When transferring tokens, the gas amount is actually higher, at about 50,000 gas units for transferring to a new wallet. The reason is that creating a new wallet requires new memory on the blockchain, and memory costs an additional fee.

So there are two ways of reducing transaction costs:

1.  Choose a lower gas price

2.  Find a way to reduce the amount of gas units needed for each transfer

When you choose a lower gas price, e.g. 7 Gwei, when the Ethereum network is busy (as has been the case lately), it can take several hours to enter a block, and you must wait for the transaction to enter a block before submitting a new transaction. Ethereum does not support parallel transactions from the same wallet. In our case, we had to transfer tokens to 520 bounty winners. So it could have taken 4 hours \* 520 transactions = almost three months; way too long. So if you don’t want to wait so long when the network is busy, you need increase the gas price to about 40 Gwei.

Instead, we developed a new smart contract, which supports transferring tokens to an almost unlimited number of users in one transaction. Then we transferred all the tokens to the new smart contract and executed all the transactions at once for one low gas price 7Gwei . When the block entered the blockchain, all the transactions came together in one piece, taking only 35,000 gas units per transfer, and we only had to wait two hours instead of three months.

To sum up, the regular price would have been 50,000 gas units _ 40 Gwei _ 520 = 1.04 Ether, which would allow us to make 520 transactions in a couple of hours over a busy network.

Instead we paid: 35,000 gas units per transfer _ 7 Gwei _ 520 = 0.1274 Ether in one transaction, saving over 85% in gas fees!
