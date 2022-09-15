---
description: >-
  Returns the currently configured chain id, a value used in replay-protected
  transaction signing as introduced by EIP-155.
---

# eth\_chainId - Optimism

The chain ID returned should always correspond to the information in the current known head block. This ensures that caller of this RPC method can always use the retrieved information to sign transactions built on top of the head.

### **Parameters**

None.

### **Returns**

* `QUANTITY` - big integer of the current chain id.

## **Example**

### **Request**

{% tabs %}
{% tab title="Curl" %}
```
curl https://opt-mainnet.nodereal.io/v1//your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_chainId","params":[],"id":83}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "id": 83,
  "jsonrpc": "2.0",
  "result": "0x3d" // 61
}
```

### &#x20;
