---
description: This API method helps you to get specific token's metadata.
---

# nr\_getTokenMeta

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - Address of the token&#x20;

## Returns

* `result`
  * `name` - the readable name of the token
  * `symbol` - the abbreviation
  * `decimals` - used in frontends to show the proper significant digits of a token
  * `tokenType` - the technical standard of the token

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTokenMeta","params":["0x8AC76a51cc950d9822D68b83fE1Ad97B32Cd580d"],"id": 0 }'
```

**Result**

```
{
  "id": "0",
  "jsonrpc": "2.0",
  "result": {
    "name": "USD Coin",
    "symbol": "USDC",
    "decimails": 18,
    "tokenType": "erc20"
  }
}
```
