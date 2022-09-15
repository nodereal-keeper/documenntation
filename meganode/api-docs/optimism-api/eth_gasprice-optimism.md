---
description: Returns the current price per gas in wei.
---

# eth\_gasPrice - Optimism

### Parameters

none

### Returns

`QUANTITY` - integer of the current gas price in wei.

### **Example**

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl https://opt-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_gasPrice","params":[],"id":0}'
```
{% endtab %}
{% endtabs %}

#### Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 0,
  "result": "0x12a05f200"
}
```
