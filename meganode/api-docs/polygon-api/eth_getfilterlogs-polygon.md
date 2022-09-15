---
description: Returns an array of all logs matching filter with given id.
---

# eth\_getFilterLogs - Polygon

{% hint style="info" %}
The response size for getFilterLogs method would be different according to your block range:

* **Block range >= 5000**: Not available
* **Block range < 5000**: No response size limit
{% endhint %}

## Parameters

* `QUANTITY` - The filter id.

## Returns

* See [eth\_getFilterChanges](../ethereum-api/eth\_getfilterchanges-ethereum.md)

## Example

Check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://polygon-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getFilterLogs","params":["0xd1bdcf5b6141c7ec379531c851cb91d3"],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

See [eth\_getFilterChanges](../ethereum-api/eth\_getfilterchanges-ethereum.md)

