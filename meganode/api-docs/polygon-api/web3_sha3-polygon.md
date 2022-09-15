---
description: Returns Keccak-256 (not the standardized SHA3-256) of the given data
---

# web3\_sha3 - Polygon

## Parameters

* `DATA` - the data to convert into a SHA3 hash.

## Returns

* `DATA` - The SHA3 result of the given string.

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://polygon-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"web3_sha3","params":["0x68656c6c6f20776f726c64"],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x47173285a8d7341e5e972fc677286384f802f8ef42a5ec5f03bbfa254cb01fad"
}
```

