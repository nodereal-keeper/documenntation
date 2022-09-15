---
description: >-
  This API method helps you to get the BEP20 tokens and amount held by an
  account.
---

# nr\_getTokenHoldings

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Account Address` - the address of the account
* `Page` - the page number in hex format
* `PageSize` - pageSize is hex encoded and should be less equal than 100 (each page return at most pageSize items)

## Returns

* `tokenAddress` - the address of the token
* `tokenName` - the name of the token
* `tokenSymbol` - the symbol of the token
* `tokenDecimails` - the decimals of the token
* `tokenBalance` - the balance of the token

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTokenHoldings","params":["0x0E34aD56379aceC7F09d815729B70c85adC1Ec99", "0x1","0x12"],"id": 1 }'
```

**Result**

```
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": {
    "totalCount": "0x34",
    "details": [
      {
        "tokenAddress": "0xfcb5DF42e06A39E233dc707bb3a80311eFD11576",
        "tokenName": "www.METH.co.in",
        "tokenSymbol": "METH",
        "tokenDecimails": "0x12",
        "tokenBalance": "0x0000000000000000000000000000000000000000f"
      }
    ]
  }
}
```
