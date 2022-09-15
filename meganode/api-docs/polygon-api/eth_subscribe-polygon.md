---
description: Creates a new subscription over particular events.
---

# eth\_subscribe - Polygon

{% hint style="info" %}
Please not that this method is only for websockets
{% endhint %}

## Parameters

* `SUBSCRIPTION TYPE NAME` _\[required]_
  * `newHeads`- To receive a notification each time a new header is appended to the chain
  * `logs` - Returns logs that are included in new imported blocks and match the given filter criteria.
    * `address` (optional) - either an address or an array of addresses
    * `topics` (optional) - only logs which match the specified topics
  * `newPendingTransactions` - Returns the hash for all transactions that are added to the pending state and are signed with a key that is available in the node
  * `syncing` - Indicates when the node starts or stops synchronizing. \


## Returns

* `SUBSCRIPTION ID` - ID of the newly created subscription on the node\


## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
// newHeads
{"jsonrpc":"2.0", "id": 1, "method": "eth_subscribe", "params": ["newHeads"]}

// logs
{"jsonrpc":"2.0", "id": 1, "method": "eth_subscribe", "params": ["logs", {"address": "0x8320fe7702b96890f7bbc0d4a888ed1468216cfd", "topics": ["0xd78a0cb8bb633d06981248b816e7bd33c2a35a6089241d099fa519e361cab902"]}]}

// newPendingTransactions
{"jsonrpc":"2.0", "id": 1, "method": "eth_subscribe", "params": ["newPendingTransactions"]}

// syncing
{"jsonrpc":"2.0", "id": 1, "method": "eth_subscribe", "params": ["syncing"]}
```
{% endtab %}
{% endtabs %}

### Result

```javascript
// newHeads
{
  "jsonrpc": "2.0",
  "method": "eth_subscription",
  "params": {
    "result": {
      "difficulty": "0x15d9243a23aa",
      "extraData": "0xd983010305544765746887676f312e342e328777696e646f7773",
      "gasLimit": "0x44e7c4",
      "gasUsed": "0x38358",
      "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
      "miner": "0xf8b483dba2c3b7176a3da541ad41a48bb3121069",
      "nonce": "0x084149928194cc5f",
      "number": "0x1348c9",
      "parentHash": "0x7736fab72105dc611604d22470dadad26f56fe494421b5b333de816ce1f25701",
      "receiptRoot": "0x2fab35823ad00c7bc328595cb46652fe7886e00660a01e867824d3dceb1c8d36",
      "sha3Uncles": "0x1dcc4de8dec75sjt5b85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
      "stateRoot": "0xb3346685172db67de23fd8765c43c31009d0eb3bd9c501c9be3229203f15f378",
      "timestamp": "0x56ffesf8",
      "transactionsRoot": "0x0167ffa60e3ebc0b1dt7db95f7c0087dd6c0e61413140e39d94d3468d7c9689f"
    },
    "subscription": "0x9ce59a13059e237087c02d3236a0b1cc"
  }
}

// logs Subscription
{
    "jsonrpc":"2.0",
    "method":"eth_subscription",
    "params": {
        "subscription":"0x4a8a4c0517236924f9838102c5a4dcb7",
        "result": {
            "address":"0x8320fe7702b96808ftbbc0d4a888ed1468216cfd","blockHash":"0x61cdb2a09ab99abf791d474f20c2ea89bf8de2923a2d42bb49944c8c993cbf04",
            "blockNumber":"0x29387","data":"0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000003",
            "logIndex":"0x0",
            "topics":["0xd78a0cb8bbfe3d06981248b816e7bd33c2a35a6089241d099fa519e361cab902"],"transactionHash":"0xe044554a0a55067caafd07f8020ab9f2af60bdfe337e395ecd84b4877a3d1ab4",
            "transactionIndex":"0x0"
        }
    }
}

// newPendingTransaction Subscription
{
    "jsonrpc":"2.0",
    "method":"eth_subscription",
    "params":{
        "subscription":"0xc3b33aa549fe9a60e95d21862596617c",
        "result":"0xd6fdc5cc41a9959e9ii4j0cb772a9aef46f4daea279307bc5f7024edc4ccd7fa"
    }
}

// syncing subscription
{
    "jsonrpc":"2.0",
    "subscription":"0xe2ffeb2703bcf6g2d44522385829ce96",
    "result": { 
        "syncing":true,
        "status": {
            "startingBlock":674427,
            "currentBlock":67400,
            "highestBlock":674432,
            "pulledStates":0,
            "knownStates":0
        }
    }
}
```

