---
description: Returns the root hash given a block range
---

# bor\_getRootHash - Polygon

## Parameters

* `from` - block number (integer format)
* `to` - block number (integer format)

```
"params": [
      1000000,
      1032767
  ]
```

## Returns

* hash - the root hash

## Example

**Request**

```
curl https://polygon-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"bor_getRootHash","params":[1000000, 1032767], "id":1}'
```

**Result**

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": "04b073e17b7186ab4daae17c5e2cc2d5a729cffd102cede41ee458a2d5573994"
}
```
