---
description: Gets the Nep17 transfer by contract script hash
---

# GetNep17TransferByContractHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ContractHash" required="true" %}
the contract script hash
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Limit" type="int" %}
the number of items to return 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Skip" type="int" %}
the number of items to skip
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "_id": "617124c450025b01612b7b84",
                "blockhash": "0x663d48067d4041734ce63e0cb373a85520f0c8fad4e278234af8d7ba242e53bc",
                "contract": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "from": null,
                "frombalance": "0",
                "timestamp": 1634804931955,
                "to": "0xa8baabcbed1ed250e3d55a5999684a74c5f49b90",
                "tobalance": "1197375108790",
                "txid": "0x0000000000000000000000000000000000000000000000000000000000000000",
                "value": "50000000",
                "vmstate": "HALT"
            },
            {
                "_id": "617124b450025b01612b7b7b",
                "blockhash": "0x7439369cc6f5f2a98dbd5d854940f1cd85edc86969bcb45964d9b42e5120dcd7",
                "contract": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "from": null,
                "frombalance": "0",
                "timestamp": 1634804916868,
                "to": "0x96b9b57bb0a68e3a3c6713f526a8c64aabe35cfa",
                "tobalance": "1297631334825",
                "txid": "0x0000000000000000000000000000000000000000000000000000000000000000",
                "value": "50000000",
                "vmstate": "HALT"
            }
        ],
        "totalCount": 593447
    },
    "error": null
}
```
{% endswagger-response %}
{% endswagger %}

### Requests

{% tabs %}
{% tab title="cURL" %}
```
curl --location --request POST 'https://testneofura.ngd.network:444' \
--header 'Content-Type: application/json' \
--data-raw '{
    "jsonrpc":"2.0",
    "method":"GetNep17TransferByContractHash",
    "params":{"ContractHash":"0xd2a4cff31913016155e38e474a2c06d08be276cf","Limit":2},
    "id":1
}'
```
{% endtab %}

{% tab title="Nodejs" %}
```
var request = require('request');
var options = {
  'method': 'POST',
  'url': 'https://testneofura.ngd.network:444',
  'headers': {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    "jsonrpc": "2.0",
    "method": "GetNep17TransferByContractHash",
    "params": {
      "ContractHash": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
      "Limit": 2
    },
    "id": 1
  })

};
request(options, function (error, response) {
  if (error) throw new Error(error);
  console.log(response.body);
});
```
{% endtab %}
{% endtabs %}
