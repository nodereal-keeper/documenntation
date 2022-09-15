---
description: >-
  This API method helps you to get the number of token holders of an ERC20
  token.
---

# nr\_getTokenHolderCount

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - the address of the token

## Returns

* `count` - the hex-encoded number of token holders

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTokenHolderCount","params":["0x2170ed0880ac9a755fd29b2688956bd959f933f8"],"id": 1 }'
```

**Result**

```
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": "0x123"
}
```
