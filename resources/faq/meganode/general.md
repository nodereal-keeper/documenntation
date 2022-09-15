# General

### **What is MegaNode?**

MegaNode provides easy access to Web3 networks, empowering developers to create decentralized applications and enhance efficiency using reliable infrastructure.

### Why should I use MegaNode?

Running a blockchain node is expensive and time consuming. Also, you need to pay extra attention to maintain a reliable node. MegaNode provides you with affordable, reliable, and instant infrastructure to help you get started.

### What blockchains are available on MegaNode?

We now support Binance Smart Chain, Ethereum Mainnet, Polygon. More chains are coming soon!

### What is the difference between API and RPC endpoint?

We call any programmable interface an API (Application Programming Interface). It is a general concept. For web3 development, we have JSON RPC (Remote Procedure Calls) as the interface for the block chain calls. Almost all the APIs we provide are RPC endpoints. Just be consistent when you discuss the topic with others.

### What is a batch request?

A batch request is designed to allow client applications call multiple requests in one single batch request.&#x20;

{% hint style="info" %}
Please note, a batch request is not suitable for resource-intensive calls, such as debug tracing requests. &#x20;
{% endhint %}

We do not recommend client to encapsulate too many requests in a single batch request, and our system has a limit of 500 requests.

In most cases, NodeReal recommends the individual requests instead of batch requests as the stability design of batch requests is not as high as of individual calls.

### What is the CU limit and how to check my current limit and usage info?

A CU(Computing Unit) limit is a quotation for your subscription. You can query your quota and usage on your dashboard and via our platform API.

### What is an API key?

An API Key is the credential to query all services. When you create an App in your dashboard, an API key will be generated with your NodeReal App. Please note, you should never share your API key to others to prevent others from using your account. If you need additional security for your App, JWT is a good option that you can enable in your App.

### What is a JWT?

A JWT is a security mechanism that you can enable for each app you’ve created. After you enable JWT, you need to add your JWT in your header to send requests to your API endpoints.

For details, you can refer to JWT documentation(https://docs.nodereal.io/nodereal/meganode/json-web-token-jwt).
