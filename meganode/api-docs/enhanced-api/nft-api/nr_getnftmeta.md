---
description: >-
  This API method helps you to get the meta of an ERC1155/ERC721 token of an
  address.
---

# nr\_getNFTMeta

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Contract Address` - The address of the NFT contract
* `Token Id` - The tokenId in hex format
* `Token Type` : Please specify the type of token you query for, e.g. "ERC721", "ERC1155", etc.

## Returns

* `token_address` - The address of the token
* `token_id` - The id of the token
* `meta_url` - The url of the meta, example: https://
* `meta` - The content of the meta

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getNFTMeta","params":["0xEA5613EBBBE1E69BF5F05252C215462254F41565","0x7C7","ERC721"],"id": 1 }'
```

**Result**

```json
{
	"jsonrpc":"2.0",
	"id":1,
	"result":{
		"token_address":"0xea5613ebbbe1e69bf5f05252c215462254f41565",
		"token_id":"1991",
		"meta":"{\"name\":\"Standard Green Pepe\",\"description\":\"Standard Green Pepe with Earth\\n\\nNothing is beyond our reach\",\"category\":\"memes\",\"collection_address\":\"0xea5613ebBBE1E69Bf5F05252C215462254F41565\",\"creator\":\"0x3988c52ac9a2f9b2e591e14e173161cec6ce98ff\",\"ifps_image\":\"Qme8HFmv5aM2J1nGwxgQqU1Yt2H7e7zVHbadQxqb4Aqynq\",\"attributes\":[]}",
		"meta_url":"https://ipfs.io/ipfs/QmRzUasL1uyFjT9bbgEq5XaRjRgdUo3Q4K9qfHhEjRsy7A"
	}
}
```

****

