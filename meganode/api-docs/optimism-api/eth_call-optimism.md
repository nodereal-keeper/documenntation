---
description: >-
  Executes a new message call immediately without creating a transaction on the
  block chain.
---

# eth\_call - Optimism

This is one of the most commonly used API calls. It is used to read from the blockchain which includes executing smart contracts, but does not publish anything to the blockchain. This call does not consume any Ether.

{% hint style="warning" %}
To prevent abusive of the API, the `gas` parameter to `eth_estimateGas` and `eth_call` are capped at 10x (1000%) the current block gas limit. You can recreate this behavior in your local test environment (ganache, besu, geth, or other client) via the `rpc.gascap` command-line option.
{% endhint %}

## Parameters

* `TRANSACTION CALL OBJECT` _\[required]_
  * `from`: 20 Bytes - the address the transaction is sent from.
  * `to`: 20 Bytes - the address the transaction is directed to.
  * `gas`: _\[optional]_ Integer of the gas provided for the transaction execution. eth\_call consumes zero gas, but this parameter may be needed by some executions.
  * `gasPrice`: _\[optional]_ Integer of the gasPrice used for each paid gas
  * `value`: _\[optional]_ Integer of the value sent with this transaction
  * `data`: _\[optional]_ Hash of the method signature and encoded parameters. For details see Ethereum Contract ABI
* `BLOCK PARAMETER` _\[required]_ - an integer block number, or the string "latest", "earliest" or "pending",&#x20;



## Returns

* `RETURN VALUE` - the return value of the executed contract method.

## Example

Check out the example below:

### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://opt-mainnet.nodereal.io/v1/your-api-key \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_call","params": [{"from": "0xb60e8dd61c5d32be8058bb8eb970870f07233155","to": "0xd46e8dd67c5d32be8058bb8eb970870f07244567","gas": "0x76c0","gasPrice": "0x9184e72a000","value": "0x9184e72a","data": "0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675"}, "latest"],"id":1}'
```
{% endtab %}
{% endtabs %}

### Result

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x"
}
```

