---
description: Returns the number of transactions in the block with the given block hash.
---

# eth\_getBlockTransactionCountByHash - Optimism

### Parameters

`DATA`, 32 Bytes - hash of a transaction

```javascript
params: [
    "0x88df016429689c079f3b2f6ad39fa052532c56795b733da78a91ebe6a713944b"
]
```

### Returns

* `BLOCK TRANSACTION COUNT` - a hex code of the integer representing the number of transactions in the provided block

### Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl https://opt-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getBlockTransactionCountByHash","params":["0x8243343df08b9751f5ca0c5f8c9c0460d8a9b6351066fae0acbd4d3e776de8bb"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x50"
}
```
