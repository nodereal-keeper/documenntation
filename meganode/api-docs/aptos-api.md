---
description: >-
  NodeReal Aptos Node API is a RESTful API for client applications to interact
  with the Aptos devnet.
---

# Aptos API

{% hint style="info" %}
Please note that Aptos API is in BETA phase
{% endhint %}

* Server URL: [**aptos-devnet.nodereal.io/v1**](https://aptos-devnet.nodereal.io/v1)****

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/accounts/{address}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/accounts/{address}/resources" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/accounts/{address}/modules" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/spec" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/-/healthy" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/blocks/by_height/{block_height}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/blocks/by_version/{version}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/events/{event_key}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/accounts/{address}/events/{creation_number}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/accounts/{address}/events/{event_handle}/{field_name}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/accounts/{address}/resource/{resource_type}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/accounts/{address}/module/{module_name}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/tables/{table_handle}/item" method="post" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/transactions" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/transactions" method="post" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/transactions/by_hash/{txn_hash}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/transactions/by_version/{txn_version}" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/accounts/{address}/transactions" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/transactions/batch" method="post" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/transactions/simulate" method="post" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/transactions/encode_submission" method="post" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/aptos (1).yaml" path="/estimate_gas_price" method="get" %}
[aptos (1).yaml](<../../.gitbook/assets/aptos (1).yaml>)
{% endswagger %}
