---
description: >-
  This API method helps you to get the number of ERC20 token holdings of an
  account.
---

# nr\_getTokenHoldingCount

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Account Address` - the address of the account

## Returns

* `count` - the hex-encoded number of ERC20 token holdings of the given account

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTokenHoldingCount","params":["0x35BA0C8AB94F09772A074374647E04F7B939F458"],"id": 1 }'
```

**Result**

```
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": "0x4E5"
}
```
