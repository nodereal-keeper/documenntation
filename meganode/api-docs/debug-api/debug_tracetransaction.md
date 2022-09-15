---
description: >-
  This API would replay any transaction that may have been executed prior to
  this one before it will finally attempt to execute the transaction that
  corresponds to the given hash.
---

# debug\_traceTransaction

{% hint style="info" %}
Supported on BSC, Ethereum, and Optimism mainnet only.
{% endhint %}

## Parameters

* `transactionHash`_\[REQUIRED]_ - The hash of transaction
* `tracer` _\[REQUIRED]_ - The tracer type

```
"params": [
  "0x34bd3463c504e6188a8549a70973bfdb944a42a16e4ee44cb1467e7843753174",
  {
    "tracer": "callTracer"
  }
]
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
  * `calls` - The transaction calls

## Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"debug_traceTransaction","params": ["0x34bd3463c504e6188a8549a70973bfdb944a42a16e4ee44cb1467e7843753174",{"tracer": "callTracer"}],"id": 0 }'
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
        "gas": "0x45844",
        "output": "0x08c379a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000016100000000000000000000000000000000000000000000000000000000000000",
        "calls": [
            {
                "input": "0x0902f1ac",
                "output": "0x000000000000000000000000000000000000000000011c6a552be13a04d16ed400000000000000000000000000000000000000000000003a5bf56e902f799fe60000000000000000000000000000000000000000000000000000000062bb0828",
                "type": "STATICCALL",
                "from": "0x602af6edcfdd2c23589b9ef1c39f89bc87e01f35",
                "to": "0x524ebbfdbf8ac97bea24f6a142104e5dfaddf49d",
                "gas": "0x42d45",
                "gasUsed": "0xbb1"
            }
        ],
        "from": "0x979d9dd23d71a414eb6aad8b5543f42348315093",
        "to": "0x602af6edcfdd2c23589b9ef1c39f89bc87e01f35",
        "value": "0x0",
        "gasUsed": "0x29d7",
        "input": "0x9aad44180000000000000000000000000000000000000000000000d3b296481b75e684b7000000000000000000000000000000000000000000000000306b30a884951fc8000000000000000000000000d983780da5383bcdb57d12562e5fe8a6171140e50000000000000000000000042dff8be2ba0c3b4ae3e086305ad3fac5bd456bf9000000000000000000000000000000000000000000011cc7164c4a8d138629cf000000000ec9c05600000000000000000000000062bb08240000000000000000000000054ca0850f80fd1cbe2fd15d42ab068a9478419f8500",
        "error": "execution reverted"
    }
}
```



