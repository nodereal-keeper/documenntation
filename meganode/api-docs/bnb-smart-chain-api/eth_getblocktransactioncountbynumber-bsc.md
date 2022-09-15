---
description: Returns the number of transactions in the block with the given block number.
---

# eth\_getBlockTransactionCountByNumber - BSC

### Parameters

* `BLOCK PARAMETER` _\[required]_ - an integer block number, or the string "latest", "earliest" or "pending", see the [default block parameter](https://github.com/ethereum/wiki/wiki/JSON-RPC#the-default-block-parameter)

### Returns

* `BLOCK TRANSACTION COUNT` - a hex code of the integer representing the number of transactions in the provided block

### Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getBlockTransactionCountByNumber","params":["latest"],"id":0}'
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
