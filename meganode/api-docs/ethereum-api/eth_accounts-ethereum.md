---
description: Returns a list of addresses owned by client
---

# eth\_accounts - Ethereum

## Parameters

none

## Returns

`Array of DATA`, 20 Bytes - addresses owned by the client.

## Example

Check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://eth-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_accounts","params":[],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0xc94770007dda54cF92009BFF0dE90c06F603a09f"
}
```

