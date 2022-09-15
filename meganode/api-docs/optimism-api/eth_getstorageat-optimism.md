---
description: >-
  Returns the value from a storage position at a given address, or in other
  words, returns the state of the contract's storage, which may not be exposed
  via the contract's methods.
---

# eth\_getStorageAt - Optimism

### Parameters

* `ADDRESS` _\[required]_ - a string representing the address (20 bytes) of the storage
* `STORAGE POSITION` _\[required]_ - a hex code of the position in the storage
* `BLOCK PARAMETER` _\[required]_ - an integer block number, or the string "latest", "earliest" or "pending", see the [default block parameter](https://github.com/ethereum/wiki/wiki/JSON-RPC#the-default-block-parameter)

### Returns

* `STORAGE VALUE` - a hex code of the integer indicating the value of the storage position at the provided address

```javascript
{
    "jsonrpc": "2.0",
    "id": 73,
    "result": [{
        "address": "0xb5a5f22694352c15b00323844ad545abb2b11028",
        "blockHash"
```



### Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```
curl https://opt-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0", "method": "eth_getStorageAt", "params": ["0x295a70b2de5e3953354a6a8344e616ed314d7251", "0x0", "latest"], "id": 1}'
```
{% endtab %}
{% endtabs %}



#### Result

```javascript
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x00000000000000000000000000000000000000000000000000000000000004d2"
}
```
