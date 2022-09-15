---
description: >-
  Creates a filter object, based on filter options, to notify when the state
  changes (logs). To check if the state has changed, call eth_getFilterChanges.
---

# eth\_newFilter - Ethereum

## Parameters

1. `Object` - The filter options:

* `fromBlock`: `QUANTITY|TAG` - (optional, default: `"latest"`) Integer block number, or `"latest"` for the last mined block or `"pending"`, `"earliest"` for not yet mined transactions.
* `toBlock`: `QUANTITY|TAG` - (optional, default: `"latest"`) Integer block number, or `"latest"` for the last mined block or `"pending"`, `"earliest"` for not yet mined transactions.
* `address`: `DATA|Array`, 20 Bytes - (optional) Contract address or a list of addresses from which logs should originate.
* `topics`: `Array of DATA`, - (optional) Array of 32 Bytes `DATA` topics. Topics are order-dependent. Each topic can also be an array of DATA with "or" options.

## Returns

* `QUANTITY` - A filter id.

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://eth-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_newFilter","params":[{"topics":["0x0000000000000000000000000000000000000000000000000000000012341234"]}],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x7185030cb5dabae60f32b996a4ab04a3"
}
```

