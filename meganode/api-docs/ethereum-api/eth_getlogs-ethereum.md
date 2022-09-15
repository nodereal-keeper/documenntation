---
description: Returns an array of all logs matching a given filter object.
---

# eth\_getLogs - Ethereum

{% hint style="info" %}
The response size for getLogs method would be different according to your block range:

* **Block range > 50K**: Not available
* **Block range <= 100**: No response size limit
* **Block range between 100 and 50K**: Maximum 50K records would be responded
{% endhint %}

### Parameters

`Object` - The filter options:

* `address` _\[optional]_ - a string representing the address (20 bytes) to check for balance
* `fromBlock` _\[optional, default is "latest"]_ - an integer block number, or the string "latest", "earliest" or "pending"
* `toBlock` _\[optional, default is "latest"]_ - an integer block number, or the string "latest", "earliest" or "pending"
* `topics`_\[optional]_ - Array of 32 Bytes DATA topics. Topics are order-dependent.
* `blockhash`:_\[optional]_ With the addition of EIP-234, `blockHash` restricts the logs returned to the single block with the 32-byte hash `blockHash`. Using `blockHash` is equivalent to `fromBlock` = `toBlock` = the block number with hash `blockHash`. If `blockHash` is present in in the filter criteria, then neither `fromBlock` nor `toBlock` are allowed.

### Returns

*   `LOG OBJECTS` - An array of log objects, or an empty array if nothing has changed since last poll.

    * logs are objects with following params:
      * `removed`: true when the log was removed, due to a chain reorganization. false if it's a valid log.
      * `logIndex`: integer of the log index position in the block. null when its pending log.
      * `transactionIndex`: integer of the transactions index position log was created from. null when its pending log.
      * `transactionHash`: 32 Bytes - hash of the transactions this log was created from. null when its pending log.
      * `blockHash`: 32 Bytes - hash of the block where this log was in. null when its pending. null when its pending log.
      * `blockNumber`: the block number where this log was in. null when its pending. null when its pending log.
      * `address`: 20 Bytes - address from which this log originated.
      * `data`: contains one or more 32 Bytes non-indexed arguments of the log.
      * `topics`: Array of 0 to 4 32 Bytes of indexed log arguments. (In solidity: The first topic is the hash of the signature of the event (e.g. Deposit(address,bytes32,uint256)), except you declared the event with the anonymous specifier.)

    ###

### Example

#### Request

{% tabs %}
{% tab title="Curl" %}


```
curl https://eth-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getLogs","params":[{"address": "0xb59f67a8bff5d8cd03f6ac17265c550ed8f33907","topics": ["0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef"],"blockHash": "0x8243343df08b9751f5ca0c5f8c9c0460d8a9b6351066fae0acbd4d3e776de8bb"}],"id":0}'
```
{% endtab %}
{% endtabs %}

#### Result

Result

```javascript
{
    "jsonrpc": "2.0",
    "id": 73,
    "result": [{
        "address": "0xb5a5f22694352c15b00323844ad545abb2b11028",
        "blockHash": "0x99e8663c7b6d8bba3c7627a17d774238eae3e793dee30008debb2699666657de",
        "blockNumber": "0x5d12ab",
        "data": "0x0000000000000000000000000000000000000000000000a247d7a2955b61d000",
        "logIndex": "0x0",
        "removed": false,
        "topics": ["0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef", "0x000000000000000000000000bdc0afe57b8e9468aa95396da2ab2063e595f37e", "0x0000000000000000000000007503e090dc2b64a88f034fb45e247cbd82b8741e"],
        "transactionHash": "0xa74c2432c9cf7dbb875a385a2411fd8f13ca9ec12216864b1a1ead3c99de99cd",
        "transactionIndex": "0x3"
    }, {
        "address": "0xe38165c9f6deb144afc9c32c206b024817e1496d",
        "blockHash": "0x99e8663c7b6d8bba3c7627a17d774238eae3e793dee30008debb2699666657de",
        "blockNumber": "0x5d12ab",
        "data": "0x0000000000000000000000000000000000000000000000000000000025c6b720",
        "logIndex": "0x3",
        "removed": false,
        "topics": ["0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef", "0x00000000000000000000000080e73e47173b2d00b531bf83bc39e710157125c3", "0x0000000000000000000000008f6cc93795969e5bbbf07c66dfee7d41ad24f1ef"],
        "transactionHash": "0x9e8f1cb1facb9a11a1cf947634053a0b2d557399f926b12127aa10497a2f0153",
        "transactionIndex": "0x5"
    }
}
```

###

