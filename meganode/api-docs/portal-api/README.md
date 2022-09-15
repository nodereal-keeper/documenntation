---
description: You can access MegaNode dashboard metrics & account information via Portal API
---

# Portal API

MegaNode provides basic statistics regarding the JSON-RPC API usage. You can easily find the average response time and total number of requests sent in the past 24 hours on the dashboard. This statistics dashboard help you to monitor your apps performance at glance, and now we make it more simpler, you can access those statistics via Portal API.

{% hint style="info" %}
Please note that Portal API is in BETA phase and only available for Growth & Enterprise customers.
{% endhint %}

## Find your API endpoint

![Find your API endpoint in Account page](<../../../.gitbook/assets/Screen Shot 2022-07-21 at 21.52.09 (1).png>)

You can use this API to query statistics, such as your pricing plan, monthly quota & the remaining quota (CU). By sending request to this API endpoint, you will have more direct integration with MegaNode, like monitoring the latest CU usage and take actions automatically before consuming all the CUs. We will soon support more statistics to help you retrieve all the MegaNode data you need for your business.

Get started with our first cu-detail API.

{% content-ref url="cu-detail.md" %}
[cu-detail.md](cu-detail.md)
{% endcontent-ref %}
