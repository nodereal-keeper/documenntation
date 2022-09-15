---
description: Detailed introduction of DirectRoute API
---

# API docs

The Mainnet endpoint: [**https://api.nodereal.io/direct-route**](https://api.nodereal.io/direct-route)****

The Testnet endpoint: [**https://testnet-api.nodereal.io/direct-route**](https://testnet-api.nodereal.io/direct-route)****

## &#x20;:orange\_book: Bundles

Calls related to bundles&#x20;

### eth\_sendBundle

Returns the bundle hash if it is accepted by the service.

**Parameters**

* `txs`,  Array\[String], A list of signed transactions to execute in an atomic bundle
* `maxBlockNumber`, String, a hex encoded block number for which this bundle is valid before.
* `minTimestamp`, (Optional) Number, the minimum timestamp for which this bundle is valid, in seconds since the unix epoch
* `maxTimestamp`,(Optional) Number, the maximum timestamp for which this bundle is valid, in seconds since the unix epoch
* `revertingTxHashes`,(Optional) Array\[String], A list of tx hashes that are allowed to revert

**Returns**

`Object` - An object with the following fields, or null when nothing was found:

* `hash`: Number - Returns the bundle hash if it is accepted by the service.

**Example**

{% tabs %}
{% tab title="Curl" %}
```
curl -X POST https://api.nodereal.io/direct-route \
--data '{"jsonrpc":"2.0","method":"eth_sendBundle",\
"params":[{"txs": ["0xf87181f785028fa6ae00830f424094d11bb98886dc49a8a925d830511e1db43be528658609184e72a00084f9da581d81e6a0c9c62706b5425cc51da2e20e2861d18b6c79d83cede37d582f40ce85fd79af06a0605c3d97b55f405f687de99425bff0ced9e5cd9830ea168a747e6517161eff0a"], "maxBlockNumber":"0x123", "minTimestamp": "231","maxTimestamp":"1231", "revertingTxHashes": ["xx1","xx2"]}],"id":83}' \
-H "Content-Type: application/json"
```
{% endtab %}

{% tab title="Postman" %}
```http
URL: https://api.nodereal.io/direct-route
RequestType: POST
Body: 
{
    "jsonrpc":"2.0",
    "method":"eth_sendBundle",
    params":[{"txs": ["0xf87181f785028fa6ae00830f424094d11bb98886dc49a8a925d830511e1db43be528658609184e72a00084f9da581d81e6a0c9c62706b5425cc51da2e20e2861d18b6c79d83cede37d582f40ce85fd79af06a0605c3d97b55f405f687de99425bff0ced9e5cd9830ea168a747e6517161eff0a"], "maxBlockNumber":"0x123", "minTimestamp": "231","maxTimestamp":"1231", "revertingTxHashes": ["xx1","xx2"]}],
    "id":0
}
```
{% endtab %}
{% endtabs %}

**Result**

```javascript
{
   "jsonrpc":"2.0",
   "id":83,
   "result":"0x2ed12f960e3c47fc8ea5a26d047c3ce11c166c68e65cd51d700d5fb070ea4894"
}
```

### **eth\_bundlePrice**

Returns the suggested bundle price.\
**Parameters**

none

**Returns**

`bundlePrice` - integer of the current median gas price of transactions in the bundle.\
`minimalGasPrice` - integer of the current suggested bundle price. (valid for 60 seconds)

**Example**

{% tabs %}
{% tab title="Curl" %}
```javascript
curl -X POST https://api.nodereal.io/direct-route \
--data '{"jsonrpc":"2.0","method":"eth_bundlePrice","params":[],"id":83}' \
-H "Content-Type: application/json"
```
{% endtab %}

{% tab title="Postman" %}
```http
URL: https://api.nodereal.io/direct-route
RequestType: POST
Body: 
{
    "jsonrpc":"2.0",
    "method":"eth_bundlePrice",
    params":[],
    "id":0
}
```
{% endtab %}
{% endtabs %}

**Return**

```javascript
{ 
  "jsonrpc": "2.0",
  "id": 83,
  "result": {
     "bundlePrice": 20000000000,
     "minimalGasPrice": 28538517104 
  } 
}
```

### txpool\_getBundleByHash

Returns the bundle object if it exists.\
**Parameters**

* `bundleHash`: the hash of the bundle.

**Returns**

* `txs`,  Array\[String], A list of signed transactions to execute in an atomic bundle
* `maxBlockNumber`, String, a hex encoded block number for which this bundle is valid before.
* `minTimestamp`, (Optional) Number, the minimum timestamp for which this bundle is valid, in seconds since the unix epoch
* `maxTimestamp`,(Optional) Number, the maximum timestamp for which this bundle is valid, in seconds since the unix epoch
* `revertingTxHashes`,(Optional) Array\[String], A list of tx hashes that are allowed to revert
* `status`, Number, 0 means pending, 1 means success, 2 means fail.
* &#x20;`errMsg`, String, the detailed error message if the bundle fails.

**Example**

{% tabs %}
{% tab title="Curl" %}
```javascript
curl -X POST https://api.nodereal.io/direct-route \
--data '{"jsonrpc":"2.0","method":"txpool_getBundleByHash","params":[“0x2ed12f960e3c47fc8ea5a26d047c3ce11c166c68e65cd51d700d5fb070ea4894”],"id":83}'\
-H "Content-Type: application/json"
```
{% endtab %}

{% tab title="Postman" %}
```http
URL: https://api.nodereal.io/direct-route
RequestType: POST
Body: 
{
    "jsonrpc":"2.0",
    "method":"txpool_getBundleByHash",
    params":[“0x2ed12f960e3c47fc8ea5a26d047c3ce11c166c68e65cd51d700d5fb070ea4894”],
    "id":0
}
```
{% endtab %}
{% endtabs %}

**Return**

```javascript
{
   "jsonrpc":"2.0",
   "id":83,
   "result":{
      "txs":[
         "0xf87181f785028fa6ae00830f424094d11bb98886dc49a8a925d830511e1db43be528658609184e72a00084f9da581d81e6a0c9c62706b5425cc51da2e20e2861d18b6c79d83cede37d582f40ce85fd79af06a0605c3d97b55f405f687de99425bff0ced9e5cd9830ea168a747e6517161eff0a"
      ],
      "maxBlockNumber":"0x123",
      "minTimestamp":"231",
      "maxTimestamp":"1231",
      "revertingTxHashes":[
         "xx1",
         "xx2"
      ],
    "status":0,
    "errMsg": ""
   }
}
```

### eth\_validatorStatus

Returns the status of direct route service.

**Parameters**

none

**Returns**

* `status`, the status of the service, 0 means available, 1 means unavailable.&#x20;
* `validators`, the status of each validator which supports direct-route, 0 means alive, 1 means offline.

**Example**

{% tabs %}
{% tab title="Curl" %}
```javascript
curl -X POST https://api.nodereal.io/direct-route \
--data '{"jsonrpc":"2.0","method":"eth_validatorStatus","params":[],"id":83}' \
-H "Content-Type: application/json"
```
{% endtab %}

{% tab title="Postman" %}
```
URL: https://api.nodereal.io/direct-route
RequestType: POST
Body: 
{
    "jsonrpc":"2.0",
    "method":"eth_validatorStatus",
    "id":0
}
```
{% endtab %}
{% endtabs %}

**Return**

```
{
   "jsonrpc":"2.0",
   "id":83,
   "result":{
      "status":0,
      "validators": {
         "nodeReal":0
      }
   }
}
```

### Coming soon

The service will soon refactor the **txpool\_getBundleByHash** API and support query bundle history soon. Before that you may need to query the status of your transaction on chain to confirm whether the bundle is successful or not. For more details please refer to our [examples](https://github.com/node-real/go-direct-route/blob/master/example/example.go).
