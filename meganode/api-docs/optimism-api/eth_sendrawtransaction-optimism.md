---
description: >-
  Creates new message call transaction or a contract creation for signed
  transactions.
---

# eth\_sendRawTransaction - Optimism

## Parameters

* `DATA`, The signed transaction data.

## Returns

*   `DATA`, 32 Bytes - the transaction hash, or the zero hash if the transaction is not yet available.

    Use [eth\_getTransactionReceipt](../ethereum-api/eth\_gettransactionreceipt-ethereum.md) to get the contract address, after the transaction was mined, when you created a contract.

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://opt-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_sendRawTransaction","params":["0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675"],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0xe670ec64341771606e55d6b4ca35a1a6b75ee3d5145a99d05921026d1527331"
}
```

