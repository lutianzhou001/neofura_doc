---
description: Gets the committee of the blockchain
---

# GetCommittee

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Limit" type="int" required="false" %}
the number of items to return  
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Skip" type="int" %}
the number of items to skip
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "_id": "614bef0ea14111843551a811",
                "candidate": "0x8b915b5abcb81841face2afc42982c08a7e72b81",
                "isCommittee": true,
                "state": true,
                "votesOfCandidate": "2000000"
            },
            {
                "_id": "614bef0ea14111843551a812",
                "candidate": "0xa4887b48371fe7727d9f96f4922f464c9c457d89",
                "isCommittee": true,
                "state": true,
                "votesOfCandidate": "2000000"
            }
        ],
        "totalCount": 21
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
  "method": "GetCommittee",
  "params": {"Limit":2},
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
    "method": "GetCommittee",
    "params": {
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
