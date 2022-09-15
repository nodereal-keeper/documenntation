# Quick Start

## **How to send my first DirectRout bundle?**

It's very easy to send bundle transactions. We have prepared SDKs and endpoint for bundles.

The Mainnet endpoint: [**https://api.nodereal.io/direct-route**](https://api.nodereal.io/direct-route)****

The Testnet endpoint: [**https://testnet-api.nodereal.io/direct-route**](https://testnet-api.nodereal.io/direct-route)****



**in Golang:**

#### Import dependency of `github.com/node-real/go-direct-route` <a href="#import-dependency-of-github.com-node-real-go-direct-route" id="import-dependency-of-github.com-node-real-go-direct-route"></a>

You can import `github.com/node-real/go-direct-route` in your go.mod. For example:

```
require ( 
github.com/node-real/go-direct-route latest 
)
```

#### Init client <a href="#init-client" id="init-client"></a>

You can init your client with SDK and our endpoint.

```
var directRouteEndPoint = "https://api.nodereal.io/direct-route"
client, _ := client.Dial(directRouteEndPoint)
```

#### Query suggested bundle price <a href="#query-suggested-bundle-price" id="query-suggested-bundle-price"></a>

To ensure your bundle transactions to be processed in time, you need to query the bundle price before sending transactions.

```
price, _ := client.BundlePrice(context.Background())
```

#### Send bundle transactions

For example, you want to transfer BNB to some addresses.

```
var account1, _ = utils.FromHexKey("input your private key1 here")
var account2, _ = utils.FromHexKey("input your private key2 here")

tx1, hash1, _ := utils.SignTransaction(account1, account2.Addr, valueToTransfer, nil, n1, gasLimit, price, chainId)
tx2, hash2, _ := utils.SignTransaction(account2, account1.Addr, valueToTransfer, nil, n2, gasLimit, price, chainId)

maxTime := uint64(time.Now().Unix() + 80)

bundle := &client.SendBundleArgs{
    Txs:               []string{hexutil.Encode(tx1), hexutil.Encode(tx2)},
    MaxBlockNumber:    "",
    MinTimestamp:      nil,
    MaxTimestamp:      &maxTime,
    RevertingTxHashes: nil,
}
bundleHash, err := directClient.SendBundle(context.Background(), bundle)
```

After sending the bundle, you will get the bundle hash for the bundle you sent.



#### Query bundle

For the bundle sent, you can also query the bundle info via sdk:

```
bundle, _ := directClient.GetBundleByHash(context.Background(), bundleHash)
```

For more detailed instructions you can refer to our [node.js sdk](https://github.com/node-real/js-direct-route) or [go sdk](https://github.com/node-real/go-direct-route).

If you want to interact with our endpoint directly, you can also refer to the [API of our endpoint](https://nodereal.gitbook.io/nodereal/direct-route/direct-route-api).

\
\


\
