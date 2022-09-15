---
description: This API method helps you to get token's total supply for ERC20 & BEP20
---

# nr\_getTotalSupply20

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `address` - the contract address
* `blockNumber` - the block number

## Returns

* `totalSupply` - the total supply of the token

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTotalSupply20","params":["0x8AC76a51cc950d9822D68b83fE1Ad97B32Cd580d", "latest"],"id": 1 }'
```

**Result**

```
{
	"jsonrpc":"2.0",
	"id":1,
	"result":"0x0000000000000000000000000000000000000000061245ba1ae22428223e59d4"
}   
```
