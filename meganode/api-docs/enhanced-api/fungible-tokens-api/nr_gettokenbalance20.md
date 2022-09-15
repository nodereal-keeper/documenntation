---
description: This API method helps you to get the token balance for ERC20/BEP20
---

# nr\_getTokenBalance20

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `contractAddress` - The address of the contract
* `address` - Target address
* `blockNumber` - The block number in hex format

## Returns

* `balance` - The balance of the address

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTokenBalance20","params":["0xe9e7CEA3DedcA5984780Bafc599bD69ADd087D56", "0x8894e0a0c962cb723c1976a4421c95949be2d4e3", "0x1312D00"],"id": 0 }'
```

**Result**

```
{
  "jsonrpc": "2.0",
  "id": 0,
  "result": "0x000000000000000000000000000000000000000002e04bb41ca9ed87e4b22cb6"
}
```

