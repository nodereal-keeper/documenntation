---
description: >-
  This API method helps you to sum the totalSupply of every token id in an
  ERC1155 token.
---

# nr\_getSummedSupply1155

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `Token Address` - The address of the ERC1155/BEP1155 token

## Returns

* `SummedSupply` - the hex decoded summed Summed supply

## Example

**Request**

```
curl https://bsc-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"nr_getSummedSupply1155","params":["0xed8711feff83b446158259981fd97645856e82a5"],"id": 1 }'
```

**Result**

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "result": "0x123456"
}
```

****

