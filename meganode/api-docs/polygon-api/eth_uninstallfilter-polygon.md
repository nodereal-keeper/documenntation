---
description: >-
  Uninstalls a filter with given id. Should always be called when watch is no
  longer needed. Additonally Filters timeout when they aren't requested with
  eth_getFilterChanges for a period of time.
---

# eth\_uninstallFilter - Polygon

## Parameters

* `QUANTITY` - The filter id.

## Returns

* `Boolean` - `true` if the filter was successfully uninstalled, otherwise `false`.

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://polygon-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_uninstallFilter","params":["0xb"],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": true
}
```

