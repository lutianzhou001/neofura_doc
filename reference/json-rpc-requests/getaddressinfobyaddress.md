---
description: Get the address info by the address
---

# GetAddressInfoByAddress

### API Format

{% swagger method="post" path="://testneofura.ngd.network:444" baseUrl="https" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Address" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "_id": "614bef0ea14111843551a800",
        "address": "0x0bf916d727c75f2e51e1ab2c476304513da59701",
        "firstusetime": 1468595301000,
        "lastusetime": 1627572748907,
        "transactionssent": 10
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
  "method": "GetAddressInfoByAddress",
  "params": {"Address":"0x0bf916d727c75f2e51e1ab2c476304513da59701"},
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
    "method": "GetAddressInfoByAddress",
    "params": {
      "Address": "0x0bf916d727c75f2e51e1ab2c476304513da59701"
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
