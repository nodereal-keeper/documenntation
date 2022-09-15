---
description: >-
  This API method provides all details of transactions in pool, including
  'pending' and 'queued' transactions. Details include address "from", gas,
  gasPrice, transaction hash, etc.
---

# txpool\_content

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `None`

## Returns

* `array` - list of pending and queued transactions, with each having the following fields:
  * `pending` - Array of transaction objects, with following fields
    * `blockHash` - Hash of the block where this transaction was in, null here.
    * `blockNumber` - Block number where this transaction was added encoded as a hexadecimal, null here.
    * `from` - Address of the sender.
    * `gas` - The total amount of gas units used in the transaction.
    * `gasPrice` - The total amount in wei the sender is willing to pay for the transaction.
    * `hash` - Hash of the transaction.
    * `input` - Encoded transaction input data.
    * `nonce` - Number of transactions the sender has sent till now.
    * `r` - ECDSA signature r.
    * `s` - ECDSA signature s.
    * `to` - Address of the receiver. null when its a contract creation transaction.
    * `transactionIndex` - Integer of the transactions index position in the block encoded as a hexadecimal.
    * `type` - A number between 0 and 0x7f, for a total of 128 possible transaction types.
    * `v` - ECDSA recovery id encoded as a hexadecimal.
    * `value` - Value transferred in Wei encoded as a hexadecimal.
  * `queued`  - Array of transaction objects, with following fields:
    * `accesslist` - A list of addresses and storage keys that the transaction plans to access, introduced in EIP-2929.
    * `blockHash` - Hash of the block where this transaction was in, null here.
    * `blockNumber` - Block number where this transaction was added encoded as a hexadecimal, null here.
    * `chainId` - The current network/chain ID, used to sign repplay-protected transaction introduced in EIP-155.
    * `from` - Address of the sender.
    * `gas` - The total amount of gas units used in the transaction.
    * `gasPrice` - The total amount in wei the sender is willing to pay for the transaction.
    * `hash` - Hash of the transaction.
    * `input` - Encoded transaction input data.
    * `maxFeePerGas` - The maximum amount of gas willing to be paid for the transaction.
    * `maxPriorityFeePerGas` - The maximum amount of gas to be included as a tip to the miner.
    * `nonce` - Number of transactions the sender has sent till now.
    * `r` - ECDSA signature r.
    * `s` - ECDSA signature s.
    * `to` - Address of the receiver. null when its a contract creation transaction.
    * `transactionIndex` - Integer of the transactions index position in the block encoded as a hexadecimal.
    * `type` - A number between 0 and 0x7f, for a total of 128 possible transaction types.
    * `v` - ECDSA recovery id encoded as a hexadecimal.
    * `value` - Value transferred in Wei encoded as a hexadecimal.

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"txpool_content","params":[],"id":1}'
```

**Result**

```
{
  "jsonrpc":"2.0",
  "id":1,
  "result":{
    "pending":{
      "0x0000412b8ccb938cd2a3f473c3ce466cdedee049":{
        "36096":{
          "blockHash":null,
          "blockNumber":null,
          "from":"0x0000412b8ccb938cd2a3f473c3ce466cdedee049",
          "gas":"0x2dc6c0",
          "gasPrice":"0x138eca480",
          "hash":"0xb6721e4888adc621158aed7586ea80db4f96529cf5bad16ae1795bbae5eba9a3",
          "input":"0x000000000300010026f2271084ee532a0d4238f5fc4a1e8c043f8749ed4f274dbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c05000100022710f2b9155e3c9756a18ef6572",
          "nonce":"0x8d00",
          "to":"0x05ccc798a921800441291636640880045cebe7c6",
          "transactionIndex":null,
          "value":"0x0",
          "type":"0x0",
          "v":"0x94",
          "r":"0x19eba5a20f3e4d0cdd5f8b5d93b1127e7bbc7426267398e4cbef5c8928648b34",
          "s":"0x44d235ded909b9ac279a1a350507f554d0eb1846c3cf1b36e9d1b535e2eee524"
        }
      }
    },
    "queued":{
      "0xa267828beb9ed84b0e91d3341fbb973153b9b925":{
        "315743":{
          "blockHash":null,
          "blockNumber":null,
          "from":"0xa267828beb9ed84b0e91d3341fbb973153b9b925",
          "gas":"0x5cc60",
          "gasPrice":"0x147d35700",
          "hash":"0xe13dbbce3cfc30f18027c3cc0b8857ee5d412e6d20bded9a4e8ed1f52cde747d",
          "input":"0x8ca0d39c00000000000000000000000000000000000000000000000000000000000000c00000000000000000000000000000000000",
          "nonce":"0x4d15f",
          "to":"0xb400af9ff00e7ba1f6aac4eeff475e965f9cba1f",
          "transactionIndex":null,
          "value":"0x0",
          "type":"0x0",
          "v":"0x94",
          "r":"0xdb838ea3f72e1bf066cab996e448698399130a4c159d4fe1507f342a107c47f8",
          "s":"0x60f7ba3eee2a382852d7b1971838c3ec9702dca705811170b6c4696d7b1fa14c"
        }
      }
    }
  }
}
```
