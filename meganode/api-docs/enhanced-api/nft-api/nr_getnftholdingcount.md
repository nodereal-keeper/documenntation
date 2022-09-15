---
description: >-
  This API method helps you to get the number of NFT(721/1155) token holdings of
  an account.
---

# nr\_getNFTHoldingCount

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Account Address` - The address of the account in hex format

## Returns

* `count721` - string, number of NFT(721) token holdings
* `count1155` - string, number of NFT(1155) token holdings

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getNFTHoldingCount","params":["0x21d45650db732cE5dF77685d6021d7D5d1da807f"],"id": 1 }'
```

**Result**

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": {
    "count721": "0x2",
    "count1155": "0x0"
  }
}      
```

****

