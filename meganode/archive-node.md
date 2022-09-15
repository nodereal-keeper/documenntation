---
description: >-
  MegaNode provides archive data and debug API on archive node. This document
  describe the detailed information about how it works in MegaNode
---

# Archive Node

{% hint style="info" %}
Archive node is available on BNB Chain & Ethereum now!
{% endhint %}

Archive node has all the historical data of the blockchain. In some cases, if you need to access the data from earlier blocks, you will need to access the archive node. It requires huge storage to run an archive node, and typically due to this huge amount of data, it takes a longer time to process.

MegaNode provides industry-leading capabilities for archive node on BSC. It is the fastest and always consistent. Here is the response time on different percentiles and QPS for BSC.

| QPS    | Avg. response time | 90th percentile response time |
| ------ | ------------------ | ----------------------------- |
| 1,000  | 15ms               | 22ms                          |
| 10,000 | 23ms               | 37ms                          |

## Archive data

MegaNode provides archive data accessibility to all tiers of customers with no additional fee required! If your application requires historical data, you can request using the below JSON-RPC methods.

* eth\_getBalance
* eth\_getProof (only available on BSC)
* eth\_getCode
* eth\_getStorageAt
* eth\_call
* eth\_estimateGas
* eth\_getTransactionCount

## Debug API

Debug API helps you to reply to the transactions that may have been executed prior in the same manner. It requires higher cost and response time due to its maintenance and infrastructure cost.

* debug\_traceTransaction
* debug\_traceCall
* debug\_traceBlockByNumber
* debug\_traceBlockByHash

