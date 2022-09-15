---
description: This API method helps you to get the total supply for ERC721/BEP721
---

# nr\_getTotalSupply721

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - The address of the ERC721/BEP721 token
* `block Number` - The block number in hex format or the string 'latest' or 'earliest' on which the total supply will be checked

## Returns

* `TotalSupply` - the total supply of the token, 32-byte fixed-length hexadecimal number

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTotalSupply721","params":["0x8AC76a51cc950d9822D68b83fE1Ad97B32Cd580d", "0x895440"],"id": 0 }'
```

**Result**

```
{
  "id": "0",
  "jsonrpc": "2.0",
  "result": "0x000000000000000000000000000000000000000005bf8de73e1a17553e3e59d4"
}
```
