---
description: Returns an array of all logs matching filter with given id.
---

# eth\_getFilterLogs - BSC

{% hint style="info" %}
The response size for getFilterLogs method would be different according to your block range:

* **Block range > 50K**: Not available
* **Block range <= 100**: No response size limit
* **Block range between 100 and 50K**: Maximum 50K records would be responded
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
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getFilterLogs","params":["0xd1bdcf5b6141c7ec379531c851cb91d3"],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

See [eth\_getFilterChanges](../ethereum-api/eth\_getfilterchanges-ethereum.md)

