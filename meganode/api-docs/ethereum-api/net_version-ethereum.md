---
description: Returns the current network id
---

# net\_version - Ethereum

## Parameters

none

## Returns

* `String` - The current network id.
  * 1: Ethereum Mainnet
  * 56: BSC Mainnet

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://eth-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"net_version","params":[],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "56"
}
```

