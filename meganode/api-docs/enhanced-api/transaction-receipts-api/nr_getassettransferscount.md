---
description: This API method helps you to get the transfers count for any address.
---

# nr\_getAssetTransfersCount

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `category` - example: List \[ "external", "20" ]; ------ external, internal; 20, 721, 1155;&#x20;
* `fromBlock` - hexadecimal string or latest
* `toBlock` -  hexadecimal string or latest
* `contractAddresses` - contract addresses array; max items: 100
* `fromAddress` - string
* `toAddress` - string
* `transactionHash` - string
* `excludeZeroValue` - boolean, true for excluding zero value data, false for all data

## Returns

* `transfer count` - string, a hex-encoded number of transfers

## Example

**Request**

```
curl https://eth-mainnet.nodereal.io/v1/your-api-key \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"nr_getAssetTransfersCount","params":[{"category": ["external","20"],"fromBlock": "0xE81916","toBlock": "0xE81917","excludeZeroValue": false}],"id":1}'
```

**Result**

```
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": "0x4"
}
```
