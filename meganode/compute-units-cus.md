---
description: Explanation for Compute Unite and how it works
---

# Compute Units (CUs)

Compute Unit is a way to measure your RPC request usage on MegaNode. We provide each MegaNode user a monthly quota of usage, and each method will consume a cost based on the resource required for execution. You can think of this as you have a balance in your account and each method has its own price. This will be deducted from your account upon submission of RPC requests. The price of each RPC method is called Compute Unit. Based on this calculation, we enable our users to utilize the monthly request quota more efficiently. In short, you only pay for what you use.

{% hint style="info" %}
For different subscription tiers, there may have different monthly usage quotas.
{% endhint %}

## CUs of RPC Method

Below are the CUs for each method. We define the CUs based on the resource required for execution.&#x20;

### Supported Method

**BSC, Ethereum & Polygon**

| Method                                   | CUs  |
| ---------------------------------------- | ---- |
| eth\_accounts                            | 5    |
| eth\_blockNumber                         | 5    |
| eth\_chainId                             | 5    |
| eth\_syncing                             | 5    |
| net\_listening                           | 5    |
| net\_version                             | 5    |
| web3\_clientVersion                      | 5    |
| eth\_subscribe                           | 10   |
| eth\_uninstallFilter                     | 10   |
| eth\_unsubscribe                         | 10   |
| web3\_sha3                               | 10   |
| eth\_gasPrice                            | 15   |
| eth\_getBalance                          | 15   |
| eth\_getBlockByNumber                    | 15   |
| eth\_getCode                             | 15   |
| eth\_getStorageAt                        | 15   |
| eth\_getTransactionByBlockHashAndIndex   | 15   |
| eth\_getTransactionByBlockNumberAndIndex | 15   |
| eth\_getTransactionByHash                | 15   |
| eth\_getTransactionReceipt               | 15   |
| eth\_getBlockByHash                      | 18   |
| eth\_getBlockTransactionCountByHash      | 18   |
| eth\_getBlockTransactionCountByNumber    | 18   |
| eth\_getFilterChanges                    | 18   |
| eth\_newBlockFilter                      | 18   |
| eth\_newFilter                           | 18   |
| eth\_newPendingTransactionFilter         | 18   |
| eth\_call                                | 20   |
| eth\_getProof                            | 20   |
| eth\_getTransactionCount                 | 25   |
| eth\_getFilterLogs                       | 50   |
| eth\_getLogs                             | 50   |
| eth\_estimateGas                         | 75   |
| eth\_sendRawTransaction                  | 150  |
| debug\_traceTransaction                  | 280  |
| debug\_traceCall                         | 280  |
| debug\_traceBlockByNumber                | 1800 |
| debug\_traceBlockByHash                  | 1800 |

**Ethereum only**

| Method                             | CUs |
| ---------------------------------- | --- |
| eth\_protocolVersion               | 5   |
| eth\_createAccessList              | 10  |
| eth\_feeHistory                    | 10  |
| eth\_maxPriorityFeePerGas          | 10  |
| eth\_getUncleByBlockHashAndIndex   | 15  |
| eth\_getUncleByBlockNumberAndIndex | 15  |
| eth\_getUncleCountByBlockHash      | 15  |
| eth\_getUncleCountByBlockNumber    | 15  |

**Polygon API**

| Method                             | CUs |
| ---------------------------------- | --- |
| bor\_getAuthor                     | 15  |
| bor\_getCurrentProposer            | 15  |
| bor\_getCurrentValidators          | 15  |
| bor\_getRootHash                   | 15  |
| bor\_getSignersAtHash              | 15  |
| eth\_getTransactionReceiptsByBlock | 250 |

**Optimism API**

| Method             | CUs |
| ------------------ | --- |
| eth\_getBlockRange | 25  |
| rollup\_getInfo    | 15  |
| rollup\_gasPrices  | 15  |

****

**Enhanced API**

| Method                                  | CUs  |
| --------------------------------------- | ---- |
| eth\_getDiffAccounts                    | 1000 |
| eth\_getDiffAccountsWithScope           | 1200 |
| nr\_getTokenBalance20                   | 25   |
| nr\_getTokenBalance721                  | 25   |
| nr\_getTokenBalance1155                 | 25   |
| nr\_getTokenMeta                        | 80   |
| nr\_getTotalSupply20                    | 25   |
| nr\_getTotalSupply721                   | 25   |
| nr\_getTransactionReceiptsByBlockHash   | 250  |
| nr\_getTransactionReceiptsByBlockNumber | 250  |

### Unsupported Method

If MegaNode received requests using unsupported RPC method, the CUs are **2** for each request.

### How does MegaNode calculate my monthly quota?

We accumulate the monthly usage by account. Regardless of how many apps you created in your account, we calculate the usage by summing the entire usage across apps.

## Websocket subscription

&#x20;MegaNode charges the websocket subscription by bandwidth. For every byte, the cost is 0.04 CU.

### What happens if I run out of monthly quota?

If you keep sending RPC request even though you've reached the monthly quota, the request will fail and you will receive http 429 error and an error code: -**32005**

```
{
   "jsonrpc":"2.0",
   "id":1,
   "error":{
      "code":-32005,
      "message":"limit exceeded"
   }
}
```

### What happens if I send a request with incorrect payload?

If you're sending a RPC request with an incorrect payload, it will cost:

* **If incorrect method**: it will cost you 2 usage for incorrect or unsupported RPC method.
* **If other parameters are incorrect, or execution failed due to the wrong payload**: it will consume the original cost of each method.

### How much monthly quota do I have?

We provide MegaNode users different tiers of monthly quota according to their pricing plan. Pleaserefer to our [pricing plan](pricing-plan/).

