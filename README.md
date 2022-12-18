# Gas Fee Estimator

Many apps like to offer users the option to set their own gas fee bids with a "slow", "average", and "fast" option. With this app, we will go through building these options with the eth_feeHistory API post London fork. We will also use the eth_maxPriorityFeePerGas method and replicate the calculation it performs. 

## Application

This code would not be particularly viable in production. Running these calculations every time we need an estimate is not practical for an application that might be serving thousands of transactions per second.

Geth consults what's known as an "Oracle" whare area software actor whose only job is to keep track of historical blocks and keep the gas estimates up to date. Then Geth will simply ask the oracle "what is the current estimate" and get back an immediate response. 