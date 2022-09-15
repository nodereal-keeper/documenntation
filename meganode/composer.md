---
description: The step-by-step instructions for submitting your first request using Composer
---

# Composer

After you have created your first app in MegaNode, it's the time to make your first RPC request. You can use any REST API testing tool, e.g. Postman, to test your MegaNode JSON-RPC request. However, there's a built-in tool in our portal to make things easier.

## Find Composer

You can very easily find the Composer from the drop-down menu. It's a built-in free tool on MegaNode to test every supported JSON-RPC method.

![Find Composer from the menu](<../.gitbook/assets/Screen Shot 2022-04-27 at 19.24.45.png>)

## Configure Request

Composer consists of two parts i.e. Configure Request and Request Result. Configure Request is where you can choose your app and the method you want to test. If you cannot find any app from the menu, please go to [create your first app](https://docs.nodereal.io/nodereal/meganode/getting-started#create-your-first-app).

![Composer](<../.gitbook/assets/Screen Shot 2022-04-27 at 19.41.20.png>)

* **App**: List of the apps you created.
* **Method**: List of supported JSON-RPC method.
* **Params**: If you selected a method with params, you will see some additional text fields required to input. Please ensure you've input all necessary params before sending the request.&#x20;

![Additional params required for input](<../.gitbook/assets/Screen Shot 2022-04-27 at 20.01.51.png>)

## Send Request

Once you have input all the required params, the Preview will show you the request content you composed. Also, the "Send Request" button will become available, which you can simply click on to send the request.

![Example of request](<../.gitbook/assets/Screen Shot 2022-04-27 at 20.22.51.png>)

{% hint style="info" %}
Please note that all the requests you've sent will cost you the CU accordingly. See [what is CU and how does it work](compute-units-cus.md).
{% endhint %}

## Request Result

After you send a request, you can easily find the result from the Response.

![Result of your request](<../.gitbook/assets/Screen Shot 2022-04-27 at 20.24.26.png>)

{% hint style="info" %}
Archive data is also available in Composer as long as you submit a historical block number.
{% endhint %}

Composer is an easy, simple and straightforward tool for you to test the JSON-RPC request. Please go create your first app and send the request to enjoy the fastest blockchain infrastructure service!

