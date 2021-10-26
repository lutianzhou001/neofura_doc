---
description: Gets assets held by the user's address
---

# GetAssetHeldByAddress

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Address" required="true" %}
the user's address
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Limit" %}
the number of item to return
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Skip" %}
the number of item to skip
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
            },
            {
                "_id": "614bef0ea14111843551a802",
                "address": "0xeba621d37ff117d9ce73c1579bf260aa779cb392",
                "asset": "0xef4073a0f2b305a38ec4050e4d3d28bc40ea63f5",
                "balance": "79000000",
                "tokenid": ""
            }
        ],
        "totalCount": 2
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
  "method": "GetAssetsHeldByAddress",
  "params": {"Address":"0xeba621d37ff117d9ce73c1579bf260aa779cb392"},
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
    "method": "GetAssetsHeldByAddress",
    "params": {
      "Address": "0xeba621d37ff117d9ce73c1579bf260aa779cb392"
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
