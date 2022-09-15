---
description: >-
  This page provides self-service troubleshooting for MegaNode users when
  encountering errors.
---

# MegaNode: Handling Errors



| ERROR                                                                           | DESCRIPTION                                                              | SOLUTION                                                                                    |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------- |
| <p>code: -32000</p><p>message: Unauthorized</p>                                 | Invalid KEY                                                              | See your MegaNode account for the valid API KEY                                             |
| <p>code:-32000</p><p>message: timeout</p>                                       | Request hit 30 seconds timeout                                           | Splitting heavy subqueries into smaller bites                                               |
| <p>code: -32002</p><p>message: IP address XX.XXX.XXX is not on whitelist</p>    | The current IP address being used is not whitelisted                     | Check the whitelisted IP addresses on your APP’s settings                                   |
| <p>code:-32004</p><p>message: method xxx does not support</p>                   | The method is not allowed to you                                         | Upgrade plan                                                                                |
| <p>code: -32005</p><p>message: batch size exceed limit 500</p>                  | Occurs when hitting the 500 requests limitation in a batch call          | Limit the number of requests in a batch call (<500)                                         |
| <p>code: -32005</p><p>message: ran out of cu</p>                                | Occurs when CU runs out                                                  | Upgrade plan or buy more CUs                                                                |
| <p>code: -32600</p><p>message: Invalid request</p>                              | JSON is not a valid request object                                       | Check the correct JSON at API doc section for the method being used                         |
| <p>code: -32601</p><p>message: method XXXX does not exist/is not available.</p> | Unsupported method or Unsupported clients were used when calling the API | <p>Check at the API doc section if the method is supported<br><br>Use GETH or ethclient</p> |
| <p>code: -32602<br>message: too many params / missing value</p>                 | Invalid Params                                                           | Check the correct params number and type.                                                   |
| <p>code: -32700<br>message: parse error</p>                                     | Invalid JSON                                                             | Check the correct JSON at API doc section for the method being used.                        |
