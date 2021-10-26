---
description: Gets the candidate by the candidate address
---

# GetCandidateByAddress

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Address" required="true" %}
the candidate address
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "_id": "614bef0ea14111843551a820",
        "candidate": "0xaa606e99a6d1cb45ba34872864a3578c8a668143",
        "isCommittee": true,
        "state": true,
        "votesOfCandidate": "2006803"
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
curl --location --request GET 'https://testneofura.ngd.network:444' \
--header 'Content-Type: application/json' \
--data-raw '{
    "jsonrpc": "2.0",
    "method": "GetCandidateByAddress",
    "params": {"Address": "0xaa606e99a6d1cb45ba34872864a3578c8a668143"},
    "id": 1
}'
```
{% endtab %}

{% tab title="Nodejs" %}
```
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://testneofura.ngd.network:444',
  'headers': {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    "jsonrpc": "2.0",
    "method": "GetCandidateByAddress",
    "params": {
      "Address": "0xaa606e99a6d1cb45ba34872864a3578c8a668143"
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
