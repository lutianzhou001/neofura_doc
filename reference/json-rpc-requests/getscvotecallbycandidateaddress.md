---
description: Gets the scvote call by candidate address
---

# GetScVoteCallByCandidateAddress

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="CandidateAddress" required="true" %}
the candidate's address
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Skip" type="Int" %}
the number of results to skip
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Limit" type="Int" %}
the number of results to return  // Response
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "_id": "617009dacd1d7cf225a4744b",
                "blockNumber": 3957,
                "candidate": "0x0bf916d727c75f2e51e1ab2c476304513da59701",
                "candidatePubKey": "023e9b32ea89b94d066e649b124fd50e396ee91369e8e2a6ae1b11c170d022256d",
                "txid": "0x3d07e51614efd0d6eeeb1de7da6ce5b2f1db61a901e10b9c6715de5add0888fc",
                "voter": "0x0bf916d727c75f2e51e1ab2c476304513da59701"
            },
            {
                "_id": "61701465cd1d7cf225a5b3e2",
                "blockNumber": 26938,
                "candidate": "0x0bf916d727c75f2e51e1ab2c476304513da59701",
                "candidatePubKey": "023e9b32ea89b94d066e649b124fd50e396ee91369e8e2a6ae1b11c170d022256d",
                "txid": "0x0f57656d2dd1bb5fc1b63f8c68b2ea156ffa23489d4fbf80d47b5f809aacb387",
                "voter": "0xd37794031f283a064abd155d610a80ef844d375d"
            }
        ],
        "totalCount": 34
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
  "method": "GetScVoteCallByCandidateAddress",
  "params": {"CandidateAddress":"0x0bf916d727c75f2e51e1ab2c476304513da59701","Limit":2},
  "id": 1
}'
```
{% endtab %}

{% tab title="Node.js" %}
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
    "method": "GetScVoteCallByCandidateAddress",
    "params": {
      "CandidateAddress": "0x0bf916d727c75f2e51e1ab2c476304513da59701",
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
