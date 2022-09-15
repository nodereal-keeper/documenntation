---
description: This API method helps you to get the token balance for ERC1155/BEP1155
---

# nr\_getTokenBalance1155

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - The address of the ERC1155/BEP1155 token
* `Account Address` - Account address whose balance will be checked&#x20;
* `Block Number` - The block number in hex format or the string 'latest' or 'earliest' on which the balance will be checked
* `Token Id` - The tokenId in hex format of the ERC1155/BEP1155 token

## Returns

* `Balance` - The balance of the address

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTokenBalance1155","params":["0x98387108842a7CfC7bA23E080030351f6ea68ac0", "0x38767ebadf9b4f9302c5cb88be9a3426234bc9a5", "0x1333EF1", "0x1"],"id": 1 }'
```

**Result**

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x000000000000000000000000000000000000000000000000000000000000006c"
}
```

****

