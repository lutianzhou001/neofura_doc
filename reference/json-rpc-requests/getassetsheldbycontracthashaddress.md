---
description: Gets the assets held by contract script hash and user's address
---

# GetAssetsHeldByContractHashAddress

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ContractHash" required="true" %}
contract script hash
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Address" required="true" %}
user's address
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "_id": "614bef0ea14111843551a804",
                "address": "0xeba621d37ff117d9ce73c1579bf260aa779cb392",
                "asset": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "balance": "5099945401484000",
                "tokenid": ""
            }
        ],
        "totalCount": 1
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
  "jsonrpc": "2.0",
  "method": "GetAssetsHeldByContractHashAddress",
  "params": {"Address":"0xeba621d37ff117d9ce73c1579bf260aa779cb392","ContractHash":"0xd2a4cff31913016155e38e474a2c06d08be276cf"},
  "id": 1
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
    "method": "GetAssetsHeldByContractHashAddress",
    "params": {
      "Address": "0xeba621d37ff117d9ce73c1579bf260aa779cb392",
      "ContractHash": "0xd2a4cff31913016155e38e474a2c06d08be276cf"
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
