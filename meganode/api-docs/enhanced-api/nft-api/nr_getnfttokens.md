---
description: >-
  This API method helps you to get the list of NFT token ids and according
  totalSupply of an NFT(721/1155) token.
---

# nr\_getNFTTokens

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - The address of the token
* `Token Type` : Please specify the type of token you query for, e.g. "ERC721", "ERC1155", etc.
* `PageSize` - pageSize is hex encoded and should be less equal than 100 (each page return at most pageSize items)
* `PageKey` - It should be empty for the first page. If more results are available, a pageKey will be returned in the response. Pass the pageKey to fetch the next pageSize items.&#x20;

## Returns

* `token_id` - The list of tokenid
* `totalSupply` - the hex decoded total supply

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getNFTTokens","params":["0x07d971c03553011a48e951a53f48632d37652ba1","ERC721","0x14",""],"id": 1 }'
```

**Result**

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": [
    {
      "tokenId": "0x123",
      "totalSupply": "0x123"
    }
  ]
}
```

****

