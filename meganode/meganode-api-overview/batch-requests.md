---
description: >-
  You can send multiple requests within one batch call in MegaNode. This
  document explains how to send it and its limitation.
---

# Batch Requests

## What is "Batch Requests"?

In some practices, you need to send multiple API calls to get what you needed. You can either send  API requests multiple times, or simply send multiple API calls nested in a single HTTP request. The latter is "Batch Requests"

However, we does not recommend using batch requests since the nature of batch requests may not have same reliability as single requests, especially when you have too many requests in a single call.

## **Who is allowed to send batch requests?**

All the MegaNode users, regardless of your pricing plan, are allowed to send batch requests.

## Batch requests limitation

You can send batch requests only if the API calls nested within it are no more than 500 requests. Also, you can't send debug API requests as part of your batch request.&#x20;

## **How do batch requests cost?**

The cost of batch requests is according to the API calls nested within it. For example, if you send a batch request and there're 4 _eth\_blockNumber_ calls inside, it costs total CUs in total.

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '[{"jsonrpc": "2.0", "id": 1, "method": "eth_blockNumber", "params": []},
{"jsonrpc": "2.0", "id": 2, "method": "eth_blockNumber", "params": []},
{"jsonrpc": "2.0", "id": 3, "method": "eth_blockNumber", "params": []},
{"jsonrpc": "2.0", "id": 4, "method": "eth_blockNumber", "params": []}]'
```

**Result**

```
[{"jsonrpc":"2.0","id":1,"result":"0x12eed11"},{"jsonrpc":"2.0","id":2,"result":"0x12eed11"},{"jsonrpc":"2.0","id":3,"result":"0x12eed11"},{"jsonrpc":"2.0","id":4,"result":"0x12eed11"}]
```

