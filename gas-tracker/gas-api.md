# Gas Tracker API

## Get gas price

**Http Request**

Query BSC's GasPrice forecast data. Interface data updates per 5s. Please don't access it frequently, or you will be blocked.

```
GET https://api.nodereal.io/node/gasInfo
```

Response Example

```
{
  "code": 200,
  "error_msg": "",
  "data": {
    "rapid": 7100000000,
    "fast": 5000000000,
    "standard": 5000000000,
    "timestamp": 1632374875000,
    "gasUsedRatio": 0.2657367500639997,
    "pendingQueueLength": 355
  }
}
```

