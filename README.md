# Gas Fee Estimator

Many apps like to offer users the option to set their own gas fee bids with a "slow", "average", and "fast" option. With this app, we will go through building these options with the eth_feeHistory API post London fork. We will also use the eth_maxPriorityFeePerGas method and replicate the calculation it performs. 