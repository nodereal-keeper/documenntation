---
description: >-
  This API lets you run an eth_call within the context of the given block
  execution using the final state of parent block as the base.
---

# debug\_traceCall

{% hint style="info" %}
Supported on BSC, Ethereum, and Optimism mainnet only.
{% endhint %}

## Parameters

* `object`_\[OPTIONAL]_ - The transaction call object
  * `from` - The address the transaction is sent from
  * `to` - The address the transaction is directed to
  * `gas` - The gas provided for the transaction execution
  * `gasPrice` - The gas price
  * `data` - The data sent along with the transaction
  * `value` - The value transferred in Wei, encoded as a hexadecimal
* `blockNumber`_\[REQUIRED] -_ The block number, hex format
* `tracer` _\[REQUIRED]_ - The tracer type

```
"params": [
  "0x1233174",
  {
    "tracer": "callTracer"
  }
```

## Returns

This returns based on callTracer. Please refer to Geth implementation for more return data fields.

`Object` - Full trace of the block.

* `result`- Trace Object, which has the following fields:
  * `from` - The address the transaction is sent from
  * `to` - The address the transaction is directed to
  * `gas` - The gas provided for the transaction execution
  * `gasUsed` - The gasPrice used for each paid gas
  * `input` - The data sent along with the transaction
  * `output` - The output data
  * `type` - Type of the transaction
  * `value` - The value transferred in Wei, encoded as a hexadecimal

## Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"debug_traceCall","params": [{"from": "0x4982085c9e2f89f2ecb8131eca71afad896e89cb","to": "0xce56d6ff4f9c8dbcacc5f848ca8c60ba5469ae70","gas": "0x7148","value": "0x11c37937e08000"},"latest",{"tracer": "callTracer"}],"id": 0 }'
```
{% endtab %}
{% endtabs %}

#### "Result

```javascript
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "type": "CALL",
        "from": "0x4982085c9e2f89f2ecb8131eca71afad896e89cb",
        "to": "0xce56d6ff4f9c8dbcacc5f848ca8c60ba5469ae70",
        "value": "0x11c37937e08000",
        "gas": "0x1f40",
        "gasUsed": "0x0",
        "input": "0x",
        "output": "0x"
    }
}
```

