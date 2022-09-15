---
description: Returns the current client version
---

# web3\_clientVersion - BSC

## Parameters

none

## Returns

* `String` - The current client version.

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"web3_clientVersion","params":[],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "Geth/v1.1.5-8ff7d531/linux-amd64/go1.16.4"
}
```

