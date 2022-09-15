---
description: This API method helps you to get the token balance for ERC721/BEP721
---

# nr\_getTokenBalance721

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - The address of the ERC721/BEP721 token
* `Account Address` - Account address whose balance will be checked&#x20;
* `Block Number` - The block number in hex format or the string 'latest' or 'earliest' on which the balance will be checked

## Returns

* `Balance` - The balance of the address

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTokenBalance721","params":["0x07D971C03553011a48E951a53F48632D37652Ba1", "0x3d99cfc0839a0b2fe5ca8451cb160bdd205234f6", "0x1333EF1"],"id": 1 }'
```

**Result**

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x0000000000000000000000000000000000000000000000000000000000002a5d"
}
```

****

