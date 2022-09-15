---
description: >-
  Returns the number of uncles in a block from a block matching the given block
  number.
---

# eth\_getUncleCountByBlockNumber - Ethereum

### Parameters

`QUANTITY|TAG` - integer of a block number, or the string "latest", "earliest" or "pending", see the [default block parameter](https://eth.wiki/json-rpc/API#the-default-block-parameter).

```javascript
 params: [ 
  '0xe8', // 232 
 ]
```

### Returns

`QUANTITY` - integer of the number of uncles in this block.

### Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl  https://eth-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getUncleCountByBlockNumber","params":["0xe8"],"id":1}'
```
{% endtab %}
{% endtabs %}

#### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 0,
  "result": "0x0"
}
```
