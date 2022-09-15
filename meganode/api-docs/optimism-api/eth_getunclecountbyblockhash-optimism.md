---
description: >-
  Returns the number of uncles in a block from a block matching the given block
  hash.
---

# eth\_getUncleCountByBlockHash - Optimism

### Parameters

* `DATA`, 32 Bytes - hash of a block.

```javascript
params: [
 '0xb3b20624f8f0f86eb50dd04688409e5cea4bd02d700bf6e79e9384d47d6a5a35'
]
```

### Returns

`QUANTITY` - integer of the number of uncles in this block.

### Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl  https://opt-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getUncleCountByBlockHash","params":["0xb3b20624f8f0f86eb50dd04688409e5cea4bd02d700bf6e79e9384d47d6a5a35"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 0,
  "result": "0x1"
}
```
