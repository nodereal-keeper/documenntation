---
description: >-
  Creates a filter in the node, to notify when a new block arrives. To check if
  the state has changed, call eth_getFilterChanges.
---

# eth\_newBlockFilter - Optimism

## Parameters

none

## Returns

* `QUANTITY` - A filter id.

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://opt-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_newBlockFilter","params":[],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0xd1bdcf5b6141c7ec379531c851cb91d3"
}
```

