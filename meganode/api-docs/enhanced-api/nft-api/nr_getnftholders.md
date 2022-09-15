---
description: This API method helps you to get the owners for a BEP-721/1155 tokenId.
---

# nr\_getNFTHolders

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Contract Address` - The address of the contract
* `Token Id` - The tokenId in hex format of the BEP-721/1155 token
* `topN` -  (optional) hex encoded string; if use the topN parameter, it will return at most N records and results will be returned by balance order.&#x20;

## Returns

* `List` - a string representing the addresses of the owners

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getNFTHolders","params":["0x64aF96778bA83b7d4509123146E2B3b07F7deF52","0x5000004"],"id": 1 }'
```

**Result**

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": [
    "0x99817ce62abf5b17f58e71071e590cf958e5a1bf",
    "0x5e74094cd416f55179dbd0e45b1a8ed030e396a1"
  ]
}
```

****

