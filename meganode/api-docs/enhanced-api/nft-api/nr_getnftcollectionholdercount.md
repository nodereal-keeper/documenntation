---
description: >-
  This API method helps you to get the number of NFT(721/1155) collection
  holders of an NFT(721/1155) token.
---

# nr\_getNFTCollectionHolderCount

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - The address of the token
* `Token Type` : Please specify the type of token you query for, e.g. "ERC721", "ERC1155", etc.

## Returns

* `Count` - the number of NFT(721/1155) collection holders of the given token

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getNFTCollectionHolderCount","params":["0x07D971C03553011a48E951a53F48632D37652Ba1","ERC721"],"id": 1 }'
```

**Result**

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": "0x4E5"
}
```

****

