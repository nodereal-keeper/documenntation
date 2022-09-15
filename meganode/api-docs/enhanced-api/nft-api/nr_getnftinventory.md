---
description: >-
  This API method helps you to get the BEP-721/1155 token inventory of an
  address, filtered by contract address.
---

# nr\_getNFTInventory

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Contract Address` - The address of the contract
* `Account Address` - The address of the account in hex format
* `PageSize` - pageSize is hex encoded and should be less equal than 100 (each page return at most pageSize items)
* `PageKey` - It should be empty for the first page. If more results are available, a pageKey will be returned in the response. Pass the pageKey to fetch the next pageSize items.&#x20;

## Returns

* `pageKey` - string, example: 100\_342
* `details`&#x20;
  * `tokenAddress` - string, the address of the token
  * `tokenId` - string, the id of the token
  * `balance` - string, the balance of the token

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getNFTInventory","params":["0x0042f9b78c67eb30c020a56d07f9a2fc83bc2514","0x64aF96778bA83b7d4509123146E2B3b07F7deF52","0x14",""],"id": 1 }'
```

**Result**

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": {
    "pageKey": "100_342",
    "details": [
      {
        "tokenAddress": "0x5e74094cd416f55179dbd0e45b1a8ed030e396a1",
        "tokenId": "0x0000000000000000000000000000000000000000f",
        "balance": "0x00000000000000000000000000000000000000001"
      }
    ]
  }
}
```

****

