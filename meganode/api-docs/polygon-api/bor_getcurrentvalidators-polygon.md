---
description: Returns current validators
---

# bor\_getCurrentValidators - Polygon

## Parameters

none

## Returns

`author` - address

## Example

**Request**

```
curl https://polygon-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"bor_getCurrentValidators","params":[], "id":1}'
```

**Result**

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": [
        {
            "ID": 0,
            "signer": "0x46a3a41bd932244dd08186e4c19f1a7e48cbcdf4",
            "power": 1,
            "accum": -15
        },
        {
            "ID": 0,
            "signer": "0x6a654ca3bfb5cfb23bf30bafbf96b3b6ec26bb0e",
            "power": 1,
            "accum": -21
        },
        {
            "ID": 0,
            "signer": "0x7c7379531b2aee82e4ca06d4175d13b9cbeafd49",
            "power": 5,
            "accum": -8
        },
        {
            "ID": 0,
            "signer": "0xe77bbfd8ed65720f187efdd109e38d75eaca7385",
            "power": 2,
            "accum": 5
        },
        {
            "ID": 0,
            "signer": "0xf0245f6251bef9447a08766b9da2b07b28ad80b0",
            "power": 7,
            "accum": -4
        }
    ]
}
```
