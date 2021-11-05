---
description: Gets the vm state by transaction hash
---

# GetVmStateByTransactionHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="TransactionHash" required="true" %}
the transaction hash
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "vmstate": "HALT"
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
  "method": "GetVmStateByTransactionHash",
  "params": {"TransactionHash":"0xa15ed65858d1e73a45c5f0f9d29462fe00e1d608a8f471a293eeda80ac28294b"},
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
    "method": "GetVmStateByTransactionHash",
    "params": {
      "TransactionHash": "0xa15ed65858d1e73a45c5f0f9d29462fe00e1d608a8f471a293eeda80ac28294b"
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
