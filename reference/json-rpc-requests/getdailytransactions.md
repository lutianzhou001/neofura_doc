---
description: Gets the daily transaction counts in last several days
---

# GetDailyTransactions

### API Format

{% swagger method="post" path=":444" baseUrl="https://testneofura.ngd.network" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Days" type="int" %}
transactions in the last days
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": [
        {
            "DailyTransactions": 98,
            "_id": "6135961f8fb1d7b4f1f4bce9"
        },
        {
            "DailyTransactions": 128,
            "_id": "6136ab808fb1d7b4f1f4bd29"
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
  "method": "GetDailyTransactions",
  "params": {"Days":2},
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
    "method": "GetDailyTransactions",
    "params": {
      "Days": 2
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
