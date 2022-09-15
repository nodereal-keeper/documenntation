---
description: This document helps you to understand how JWT works in MegaNode
---

# JSON Web Token (JWT)

## What is JSON Web Token?

JSON Web Token (JWT) is an open, industry standard [RFC 7519](https://tools.ietf.org/html/rfc7519) method for representing claims securely between two parties. You can enable JWT in MegaNode and send requests with JWT to ensure only authorized requests are available.

## How to use it?

It's easy to enable JWT and send requests with JWT in MegaNode, you just need to follow the below instructions:

### Generate RSA-256 keys

Generate your own RSA-256 public and private key with 2048 length. Below is the example using [OpenSSL](https://www.openssl.org/).

```
# generate rsa key
openssl genrsa -out jwtRSA256-private.pem 2048
openssl rsa -in jwtRSA256-private.pem -pubout -outform PEM -out jwtRSA256-public.pem
```

### Enable JWT in MegaNode

* Login -> Dashboard -> Account
* Enable the JTW and input the public key generated in previous step.
* You will get the public key ID after clicking "Add"

![Enable JWT & input the public key](<../.gitbook/assets/Screen Shot 2022-07-04 at 11.06.14.png>)

![Get a system-generated key ID after adding public key](<../.gitbook/assets/Screen Shot 2022-07-07 at 16.27.58.png>)

### Generate the JWT

Once you've enabled the JWT, it's required to add the JWT in all the requests header. Below is the example of generating JWT using [https://jwt.io/](https://jwt.io/)

You need HEADER, PAYLOAD, & SIGNATURE to generate a JWT.

**Header**

| Field | Description                      | Example                              |
| ----- | -------------------------------- | ------------------------------------ |
| alg   | The signing algorithm being used | RS256                                |
| typ   | The type of the token            | JWT                                  |
| kid   | The key id from MegaNode         | 10e03c88-098d-47cb-b451-a67f2137fqcf |



You can use your terminal to encode the header.

```
# To encode a header
header=`echo -n '{"alg": "RS256","typ": "JWT","kid": "c6a5278e-ce1d-4f54-b7fa-f8d90f8b5756"}' | base64 | sed s/\+/-/ | sed -E s/=+$//`
```

**Payload**

| Field | Description                                                                                  | Example     |
| ----- | -------------------------------------------------------------------------------------------- | ----------- |
| aud   | The audience of this JWT                                                                     | nodereal.io |
| exp   | The expiry time. It should be  no later than current time + 24 hours. Unix timestamp format. | 1656907527  |

{% hint style="info" %}
You can convert a human-readable timestamp to epoch by command below.&#x20;

date -j -f "%Y-%m-%d %H:%M:%S" "2022-07-10 15:58:50" "+%s"

Make sure your expiration time is no longer than current time + 24 hours.
{% endhint %}

You can encode your payload by command below.

```
#To encode a payload
payload=`echo -n '{"aud": "nodereal.io","exp": "1657461530"}' | base64 | sed s/\+/-/ | sed -E s/=+$//`
```

**Signature**

To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

```
# To encode a signature
sig=`echo -n "$header.$payload" | openssl dgst -sha256 -binary -sign jwtRSA256-private.pem  | openssl enc -base64 | tr -d '\n=' | tr -- '+/' '-_'`
```

**JWT**

Your JWT is the combination of your encoded header.payload.signature.&#x20;

```
# JWT = header.payload.signature
jwt=`echo $header.$payload.$sig`
echo $jwt
```

Verify your jwt by the debugger.

![](<../.gitbook/assets/Screen Shot 2022-07-07 at 19.21.11.png>)

### Send request with JWT

After generating the JWT, you would need to add the JWT as a part of your request header `-H "Authorization: Bearer` entry.

```
curl -X POST \
-H "Content-Type: application/json" \
-H "Authorization: Bearer $jwt" \
--data '{"jsonrpc": "2.0", "id": 1, "method": "eth_blockNumber", "params": []}' \
"https://bsc-mainnet.nodereal.io/v1/<YOUR-API-KEY>"
```



## What if the JWT is incorrect ?

If you have enabled the JWT but sending requests without JWT or with incorrect JWT, you will receive a http 401 error status code and also below response.

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "error": {
        "code": -32002,
        "message": "This function is unavailable due to security setting."
    }
}
```

You should either disable the JWT setting or send requests with correct JWT.



## Do you support key rotation?

Yes, MegaNode now support up to 3 keys, you could rotate your key by uploading a new one.



## Reference

You can also check how to encrypt & sign the payload with the keys on github repo [here](https://github.com/node-real/community\_kb/blob/main/node/JWT.md).

