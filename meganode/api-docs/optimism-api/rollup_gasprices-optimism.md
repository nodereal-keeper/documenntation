---
description: >-
  Returns the L1 and L2 gas prices that are being used by the Sequencer to
  calculate fees.
---

# rollup\_gasPrices - Optimism

## **Parameters**

None

## **Returns**

`Object`

* `l1GasPrice`: `QUANTITY` - L1 gas price in wei that the Sequencer will use to estimate the L1 portion of fees (calldata costs).
* `l2GasPrice`: `QUANTITY` - L2 gas price in wei that the Sequencer will use to estimate the L2 portion of fees (execution costs).

## Example

**Request**

```
curl https://opt-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"rollup_gasPrices","params":[],"id":1}}'
```

**Result**

```
{
  "jsonrpc":"2.0",
  "id":1,
  "result":{
    "l1GasPrice":"0x237aa50984",
    "l2GasPrice":"0xf4240"
  }
}
```
