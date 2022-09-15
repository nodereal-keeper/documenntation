---
description: Returns an object with data about the sync status or false
---

# eth\_syncing - Optimism

## Parameters

none

## Returns

* `Object|Boolean`, An object with sync status data or `FALSE`, when not syncing:
  * `startingBlock`: `QUANTITY` - The block at which the import started (will only be reset, after the sync reached his head)
  * `currentBlock`: `QUANTITY` - The current block, same as eth\_blockNumber
  * `highestBlock`: `QUANTITY` - The estimated highest block

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://opt-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_syncing","params":[],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": {
    startingBlock: '0x384',
    currentBlock: '0x386',
    highestBlock: '0x454'
  }
}
```

