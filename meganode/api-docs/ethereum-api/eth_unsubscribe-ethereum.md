---
description: >-
  Subscriptions are cancelled with a regular RPC call with eth_unsubscribe as
  method and the subscription id as first parameter.
---

# eth\_unsubscribe - Ethereum

{% hint style="info" %}
Please not that this method is only for websockets
{% endhint %}

## Parameters

* `SUBSCRIPTION ID`&#x20;

## Returns

* `boolean`, true if the subscription was cancelled successful.

## Example

check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://eth-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_unsubscribe","params":["0x9cef478923ff08bf67fde6c64013158d"],"id":1}'
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

