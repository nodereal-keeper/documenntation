---
description: The log of MegaNode changes and releases to API and features.
---

# Changelog

## Past

### August 31, 2022

* **\[Chains & Network]** New chain released! We are glad to announce MegaNode users can access Optimism now.
* **\[API Marketplace]** Released 4 new enhanced API on API Marketplace:
  * [nr\_getNFTCollectionHolders](api-docs/enhanced-api/nft-api/nr\_getnftcollectionholders.md)
  * [nr\_getNFTInventory](api-docs/enhanced-api/nft-api/nr\_getnftinventory.md)
  * [nr\_getNFTHolders](api-docs/enhanced-api/nft-api/nr\_getnftholders.md)
  * [nr\_getNFTHoldings](api-docs/enhanced-api/nft-api/nr\_getnftholdings.md)

### August 24, 2022

* **\[API Marketplace]** Released 2 new enhanced API on API Marketplace:
  * [nr\_getTotalSupply1155](api-docs/enhanced-api/nft-api/nr\_getsummedsupply1155.md)
  * [nr\_getNFTMeta](api-docs/enhanced-api/nft-api/nr\_getnftmeta.md)

### August 23, 2022

* **\[Chains & Network]** Released a chain page for Aptos, see what NodeReal can do on Aptos. [https://nodereal.io/aptos](https://nodereal.io/aptos)

### August 19, 2022

* **\[Feature]** Released brand new API marketplace, providing more and more enhanced API to boost your productivity.

### August 5, 2022

* **\[Feature]** Optimized the CU quota calculation.

### July 29, 2022

* **\[Feature]** Released a new login option: Discord.&#x20;

### July 21, 2022

* **\[API]** Released a new Portal API to help you query your usage. See [https://docs.nodereal.io/nodereal/meganode/api-docs/portal-api](https://docs.nodereal.io/nodereal/meganode/api-docs/portal-api) for detail.
* **\[Feature]** The Composer now supports Polygon apps.

### July 15, 2022

* **\[Chains & Network]** New chain released! We are glad to announce MegaNode users can access Polygon now.&#x20;
* **\[Feature]** Released an improvement to help you get started for the first app.

### July 14, 2022

* **\[Feature]** Released "Contact Us" page to easier collect voices of customers. [https://nodereal.io/contact-us](https://nodereal.io/contact-us)&#x20;

### July 7, 2022

* **\[API]** eth\_getLogs & __ eth\_getFilterLogs on BSC & ETH mainnet handled block ranges as below:
  * **Block range > 50K**: Not available
  * **Block range <= 100**: No response size limit
  * **Block range between 100 and 50K**: Maximum 50K records would be responded
* **\[API]** Added health check API. You can check most current MegaNode service status via [https://\<CHAIN-NETWORK-NAME>.nodereal.io/v1/\<YOUR-API-KEY>/nr\_health](broken-reference)&#x20;
  * http status 200: Healthy
  * http status 500: Unhealthy
* **\[Ethereum]** Released [The Merge](https://nodereal.io/the-merge) page to guide you understand the upcoming Ethereum merge and how NodeReal can help you.

### July 4, 2022

* **\[Chain & Network]** Added Ethereum Goerli as part our supported network. You can create your first Goerli app in MegaNode now.&#x20;

### June 30, 2022

* **\[Feature]** Released a new security enhancement. The MegaNode users were able to send requests with JWT for more secured service. See [https://docs.nodereal.io/nodereal/meganode/json-web-token-jwt](https://docs.nodereal.io/nodereal/meganode/json-web-token-jwt) for more.&#x20;

### June 27, 2022

* **\[API]** Optimized the performance of filter related RPC API.
* **\[Homepage]** Released a brand new NodeReal homepage, consolidated product portfolio and service information. Hope you enjoy it!

### June 24, 2022

* **\[API]** Released two enhanced APIs on Ethereum mainnet. [nr\_getTransactionReceiptsByBlockHash](https://docs.nodereal.io/nodereal/meganode/api-docs/enhanced-api/nr\_gettransactionreceiptsbyblockhash) & [nr\_getTransactionReceiptsByBlockNumber](https://docs.nodereal.io/nodereal/meganode/api-docs/enhanced-api/nr\_gettransactionreceiptsbyblocknumber)

### June 20, 2022

* **\[API]** Optimized the performance of blocks related RPC API.

### June 10, 2022

* **\[Feature]** Connect your MetaMask wallet with most reliable MegaNode RPC API. Available on Chrome, Firefox, Edge and Brave. [https://docs.nodereal.io/nodereal/meganode/connect-to-wallet](https://docs.nodereal.io/nodereal/meganode/connect-to-wallet)

### June 9, 2022

* **\[API]** Released a MegaNode public API to help you get started immediately. See [https://docs.nodereal.io/nodereal/meganode/meganode-api-overview/public-api-key](https://docs.nodereal.io/nodereal/meganode/meganode-api-overview/public-api-key) for more.
* **\[API]** Released two enhanced APIs on BSC mainnet. [nr\_getTransactionReceiptsByBlockHash](https://docs.nodereal.io/nodereal/meganode/api-docs/enhanced-api/nr\_gettransactionreceiptsbyblockhash) & [nr\_getTransactionReceiptsByBlockNumber](https://docs.nodereal.io/nodereal/meganode/api-docs/enhanced-api/nr\_gettransactionreceiptsbyblocknumber)

