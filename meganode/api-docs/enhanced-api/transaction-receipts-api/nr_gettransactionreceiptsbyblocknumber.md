---
description: >-
  This API method helps you to get all transaction receipts for a given block
  number.
---

# nr\_getTransactionReceiptsByBlockNumber

{% hint style="info" %}
Supported on BSC & Ethereum mainnet only.
{% endhint %}

## Parameters

* `blockNumber`- The block number you want to get transaction receipts for.

{% hint style="info" %}
Please note the blockNumber should be in the HEX string format. e.g. 0x11a6c2c
{% endhint %}

```
"params": [
      "0x11a6c2c",
  ]
```

## Returns

`Object` - The response with a list of transaction receipts. See [eth\_gettransactionreceipt](../../ethereum-api/eth\_gettransactionreceipt-ethereum.md) for the payload.



## Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getTransactionReceiptsByBlockNumber","params":["0x11a6c2c"],"id": 0 }'
```
{% endtab %}
{% endtabs %}

#### "Result

```javascript
{
  "jsonrpc": "2.0",
  "id": 0,
  "result": [
    {
      "type": "0x0",
      "from": "0x4acc5a5505e6ce8be4a93fa9eab4529de6cdceff",
      "to": "0x0000000000f7cdcb778b0c33b09e175e4786f943",
      "status": "0x1",
      "cumulativeGasUsed": "0x12904",
      "logsBloom": "0x00200000010000000000000080000010000400000400000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000001000008000000200000000000000000004000000000000000008000000000000000000000000000000000000000004000000010000000000000000000000002008000000001000000000000000000080000004000000000000000000000000000000000000000000000000000000000000000000000000000000002000000000000000000000000200000000000001000000800000000000000010000000000000000000000000000010000000000000000020004000000",
      "logs": [
        {
          "address": "0x55d398326f99059ff775485246999027b3197955",
          "topics": [
            "0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef",
            "0x0000000000000000000000000000000000f7cdcb778b0c33b09e175e4786f943",
            "0x000000000000000000000000b19fb4ae2fd58d0c6503a3f375eb0d80bd523d03"
          ],
          "data": "0x00000000000000000000000000000000000000000000012002d5ffff439c0000",
          "blockNumber": "0x11a6c2c",
          "transactionHash": "0xe57ca657da05171aafbe5bea40758808b04f6d03a964dfb803f0ba16d14b887b",
          "transactionIndex": "0x0",
          "blockHash": "0x18ef932f9fe3f5c52c8f489c4a466c0e034b85225eb9c6b1415abce6006bf88a",
          "logIndex": "0x0",
          "removed": false
        },
        {
          "address": "0xa6660e62c223df2d9aff0ba188f1371087fa3dd6",
          "topics": [
            "0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef",
            "0x000000000000000000000000b19fb4ae2fd58d0c6503a3f375eb0d80bd523d03",
            "0x000000000000000000000000828fc6f7d3d58776c17a2f86391cf66290e86766"
          ],
          "data": "0x00000000000000000000000000000000000000000000000a4133a1ada9ed4f53",
          "blockNumber": "0x11a6c2c",
          "transactionHash": "0xe57ca657da05171aafbe5bea40758808b04f6d03a964dfb803f0ba16d14b887b",
          "transactionIndex": "0x0",
          "blockHash": "0x18ef932f9fe3f5c52c8f489c4a466c0e034b85225eb9c6b1415abce6006bf88a",
          "logIndex": "0x1",
          "removed": false
        },
        {
          "address": "0xa6660e62c223df2d9aff0ba188f1371087fa3dd6",
          "topics": [
            "0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef",
            "0x000000000000000000000000b19fb4ae2fd58d0c6503a3f375eb0d80bd523d03",
            "0x0000000000000000000000000000000000f7cdcb778b0c33b09e175e4786f943"
          ],
          "data": "0x0000000000000000000000000000000000000000000003f736f78628b6c5ad7b",
          "blockNumber": "0x11a6c2c",
          "transactionHash": "0xe57ca657da05171aafbe5bea40758808b04f6d03a964dfb803f0ba16d14b887b",
          "transactionIndex": "0x0",
          "blockHash": "0x18ef932f9fe3f5c52c8f489c4a466c0e034b85225eb9c6b1415abce6006bf88a",
          "logIndex": "0x2",
          "removed": false
        },
        {
          "address": "0xb19fb4ae2fd58d0c6503a3f375eb0d80bd523d03",
          "topics": [
            "0x1c411e9a96e071241c2f21f7726b17ae89e3cab4c78be50e062b03a9fffbbad1"
          ],
          "data": "0x0000000000000000000000000000000000000000000005fbf52ca8b0000285bf00000000000000000000000000000000000000000000115832c0dc7f73fc9577",
          "blockNumber": "0x11a6c2c",
          "transactionHash": "0xe57ca657da05171aafbe5bea40758808b04f6d03a964dfb803f0ba16d14b887b",
          "transactionIndex": "0x0",
          "blockHash": "0x18ef932f9fe3f5c52c8f489c4a466c0e034b85225eb9c6b1415abce6006bf88a",
          "logIndex": "0x3",
          "removed": false
        },
        {
          "address": "0xb19fb4ae2fd58d0c6503a3f375eb0d80bd523d03",
          "topics": [
            "0xd78ad95fa46c994b6551d0da85fc275fe613ce37657fb8d5e3d130840159d822",
            "0x0000000000000000000000000000000000f7cdcb778b0c33b09e175e4786f943",
            "0x0000000000000000000000000000000000f7cdcb778b0c33b09e175e4786f943"
          ],
          "data": "0x00000000000000000000000000000000000000000000012002d5ffff439c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000401782b27d660b2fcce",
          "blockNumber": "0x11a6c2c",
          "transactionHash": "0xe57ca657da05171aafbe5bea40758808b04f6d03a964dfb803f0ba16d14b887b",
          "transactionIndex": "0x0",
          "blockHash": "0x18ef932f9fe3f5c52c8f489c4a466c0e034b85225eb9c6b1415abce6006bf88a",
          "logIndex": "0x4",
          "removed": false
        }
      ],
      "transactionHash": "0xe57ca657da05171aafbe5bea40758808b04f6d03a964dfb803f0ba16d14b887b",
      "contractAddress": null,
      "gasUsed": "0x12904",
      "blockHash": "0x18ef932f9fe3f5c52c8f489c4a466c0e034b85225eb9c6b1415abce6006bf88a",
      "blockNumber": "0x11a6c2c",
      "transactionIndex": "0x0"
    },
    {
      "type": "0x0",
      "from": "0xb48b978ab606fb6065097a7403e47e58ca464462",
      "to": "0xbdb531548f0dc1995726b6fb509472a5b90b0572",
      "status": "0x1",
      "cumulativeGasUsed": "0x168f9",
      "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
      "logs": [
        
      ],
      "transactionHash": "0x32e76f320859c550f4b75b074a60381d1fc6ae2abe8545bd7bed44d6bccb87b1",
      "contractAddress": null,
      "gasUsed": "0x3ff5",
      "blockHash": "0x18ef932f9fe3f5c52c8f489c4a466c0e034b85225eb9c6b1415abce6006bf88a",
      "blockNumber": "0x11a6c2c",
      "transactionIndex": "0x1"
    },
    ...
  ]
}
```
