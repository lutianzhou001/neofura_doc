---
description: Gets the total sent and received amount by contract hash
---

# GetTotalSentAndReceivedByContractHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" required="true" name="ContractHash" %}
the contract scirpt hash
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Address" required="true" %}
the user's address
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "Address": "0xfa03cb7b40072c69ca41f0ad3606a548f1d59966",
        "ContractHash": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
        "received": 2439410926498,
        "sent": 2028508871288
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
  "method": "GetTotalSentAndReceivedByContractHashAddress",
  "params": {"ContractHash":"0xd2a4cff31913016155e38e474a2c06d08be276cf","Address":"0xfa03cb7b40072c69ca41f0ad3606a548f1d59966"},
  "id": 1
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
    "method": "GetTotalSentAndReceivedByContractHashAddress",
    "params": {
      "ContractHash": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
      "Address": "0xfa03cb7b40072c69ca41f0ad3606a548f1d59966"
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

