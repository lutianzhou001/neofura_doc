---
description: Gets the cumulative systemFee burn in total and last 10 blocks systemFee burn
---

# GetCumulativeFeeBurn

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```
{
    "id": 1,
    "result": [
        {
            "_id": "",
            "feeburn": 4438971290893,
            "result": [
                {
                    "index": 484849,
                    "systemFee": 0
                },
                {
                    "index": 484848,
                    "systemFee": 0
                },
                {
                    "index": 484847,
                    "systemFee": 0
                },
                {
                    "index": 484846,
                    "systemFee": 0
                },
                {
                    "index": 484845,
                    "systemFee": 0
                },
                {
                    "index": 484844,
                    "systemFee": 0
                },
                {
                    "index": 484843,
                    "systemFee": 0
                },
                {
                    "index": 484842,
                    "systemFee": 997775
                },
                {
                    "index": 484841,
                    "systemFee": 0
                },
                {
                    "index": 484840,
                    "systemFee": 0
                }
            ]
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
  "method": "GetCumulativeFeeBurn",
  "params": {},
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
    "method": "GetCumulativeFeeBurn",
    "params": {},
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
