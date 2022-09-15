---
description: This API method helps you to get the token's total supply for ERC1155/BEP1155
---

# nr\_getTotalSupply1155

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - The address of the ERC1155/BEP1155 token
* `block Number` - The block number in hex format or the string 'latest' or 'earliest' on which the total supply will be checked
* `Token Id` - The tokenId in hex format

## Returns

* `TotalSupply` - the total supply of the token, 32-byte fixed-length hexadecimal number

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTotalSupply1155","params":["0xBe23dD3c644DB84d32eA91d6121A55b8B3Eea6F1","0x1333EF1","0x80"],"id": 1 }'
```

**Result**

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x0000000000000000000000000000000000000000000000000000000000000001"
}
```

****

