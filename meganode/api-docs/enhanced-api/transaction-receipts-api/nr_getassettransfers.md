---
description: This API method helps you to get the transfers for any address, block, etc.
---

# nr\_getAssetTransfers

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `category` - example: List \[ "external", "20" ]; ------ external, internal; 20, 721, 1155;&#x20;
* `fromBlock` - hexadecimal string or latest, the difference between fromBlock and toBlock must be less than or equal to 50000, when both are specified. If the request has fromBlock but miss toBlock, toBlock will be auto-filled by fromBlock+50000
* `toBlock` -  hexadecimal string or latest, the difference between fromBlock and toBlock must be less than or equal to 50000, when both are specified. If the request has toBlock but miss fromBlock, fromBlock will be auto-filled by toBlock-50000
* `contractAddresses` - contract addresses array; max items: 100
* `fromAddress` - string
* `toAddress` - string
* `order` - option: asc or desc
* `transactionHash` - string
* `excludeZeroValue` - boolean, true for excluding zero value data, false for all data
* `maxCount` - hex encoded value, define once request return data count, max value:0x3E8
* `PageKey` - uuid for pagination. If more results are available, a uuid pageKey will be returned in the response. Pass that uuid into pageKey to fetch the next maxCount. For first page, don't need this param.

## Returns

* `PageKey` - string, page key for next page query
* `transfers` - details
  * `category` - external or internal&#x20;
  * `blockNum` - number
  * `from` - string, from addresss
  * `to` - string, to address
  * `value` - hexadecimal string, raw transfer value
  * `erc721TokenId` - 32-byte fixed-length hexadecimal string
  * `erc1155MetaData` - string, page key for next page query
    * `tokenId` - hexadecimal string
    * `value` - hexadecimal string, raw transfer value
  * `asset` - ETH/BNB or the token's symbol. null if not defined in the contract and not available from other sources.
  * `hash` - string, transaction hash
  * `contractAddress` - contract address (hex string). null if external transfer
  * `decimal` - contract decimal (hex string). null if not defined in the contract and not available from other sources.
  * `blockTimestamp` - timestamp of the block from which the transaction event originated
  * `gasPrice` - gas price for external transfer, not return when category is others
  * `gasUsed` - gas used for external transfer, not return when category is others
  * `receiptsStatus` - receipt status, 1 is success,0 is failed

## Example

**Request**

```
curl https://eth-mainnet.nodereal.io/v1/your-api-key \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"nr_getAssetTransfers","params":[{"category": ["external","20"],"fromBlock": "0xE81916","toBlock": "0xE81917","order": "asc","excludeZeroValue": false,"maxCount": "0x5","pageKey": "qg000000-0075-RyKy-efk2-Fx9n32gAu432"}],"id":1}'
```

**Result**

```
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": {
    "pageKey": "qh000000-0X5j-WSqq-mCLq-kPfWRH8B1GPS",
    "transfers": [
      {
        "category": "external",
        "blockNum": "0x6c92dd",
        "from": "0x646eafba97ec6ee7631887cdee468b323dd65d4f",
        "to": "0x8f07f7312f3ede8b0094f09ab1554c8d89f47ddf",
        "value": "0x0",
        "asset": "BNB",
        "hash": "0xf7605ce61c1855348cde8512d752265a8cbbf57e0ac4c8bc259155f8c1592838",
        "blockTimeStamp": 1620089457,
        "gasPrice": 5000000000,
        "gasUsed": 35813,
        "receiptsStatus": 1
      },
      {
        "category": "20",
        "blockNum": "0x3b8322",
        "from": "0x0554a5d083abf2f056ae3f6029e1714b9a655174",
        "to": "0x28451d455f009a30b37bbe74175c9f3460f45cc7",
        "value": "0x00000000000000000000000000000000000000000000000564d702d38f5e0000",
        "asset": "TWT",
        "hash": "0xc16db18719864e6188578d5870e6f30e84d93c52beeb3630ead1a251e460ce4b",
        "contractAddress": "0x4b0f1812e5df2a09796481ff14017e6005508003",
        "decimal": "18",
        "blockTimeStamp": 1610380207
      },
      {
        "category": "721",
        "blockNum": "0xe97966",
        "from": "0x0000000000000000000000000000000000000000",
        "to": "0xa35ea428864f790f76b80d834b7dbe4340fd8d90",
        "value": "0x0",
        "erc721TokenId": "0x000000000000000000000000000000000000000000000000000000000016ed41",
        "asset": "SpaceShip",
        "hash": "0x6ed64468e1ee365e9670ec373eecdae2ff186d3354e2f88824eddd8d2f1bcccd",
        "contractAddress": "0x25828c7d4914694cbb514bb8f88ef94e715e4819",
        "blockTimeStamp": 1644998842
      },
      {
        "category": "1155",
        "blockNum": "0xeed938",
        "from": "0x0000000000000000000000000000000000000000",
        "to": "0x3acd618733de89269496768784d6b07f844ce480",
        "value": "0x0",
        "erc1155Metadata": [
          {
            "tokenId": "51c7d5f32f7dee06107a3d522b6e0902521ba99806e191acd74b349e00000001",
            "value": "0000000000000000000000000000000000000000000000000000000000000001"
          }
        ],
        "asset": "MELOSPRELUDE1",
        "hash": "0xa931aab01613dce9ab17f22caad4efa3fd209785f675c5d81f19b10179d2f631",
        "contractAddress": "0x42616b05cfe1af50e4488c8930d7e7d65bf87ce9",
        "blockTimeStamp": 1646059155
      }
    ]
  }
}
```
