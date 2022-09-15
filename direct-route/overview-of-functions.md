# Overview of Functions

## Trading Proxy <a href="#trading-proxy" id="trading-proxy"></a>

#### Working mechanism

A private trading proxy mainly composed of DR\_relay and BSC\_Geth. Transactions initiated through Direct Route will be sent to a private trading pool where only the traders and the specific block producers can see the transaction. Traders only need to set up gas fee according to their needs. There is no need to massively increase gas fee because others set up higher gas fee.

When the transactions reach the private transaction pool, they will be seen by block producers (with BSC\_Geth) working with Direct Route and packed into blocks based on the level of gas fee from high to low. Traders do not need to pay gas fees for failed transactions. On a conventional blockchain network, block producers select transactions with high gas fees in the public transaction pool and pack them. Because there are too many failed transactions, the network can be congested at times.

The complete process is as follows:

![](<../.gitbook/assets/image (4).png>)

![](blob:https://nodereal.atlassian.net/696553f6-4cd8-4533-854e-3277ebe6f717#media-blob-url=true\&id=89c094af-c216-4107-b0eb-0337a958cfa8\&collection=contentId-7569443\&contextId=7569443\&mimeType=image%2Fpng\&name=image-20211113-083708.png\&size=63447\&height=343\&width=1280\&alt=)

#### **Roadmap** <a href="#roadmap" id="roadmap"></a>

Direct Route is moving forward quickly to achieve its ultimate goal: protect your transactions and improve profit extraction on the blockchain network. Here is an overview of its roadmap in the following 4 seasons.

![](<../.gitbook/assets/image (3).png>)

![](blob:https://nodereal.atlassian.net/a6d1ee37-9ba6-4350-adbf-3984e2f488b8#media-blob-url=true\&id=8aa89780-e47d-433c-8371-737a369f03a5\&collection=contentId-7569443\&contextId=7569443\&mimeType=image%2Fpng\&name=image-20211214-090834.png\&size=75555\&height=540\&width=960\&alt=)

## &#x20;DirectRoute Explore（Coming Soon） <a href="#mev-explore-coming-soon" id="mev-explore-coming-soon"></a>
