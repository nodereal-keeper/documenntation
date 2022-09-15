---
description: >-
  This API method provides summary of all transactions in pool, including
  'pending' and 'queued' transactions. Summary consists of address "to" if any,
  transaction value, gas and gasPrice.
---

# txpool\_inspect

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `None`

## Returns

* **`array`** - list of pending and queued transactions, with each having the following fields:
  * `pending` - Array of transaction objects, with textual data.
  * `queued` - Array of transaction objects, with textual data.

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"txpool_inspect","params":[],"id":1}'
```

**Result**

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result":
    {
        "pending":
        {
            "0x0060526a6f7c25892a65d2c0c06255be9ce8ef19":
            {
                "10": "0x10ED43C718714eb63d5aA57B78B54704E256024E: 0 wei + 234643 gas × 5000000000 wei"
            }
        },
        "queued":
        {
            "0x0000f2fe18a43f5aa6028e2a0c134e979cabeb27":
            {
                "1808": "0x0000000000008AfdAcc486225455281F614843e7: 12 wei + 315138 gas × 5500000000 wei"
            }
        }
    }
}
```
