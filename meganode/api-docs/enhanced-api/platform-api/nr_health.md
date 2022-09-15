---
description: >-
  This API method will allow developers to check the health status of the
  MegaNode service.
---

# nr\_health

It is a GET method to check the health status of the MegaNode service.&#x20;

{% hint style="info" %}
Supported on BSC & Ethereum mainnet only.
{% endhint %}

## Parameters

`None`

## Returns

`None`

``

## Example



{% tabs %}
{% tab title="Curl" %}
```bash
curl --location --request GET 'https://eth-rinkeby.nodereal.io/v1/your-api-key/nr_health'
```
{% endtab %}
{% endtabs %}

If the service status is normal, the return code is 200; otherwise, the return code is 500.
