---
description: >-
  Returns information about a transaction by block hash and transaction index
  position.
---

# eth\_getTransactionByBlockHashAndIndex - Polygon

### Parameters

`DATA`, 32 Bytes - hash of a block.

`QUANTITY` - integer of the transaction index position.

```javascript
params: [ 
    '0xc0f4906fea23cf6f3cce98cb44e8e1449e455b28d684dfa9ff65426495584de6', 
    '0x0' // 0 
]
```

###

### Returns

* `TRANSACTION` - A transaction object, or null when no transaction was found
  * `hash`: 32 Bytes - hash of the transaction.
  * `nonce`: the number of transactions made by the sender prior to this one.
  * `blockHash`: 32 Bytes - hash of the block where this transaction was in. null when its pending.
  * `blockNumber`: block number where this transaction was in. null when its pending.
  * `transactionIndex`: integer of the transactions index position in the block. null when its pending.
  * `from`: 20 Bytes - address of the sender.
  * `to`: 20 Bytes - address of the receiver. null when its a contract creation transaction.
  * `value`: value transferred in Wei.
  * `gasPrice`: gas price provided by the sender in Wei.
  * `gas`: gas provided by the sender.
  * `input`: the data send along with the transaction.

### Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://polygon-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getTransactionByBlockHashAndIndex","params":["0xc0f4906fea23cf6f3cce98cb44e8e1449e455b28d684dfa9ff65426495584de6", "0x0"],"id":0}'
```


{% endtab %}
{% endtabs %}

#### Result

```json
{
  "jsonrpc": "2.0",
  "id": 0,
  "result": {
    "blockHash": "0xc0f4906fea23cf6f3cce98cb44e8e1449e455b28d684dfa9ff65426495584de6",
    "blockNumber": "0x1e8480",
    "from": "0x32be343b94f860124dc4fee278fdcbd38c102d88",
    "gas": "0x51615",
    "gasPrice": "0x6fc23ac00",
    "hash": "0xc55e2b90168af6972193c1f86fa4d7d7b31a29c156665d15b9cd48618b5177ef",
    "input": "0x",
    "nonce": "0x1efc5",
    "to": "0x104994f45d9d697ca104e5704a7b77d7fec3537c",
    "transactionIndex": "0x0",
    "value": "0x821878651a4d70000",
    "v": "0x1b",
    "r": "0x51222d91a379452395d0abaff981af4cfcc242f25cfaf947dea8245a477731f9",
    "s": "0x3a997c910b4701cca5d933fb26064ee5af7fe3236ff0ef2b58aa50b25aff8ca5"
  }
}
```



