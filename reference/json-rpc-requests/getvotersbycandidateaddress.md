---
description: Gets the voters by candidate address
---

# GetVotersByCandidateAddress

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="CandidateAddress" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="Limit" type="Int" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="Skip" type="Int" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "_id": "614befeda141118435522031",
                "balanceOfVoter": "3000000",
                "blockNumber": 15181,
                "candidate": "0x0bf916d727c75f2e51e1ab2c476304513da59701",
                "candidatePubKey": "023e9b32ea89b94d066e649b124fd50e396ee91369e8e2a6ae1b11c170d022256d",
                "lastTransferTxid": "0x237aae2efdb459ade601d07db39b1b0134c19b40912933414217bc1494cd009b",
                "lastVoteTxid": "0x3d07e51614efd0d6eeeb1de7da6ce5b2f1db61a901e10b9c6715de5add0888fc",
                "voter": "0x0bf916d727c75f2e51e1ab2c476304513da59701"
            },
            {
                "_id": "614bfbb0a141118435598ed3",
                "balanceOfVoter": "0",
                "blockNumber": 66226,
                "candidate": "0x0bf916d727c75f2e51e1ab2c476304513da59701",
                "candidatePubKey": "023e9b32ea89b94d066e649b124fd50e396ee91369e8e2a6ae1b11c170d022256d",
                "lastTransferTxid": null,
                "lastVoteTxid": "0xa5f3d1c819865d74bd0c0562df5899f22a318bf411e924a407a304221a16b097",
                "voter": "0x1fbd5663d504c4ee04eef89548c8b4953550c67d"
            }
        ],
        "totalCount": 12
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
  "method": "GetVotersByCandidateAddress",
  "params": {"CandidateAddress":"0x0bf916d727c75f2e51e1ab2c476304513da59701","Limit":2},
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
    "method": "GetVotersByCandidateAddress",
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
