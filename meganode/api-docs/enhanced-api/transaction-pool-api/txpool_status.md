---
description: This API method provides status info of all transactions in pool.
---

# txpool\_status

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `None`

## Returns

* **`object`** - with following fields:
  * `pending` - Total number of pending transactions in the pool, represented in hexadecimal format.
  * `queued` - Total number of queued transactions in the pool, represented in hexadecimal format.

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"txpool_status","params":[],"id":1}'
```

**Result**

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result":
    {
        "pending": "0xf8",
        "queued": "0x0"
    }
}
```
