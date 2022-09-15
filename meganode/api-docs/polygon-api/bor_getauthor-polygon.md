---
description: Returns address of Author
---

# bor\_getAuthor - Polygon

## Parameters

* `blockNumber` - The block number in hex

{% hint style="info" %}
Please note the blockNumber should be in the HEX string format. e.g. 0x11a6c2c
{% endhint %}

```
"params": [
      "0x11a6c2c",
  ]
```

## Returns

* `author` - address

## Example

**Request**

```
curl https://polygon-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"bor_getAuthor","params":["0x11a6c2c"],"id": 0 }'
```

**Result**

```
{
    "jsonrpc": "2.0",
    "id": 0,
    "result": "0x5973918275c01f50555d44e92c9d9b353cadad54"
}
```
