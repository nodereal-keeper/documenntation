---
description: >-
  This API replays all transactions that were included in this block by block
  hash
---

# debug\_traceBlockByHash

{% hint style="info" %}
Supported on BSC, Ethereum, and Optimism mainnet only.
{% endhint %}

## Parameters

* `blockHash`_\[REQUIRED]_ - The block hash
* `tracer` _\[REQUIRED]_ - The tracer type. Please refer to Geth implementation for more tracer type.

```
"params": [
  "0xcb1e9e529fddcfdad8c4d43eabf8264d55d13305105cf760dfdae166ddc42046",
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



## Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"debug_traceBlockByHash","params":["0xcb1e9e529fddcfdad8c4d43eabf8264d55d13305105cf760dfdae166ddc42046", {"tracer": "callTracer"}],"id": 0 }'
```
{% endtab %}
{% endtabs %}

#### "Result

```javascript
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": [
        {
            "result": {
                "from": "0x4982085c9e2f89f2ecb8131eca71afad896e89cb",
                "to": "0xce56d6ff4f9c8dbcacc5f848ca8c60ba5469ae70",
                "value": "0x11c37937e08000",
                "gas": "0x7148",
                "gasUsed": "0x0",
                "input": "0x",
                "output": "0x",
                "type": "CALL"
            }
        },
        {
            "result": {
                "gas": "0x7f3a",
                "gasUsed": "0x3887",
                "input": "0xa9059cbb0000000000000000000000004982085c9e2f89f2ecb8131eca71afad896e89cb0000000000000000000000000000000000000000000000621eca0233750fb400",
                "output": "0x0000000000000000000000000000000000000000000000000000000000000001",
                "type": "CALL",
                "from": "0x66a1777e55b416c56ad8f2a4bfeef9c2695328b9",
                "to": "0xe9e7cea3dedca5984780bafc599bd69add087d56",
                "value": "0x0"
            }
        },
        {
            "result": {
                "input": "0xa9059cbb0000000000000000000000004982085c9e2f89f2ecb8131eca71afad896e89cb00000000000000000000000000000000000000000000017b76b5e61969930000",
                "output": "0x0000000000000000000000000000000000000000000000000000000000000001",
                "type": "CALL",
                "from": "0x37ef12b84c3dfe061ef10e8a8369054c850fd54e",
                "to": "0x4b0f1812e5df2a09796481ff14017e6005508003",
                "value": "0x0",
                "gas": "0x8096",
                "gasUsed": "0x397b"
            }
        },
        {
            "result": {
                "type": "CALL",
                "from": "0xf4509b01b19de2073f1d9547bdd3925fd4487dda",
                "to": "0xaafa10755b3b1dbf46e86d973c3f27f3671ed9db",
                "value": "0x0",
                "gas": "0x9360",
                "gasUsed": "0x393c",
                "input": "0xa9059cbb000000000000000000000000779c7a9f92ada6f94bb46b60de1db936097b91b50000000000000000000000000000000000000000000000000000000005f5e10000307832313338333362353265313233633033313133453436334435434242316345393935373632383344",
                "output": "0x0000000000000000000000000000000000000000000000000000000000000001"
            }
        },
        {
            "result": {
                "to": "0x488b347b20bfd1b193a6af688fa391706bad2930",
                "value": "0x0",
                "gas": "0x74bf8",
                "gasUsed": "0x996b",
                "input": "0x6e071f17000000000000000000000000fd754dd044fd6dc54157776ac7faed2cab332ef7000000000000000000000000e5e0da392decb0b13ee54fc68d20ad064540e473",
                "output": "0x",
                "type": "CALL",
                "from": "0xe88f37ddad5eb73c3f899659796986b8e53821de"
            }
        },
        {
            "result": {
                "from": "0x0d0707963952f2fba59dd06f2b425ace40b492fe",
                "to": "0x16153214e683018d5aa318864c8e692b66e16778",
                "value": "0x0",
                "gas": "0xeed9c",
                "gasUsed": "0x7411",
                "input": "0xa9059cbb000000000000000000000000ec507ac1e7d4069618da43a0135ce8bcaa47a364000000000000000000000000000000000000000000000a04865a8391376c8000",
                "output": "0x0000000000000000000000000000000000000000000000000000000000000001",
                "type": "CALL"
            }
        },
        ...
    ]
}
```

