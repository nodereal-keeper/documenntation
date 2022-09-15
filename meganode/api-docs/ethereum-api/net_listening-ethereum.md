---
description: Returns true if client is actively listening for network connections.
---

# net\_listening - Ethereum

## Parameters

none

## Returns

* `Boolean` - `true` when listening, otherwise `false`.

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://eth-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"net_listening","params":[],"id":67}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 67,
  "result": true
}
```

