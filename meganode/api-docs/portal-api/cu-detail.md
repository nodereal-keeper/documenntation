---
description: You get query your MegaNode CU detail via this API
---

# cu-detail

{% hint style="info" %}
Please note that Portal API is in BETA phase and only available for Growth & Enterprise customers.
{% endhint %}

## Http method

* GET

## Parameters

* none

## Returns

* Array of data:
  * totalQouta: the total monthly quota according to your pricing plan
  * remainingQuota: the remaining quota of current month&#x20;
  * plan: the pricing plan
  * cups: the rate limit, available CU per second.

## Example

**Request**

```
curl https://portal-api.nodereal.io/v1/your-api-key/cu-detail \
-X GET \
-H "Content-Type: application/json"
```

**Result**

```
{"code":20000,"msg":"","data":{"totalQuota":500000000,"remainingQuota":499979797,"plan":"Growth","cups":1000}
```

