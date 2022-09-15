---
description: This API method helps you to get the creation transaction for any contract.
---

# nr\_getContractCreationTransaction

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Contract Address` - The address of the contract
* `block Number` - The block number in hex format or the string 'latest' or 'earliest' on which the total supply will be checked

## Returns

* `hash` - string, transaction hash
* `blockNumber` - number of the block
* `blockHash` - string
* `timestamp` - number, block timestamp
* `transactionIndex` - number, transaction index in block
* `from` - string, transaction from address
* `to` - string, transaction to address
* `gas` - number, gas quantity
* `gasPrice` - number, price for gas
* `gasUsed` - number, already used gas
* `cumulativeGasUsed` - number, cumulative used gas
* `ContractAddress` - string, the address of the contract&#x20;
* `txreceiptStatus` - number, transaction receipt status, 1 is success,0 is fail
* `input` - string, a hex encoded input data&#x20;
* `nonce` - number, the number of nonce
* `value` - string

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getContractCreationTransaction","params":["0xc297020be32dc91bb24ce4cad116eb50e55ec5ae"],"id": 1 }'
```

**Result**

```
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": {
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
      "hash": "0x3c49bfbe70e0188142821dfeaba482bce0e44c9953b31415b78b04e836c072dc",
      "blockNumber": 56848,
      "blockHash": "0xf769665c8bf51f0a6678503e1a5e1f2bb494619c3b1fc3cc98eb81f9d6a1ddb8",
      "timestamp": 1598842324,
      "transactionIndex": 0,
      "from": "0xa3fd5cc5ba356433b28209d812ff0cf261881e1b",
      "to": null,
      "gas": 6721975,
      "gasPrice": 20000000000,
      "gasUsed": 225237,
      "cumulativeGasUsed": 225237,
      "contractAddress": "0xc297020be32dc91bb24ce4cad116eb50e55ec5ae",
      "txreceiptStatus": 1,
      "input": "0x608060405234801561001057600080fd5b50336000806101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff1602179055506102b7806100606000396000f3fe608060405234801561001057600080fd5b506004361061004c5760003560e01c80630900f01014610051578063445df0ac146100955780638da5cb5b146100b3578063fdacd576146100fd575b600080fd5b6100936004803603602081101561006757600080fd5b81019080803573ffffffffffffffffffffffffffffffffffffffff16906020019092919050505061012b565b005b61009d6101f7565b6040518082815260200191505060405180910390f35b6100bb6101fd565b604051808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200191505060405180910390f35b6101296004803603602081101561011357600080fd5b8101908080359060200190929190505050610222565b005b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff1614156101f45760008190508073ffffffffffffffffffffffffffffffffffffffff1663fdacd5766001546040518263ffffffff1660e01b815260040180828152602001915050600060405180830381600087803b1580156101da57600080fd5b505af11580156101ee573d6000803e3d6000fd5b50505050505b50565b60015481565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1681565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff16141561027f57806001819055505b5056fea265627a7a723158206e29ec92cab879aa3e985416229ef7528a6b4dca0bd7e02a54561f2d943dd80364736f6c63430005100032",
      "nonce": 0,
      "value": "0x0"
    }
  }
}
```
