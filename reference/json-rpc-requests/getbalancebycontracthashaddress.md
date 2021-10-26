---
description: Gets the asset balance by the asset contract script hash and user's address
---

# GetBalanceByContractHashAddress

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ContractHash" required="true" %}
asset contract script hash
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Address" required="true" %}
user's address
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "_id": "614bf1c8306693834466cd91",
        "address": "0x96d5942028891de8e5d866f504b36ff5ae13ab63",
        "asset": "0xef4073a0f2b305a38ec4050e4d3d28bc40ea63f5",
        "balance": "43",
        "tokenid": ""
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
  "method": "GetBalanceByContractHashAddress",
  "params": {"Address":"NUzy2Ns2D35BTdFVqDhUCRoZb1cmix2cXS","ContractHash":"0xef4073a0f2b305a38ec4050e4d3d28bc40ea63f5"},
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
    "method": "GetBalanceByContractHashAddress",
    "params": {
      "Address": "NUzy2Ns2D35BTdFVqDhUCRoZb1cmix2cXS",
      "ContractHash": "0xef4073a0f2b305a38ec4050e4d3d28bc40ea63f5"
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
