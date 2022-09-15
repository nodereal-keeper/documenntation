---
description: >-
  This API method helps you to get the holders' info of the NFT token for
  ERC1155/ERC721.
---

# nr\_getNFTCollectionHolders

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Contract Address` - The address of the contract
* `Token Type` : Please specify the type of token you query for, e.g. "ERC721", "ERC1155", etc.
* `PageSize` - pageSize is hex encoded and should be less equal than 100 (each page return at most pageSize items)
* `PageKey` - It should be empty for the first page. If more results are available, a pageKey will be returned in the response. Pass the pageKey to fetch the next pageSize items.&#x20;
* `withBalance` - Optional. Must be a bool value.--- decides whether Balance information is returned

## Returns

* `pageKey` - string, example: 100\_342
* `holderAddresses` - returns when the withBalance parameter is false
* `holderAddressWithBalances`- returns when the withBalance parameter is true
  * `holderAddress` - The address of the owner
  * `tokenBalances`
    * `tokenId` - The token's id
    * `Balance` - The balance for the token

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getNFTCollectionHolders","params":["0xC244E2A5c6bbC89cfda2c32Ae0086052c95c3B55","ERC1155","0x14","",true],"id": 1 }'
```

**Result**

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": {
    "pageKey": "100_342",
    "holderAddressesWithBalances": [
      {
        "holderAddress": "0x000001f568875f378bf6d170b790967fe429c81a",
        "tokenBalances": {
          "tokenId": "9446",
          "balance": "1"
        }
      }
    ]
  }
}
```

****

