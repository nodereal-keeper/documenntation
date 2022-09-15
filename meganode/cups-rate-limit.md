---
description: >-
  Explanation of Compute Unit Per Second (CUPS), and how MegaNode uses it as
  rate limit
---

# CUPS (Rate Limit)

## Why Rate Limit?

MegaNode enabled rate limits to ensure customers utilize our service fairly, in order to provide a more stable and sustainable service. The rate limits will be implemented based on each second, that means in most cases, as long as you've handled retries when receiving rate limits error, the requests will go through in the following second, and it will not affect your experience.

We use CUPS to measure and implement the rate limit, and provide different CUPS for different tiers of MegaNode users.&#x20;



## What is CUPS?

Compute Unit Per Second (CUPS) is a measure of the number of [Compute Units](compute-units-cus.md) used per second when making requests. The weight of each RPC method is different, it will be more efficient than just calculating the numbers of requests sent in a second in different use cases.

See below the CUPS for different tiers of users

