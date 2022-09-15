---
description: Returns the current "latest" block number.
---

# eth\_blockNumber - Optimism

## Parameters

none

## Returns

* `BLOCK NUMBER` : a hex code of an integer representing the current block number the client is on.

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://opt-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":0}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 0,
  "result": "0x65a8db"
}
```

