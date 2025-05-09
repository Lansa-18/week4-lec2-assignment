# week4-lec2-assignment

SelfDestructContract (CONTRACT ADDRESS) - 0x43F1DDbE9bEc683346853A8798F72458856178e2

My WhiteListedWalletAddress - 0x002AC60bA0D2b960bf67131307a40A4BadB18D3D

REPORT:
I began by writing a simple contract containing a selfdestruct function, which sends any ETH held in the contract to a specified address when invoked. I deployed this contract and funded it with 0.0005 ETH. Upon calling the destroyAndSend function, the contract self-destructed and transferred its balance to the target address.

Next, I interacted with the EtherVault contract at the provided address:
0x6dA826f51c447354f65A7480e5364672785C0417.

Before proceeding, I verified whether my address was already whitelisted by calling the appropriate function on the EtherVault contract.

After confirming my status, I deployed the SelfDestruct contract and executed its destroyAndSend function to send ETH to the EtherVault. This was the key action that triggered the expected behavior.

To verify the entire process, I checked the logs to retrieve the address of the deployed SelfDestruct contract. I then looked it up on the testnet block explorer. The transaction history showed two key events:

The contract creation

The execution of the destroyAndSend function

This confirmed that the contract was deployed and successfully executed the self-destruct call, transferring the required amount of ETH to the EtherVault.
