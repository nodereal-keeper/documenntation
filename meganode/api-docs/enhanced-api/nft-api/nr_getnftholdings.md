---
description: >-
  This API method helps you to get the BEP-721/1155 tokens and the amount held
  by an address.
---

# nr\_getNFTHoldings

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Account Address` - The address of the account in hex format
* `Token Type` : (optional) Please specify the type of token you query for, e.g. "ERC721", "ERC1155", etc.
* `Page` : page number in hex format
* `PageSize` - pageSize is hex encoded and should be less equal than 100 (each page return at most pageSize items)

## Returns

* `totalCount` - string, number in hex format
* `details`&#x20;
  * `tokenAddress` - string, the address of the token
  * `tokenName` - string, the name of the token
  * `tokenSymbol` - string, the symbol of the token
  * `tokenIdNum` - string, the id number of the token

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getNFTHoldings","params":["0x99817ce62abf5b17f58e71071e590cf958e5a1bf","erc721","0x1","0x14"],"id": 1 }'
```

**Result**

```json
{
	"jsonrpc":"2.0",
	"id":1,
	"result":{
		"totalCount":"0x1",
		"details":[
			{
				"tokenAddress":"0x5e74094cd416f55179dbd0e45b1a8ed030e396a1",
				"tokenIdNum":"0x12",
				"tokenName":"Pancake Lottery Ticket",
				"tokenSymbol":"PLT"
			},
			{
				"tokenAddress":"0xdf7952b35f24acf7fc0487d01c8d5690a60dba07",
				"tokenIdNum":"0x1",
				"tokenName":"Pancake Bunnies",
				"tokenSymbol":"PB"
			}
		]
	}
}         
```

****

