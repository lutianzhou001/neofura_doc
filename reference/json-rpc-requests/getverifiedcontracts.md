---
description: Gets the verified contract
---

# GetVerifiedContracts

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Limit" type="Int" %}
the number of results to return
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Skip" type="Int" %}
the number of results to skip
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": [
        {
            "_id": "61700825eb743bed51ae9b20",
            "hash": "0xcc5e4edd9f5f8dba8bb65734541df7a1c081c67b",
            "id": -7,
            "updatecounter": 0
        },
        {
            "_id": "61700825eb743bed51ae9b21",
            "hash": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
            "id": -6,
            "updatecounter": 0
        }
    ],
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
  "method": "GetVerifiedContracts",
  "params": {"Skip":2,"Limit":2},
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
    "method": "GetVerifiedContracts",
    "params": {
      "Skip": 2,
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
