---
description: >-
  This API method helps you to get the number of token ids of an NFT(721/1155)
  token.
---

# nr\_getNFTTokenCount

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - Address of the token&#x20;

## Returns

* `TokenCount` - a hex encoded number of tokens

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getNFTTokenCount","params":["0x07d971c03553011a48e951a53f48632d37652ba1"],"id": 1 }'
```

**Result**

```
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": "0x123"
}
```
