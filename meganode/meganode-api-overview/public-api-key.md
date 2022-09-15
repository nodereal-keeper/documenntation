---
description: This document provides the explanation of using MegaNode public API
---

# Public API Key

As a high-speed blockchain infrastructure solution, MegaNode strives to provide an instant and easy-access service to every developer. You can easily create a MegaNode account with [this guide](../getting-started.md). However, we understand you may be sharing your repository with the public, which is not proper to expose your own API key, or you just found MegaNode API endpoint in some projects and would like to try it out. We hear you. That’s why we created this public and shareable API key for you to get started with MegaNode.

{% hint style="info" %}
Public APIs have lower CUPS and it may also have some constraints. If you need full MegaNode access, please start with [this guide](../getting-started.md).
{% endhint %}

## API endpoints

| Chain & Network  | Protocol | Endpoint                                                                                                                                             |
| ---------------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| BSC mainnet      | https    | [https://bsc-mainnet.nodereal.io/v1/64a9df0874fb4a93b9d0a3849de012d3](https://bsc-mainnet.nodereal.io/v1/64a9df0874fb4a93b9d0a3849de012d3)           |
| BSC mainnet      | wss      | [wss://bsc-mainnet.nodereal.io/ws/v1/64a9df0874fb4a93b9d0a3849de012d3](wss://bsc-mainnet.nodereal.io/ws/v1/64a9df0874fb4a93b9d0a3849de012d3)         |
| BSC testnet      | https    | [https://bsc-testnet.nodereal.io/v1/e9a36765eb8a40b9bd12e680a1fd2bc5](https://bsc-testnet.nodereal.io/v1/e9a36765eb8a40b9bd12e680a1fd2bc5)           |
| BSC testnet      | wss      | [wss://bsc-testnet.nodereal.io/ws/v1/e9a36765eb8a40b9bd12e680a1fd2bc5](wss://bsc-testnet.nodereal.io/ws/v1/e9a36765eb8a40b9bd12e680a1fd2bc5)         |
| Ethereum mainnet | https    | [https://eth-mainnet.nodereal.io/v1/1659dfb40aa24bbb8153a677b98064d7](https://eth-mainnet.nodereal.io/v1/1659dfb40aa24bbb8153a677b98064d7)           |
| Ethereum mainnet | wss      | [wss://eth-mainnet.nodereal.io/ws/v1/1659dfb40aa24bbb8153a677b98064d7](wss://eth-mainnet.nodereal.io/ws/v1/1659dfb40aa24bbb8153a677b98064d7)         |
| Ethereum Rinkeby | https    | [https://eth-rinkeby.nodereal.io/v1/a4da384bf3334c5ea992eb0bf44135e0](https://eth-rinkeby.nodereal.io/v1/a4da384bf3334c5ea992eb0bf44135e0)           |
| Ethereum Rinkeby | wss      | [wss://eth-rinkeby.nodereal.io/ws/v1/a4da384bf3334c5ea992eb0bf44135e0](wss://eth-rinkeby.nodereal.io/ws/v1/a4da384bf3334c5ea992eb0bf44135e0)         |
| Ethereum Goerli  | https    | [https://eth-goerli.nodereal.io/v1/8a4432e42df94dcca2814fde8aea2a2e](https://eth-goerli.nodereal.io/v1/8a4432e42df94dcca2814fde8aea2a2e)             |
| Ethereum Goerli  | wss      | [wss://eth-goerli.nodereal.io/ws/v1/8a4432e42df94dcca2814fde8aea2a2e](wss://eth-goerli.nodereal.io/ws/v1/8a4432e42df94dcca2814fde8aea2a2e)           |
| Polygon mainnet  | https    | [https://polygon-mainnet.nodereal.io/v1/f510fc4d083b49d1ab383d25246cc7de](https://polygon-mainnet.nodereal.io/v1/f510fc4d083b49d1ab383d25246cc7de)   |
| Polygon mainnet  | wss      | [wss://polygon-mainnet.nodereal.io/ws/v1/f510fc4d083b49d1ab383d25246cc7de](wss://polygon-mainnet.nodereal.io/ws/v1/f510fc4d083b49d1ab383d25246cc7de) |

## Rate Limit

We enabled rate limit for these public API keys with 2000CU per minute for each IP address. That means, if one IP address sent requests to MegaNode with more than 2000CU in one minute, the further request will be blocked and receive -32005 error code as below.

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "error": {
        "code": -32005,
        "message": "You have reached the maximum API usage limit. If you need higher throughput, please check out https://meganode.nodereal.io/"
    }
}
```

&#x20;If you see above message and code, you will need to retry in the next minute.



