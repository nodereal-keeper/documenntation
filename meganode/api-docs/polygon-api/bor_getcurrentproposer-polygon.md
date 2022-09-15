---
description: Returns current proposer's address
---

# bor\_getCurrentProposer - Polygon

## Parameters

none

## Returns

`author` - address

## Example

**Request**

```
curl https://polygon-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"bor_getCurrentProposer","params":[], "id":1}'
```

**Result**

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": "0xec20607aa654d823dd01beb8780a44863c57ed07"
}
```
