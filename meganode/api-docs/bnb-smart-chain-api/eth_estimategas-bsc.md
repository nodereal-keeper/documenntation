---
description: >-
  Generates and returns an estimate of how much gas is necessary to allow the
  transaction to complete. The transaction will not be added to the blockchain.
---

# eth\_estimateGas - BSC

## Parameters

* `TRANSACTION CALL OBJECT` _\[required]_
  * `from`: _\[optional]_ 20 Bytes - The address the transaction is sent from.
  * `to`: 20 Bytes - The address the transaction is directed to.
  * `gas`: _\[optional]_ Integer of the gas provided for the transaction execution. eth\_estimateGas consumes zero gas, but this parameter may be needed by some executions.
  * `gasPrice`: _\[optional]_ Integer of the gasPrice used for each paid gas
  * `value`: _\[optional]_ Integer of the value sent with this transaction
  * `data`: _\[optional]_ Hash of the method signature and encoded parameters. For details see Ethereum Contract ABI

### Returns

`QUANTITY` - the amount of gas used.

## **Example**

### **Request**

{% tabs %}
{% tab title="Curl" %}
```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_estimateGas","params":[{see above}],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```javascript
{
  "id":1,
  "jsonrpc": "2.0",
  "result": "0x5208" // 21000
}
```
