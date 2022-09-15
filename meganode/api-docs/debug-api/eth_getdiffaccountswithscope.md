---
description: >-
  This API returns detailed changes of some interested accounts in a specific
  block number.
---

# eth\_getDiffAccountsWithScope

{% hint style="info" %}
Supported on BSC mainnet only.
{% endhint %}

## Parameters

* `blockNumber` - The block number in HEX format
* `ArrayofAddress` - Interested account addresses

## Returns

* `result`- detailed changes of some interested accounts in the block, which has the following fields:
  * `Number` - The block number in HEX format
  * `blockHash` - The hash of the block
  * `Transactions` - Array of DiffAccountsInTx, means the balance of interested accounts after a transaction, which has the following fields:
    * `TxHash` - hash of a transaction
    * `Accounts` - a map from address to balance of the address

## Example

#### Request

{% tabs %}
{% tab title="Curl" %}
```bash
curl https://eth-mainnet.nodereal.io/v1/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc": "2.0","id": 1,"method": "eth_getDiffAccountsWithScope","params": ["0x12dac0f",["0x4a2c860cec6471b9f5f5a336eb4f38bb21683c98","0x5a3f136feec05d5481d8150cec35e0fc32bff468","0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c","0x8aea06862f640cb4f3921e6a4e97ba5c9a992020","0x322e1a4615a232556571123024102eb9b10f6fb9","0xb28da7bc87a9dd1e60849aa7fcb5da24ea913c42","0xbc4eb8ec3e58f5ecdddce03e7142d5c261a3b21c","0x1f415eb45575c4d70e9a6fe458c3930bbbd0f524","0x5e6439554d4ae188a4935fd3e0c3a875d81d190e","0x75060656a6337c0978896adfe931b0e7c61937f7","0x2467ba56ba35e13f75b377ba2c2c0cfe3e275afa","0x8a74bc8c372bc7f0e9ca3f6ac0df51be15aec47a","0x84fc9d3e832be5f040f2cc0871862516c1b45049","0xc21cc8ec1cfb06b20ee2a58b8c9ecf190623cac3","0x390e1ba132ed9ff3394d8aa484983cc8c85f8149","0x5c8d6996d0aa618ecdc495082d421a88752afba7","0xd88f39e0811cfcc54b385e3387583b7e50b8cc48","0x721321684cb9fd2a53d2e8fd7aa4a4519685d8a2","0x5e8ce185475855e60fa121389331cd6ced61ea57","0x9a8316c0221933d03df8f653a41ab05adcea7c72","0x26193c7fa4354ae49ec53ea2cebc513dc39a10aa","0x270986629d609ad88febadd1dc17614b191e1329"]]}'
```
{% endtab %}
{% endtabs %}

#### Result

```javascript
{
	"jsonrpc": "2.0",
	"id": 0,
	"result": 
	{
		"Number":19770383,
		"BlockHash":"0xefa6d239bdd45cda401f3a779e3b9afbf02d1acd9e2c7fb7dc21c141affafcea",
		"Transactions":[
			{"TxHash":"0x035bfac98e2923430717cf7e7a80900b9fd94bf5e026c4bbfedcc80dd852edc6","Accounts":{"0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c":800000000000000,"0xd88f39e0811cfcc54b385e3387583b7e50b8cc48":-4077194000000000}},{"TxHash":"0x41a7e50d9a96adf73292fea4ed286226a044484d2b86ba56933ff79b0a1e9fa3","Accounts":{"0x5c8d6996d0aa618ecdc495082d421a88752afba7":-193395825000000}},{"TxHash":"0xc2cd62ec5f125a955d228b63513f49d688f980045eaf3d56328aba6a4bc2223c","Accounts":{"0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c":8015931622748688384}},{"TxHash":"0x94ba0ceb32cbc73941a2632b30e057ab766a884057e8a53d0f4ecb6ccbc375d2","Accounts":{"0x270986629d609ad88febadd1dc17614b191e1329":-1106080000000000}},{"TxHash":"0x253d858a7fedb0a474a618db5eba21e0afaf37b5dcb8a27c3083c8daa278e6f9","Accounts":{"0xed42315dce1cfb4384908c6a07a0bbc6b8eb0ba4":-2449995000000000}},{"TxHash":"0x3f95ec73d69307cb99b4f32c190560e056b571d8cc50d1aaf73fa69ec85daa92","Accounts":{"0x84fc9d3e832be5f040f2cc0871862516c1b45049":-1363055000000000}},{"TxHash":"0xd5533ce1656777aa8bdffbf31f86ef5570e2d95734d4678b67cc070291ae0979","Accounts":{"0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c":-120615421194208308}},{"TxHash":"0x4666ca9cfdd7e582e9c5339075d07643ea2a38d9cd7279ec3e4db3af71aa0164","Accounts":{"0xb28da7bc87a9dd1e60849aa7fcb5da24ea913c42":32546671630663,"0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c":-3715892551240070}},{"TxHash":"0x20b55ea4e0c57907b2de64615cbbab77bdf89c632efc634118d4ec4eecfa048c","Accounts":{"0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c":-11098575186580633}},{"TxHash":"0x359a7e65a44bcd0c94c57513ebc448c794a0d09cb2fb064090f809339e866db1","Accounts":{"0x1f415eb45575c4d70e9a6fe458c3930bbbd0f524":-1154570000000000}},{"TxHash":"0x28c0236a4405e2d4f115dbca3480e92a23a5cef71b08cc13aefce4c1bb8bf72c","Accounts":{"0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c":44069199735562298}},{"TxHash":"0x8e13ae37c969b27f65eeddc7254218be9df0c35f846448c6772dcfa989c25880","Accounts":{"0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c":107459979196346960}},{"TxHash":"0x652a2f551e8e5aab8d48dadc8e89d03497c4f653859488d4da4e45738fc5e211","Accounts":{"0x9a8316c0221933d03df8f653a41ab05adcea7c72":-255575000000000}}
		]
	}
}
```



