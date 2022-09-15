---
description: >-
  This API method helps you to get the current token holders and number of
  tokens held.
---

# nr\_getTokenHolders

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Contract Address` - the address of the contract
* `PageSize` - pageSize is hex encoded and should be less equal than 100 (each page return at most pageSize items)
* `PageKey` - It should be empty for the first page. If more results are available, a pageKey will be returned in the response. Pass the pageKey to fetch the next pageSize items.&#x20;
* `topN` -  (optional) hex encoded string; if use the topN parameter, it will return at most N records and results will be returned by balance order.&#x20;

## Returns

* `accountAddress` - the address of the account
* `tokenBalance` - the balance of the token

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTokenHolders","params":["0xcea59dce6a6d73a24e6d6944cfabc330814c098a", "0x14",""],"id": 1 }'
```

**Result**

```
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": {
    "pageKey": "100_342",
    "details": [
      {
        "accountAddress": "0x00000000100f9d75535cbf23f82e23db5558e8c1",
        "tokenBalance": "0x0000000000000000000000000000000000000000f"
      }
    ]
  }
}
```
