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



{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/accounts/{address}" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/accounts/{address}/resources" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/accounts/{address}/modules" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/spec" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/-/healthy" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/blocks/by_height/{block_height}" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/blocks/by_version/{version}" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/events/{event_key}" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/accounts/{address}/events/{event_handle}/{field_name}" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/accounts/{address}/resource/{resource_type}" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/accounts/{address}/module/{module_name}" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/tables/{table_handle}/item" method="post" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/transactions" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/transactions" method="post" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/transactions/by_hash/{txn_hash}" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/transactions/by_version/{txn_version}" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/accounts/{address}/transactions" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/transactions/batch" method="post" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/transactions/simulate" method="post" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/transactions/encode_submission" method="post" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml" path="/estimate_gas_price" method="get" %}
[https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml](https://raw.githubusercontent.com/aptos-labs/aptos-core/main/api/doc/spec.yaml)
{% endswagger %}
