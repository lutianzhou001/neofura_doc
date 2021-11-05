---
description: Gets the verified contract by contract hash
---

# GetVerifiedContractByContractHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ContractHash" required="true" %}
the contract script hash
{% endswagger-parameter %}

{% swagger-parameter in="body" name="UpdateCounter" type="int" %}
update counts of a certain contract
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "_id": "61700825eb743bed51ae9b1e",
        "hash": "0xfe924b7cfe89ddd271abaf7210a80a7e11178758",
        "id": -9,
        "updatecounter": 0
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
  "method": "GetVerifiedContractByContractHash",
  "params": {"ContractHash":"0xfe924b7cfe89ddd271abaf7210a80a7e11178758","UpdateCounter":0},
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
    "method": "GetVerifiedContractByContractHash",
    "params": {
      "ContractHash": "0xfe924b7cfe89ddd271abaf7210a80a7e11178758",
      "UpdateCounter": 0
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
