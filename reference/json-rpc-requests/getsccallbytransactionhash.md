---
description: Gets the ScCall by transaction hash
---

# GetScCallByTransactionHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="TransactionHash" required="true" %}
the transaction hash
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Limit" type="Int" %}
the number of items to return 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Skip" type="Int" %}
the number of items to skip
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "_id": "614befe9a141118435521f25",
                "callFlags": "All",
                "contractHash": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "hexStringParams": [
                    "92b39c77aa60f29b57c173ced917f17fd321a6eb",
                    "812be7a7082c9842fc2acefa4118b8bc5a5b918b",
                    "00e8764817000000",
                    ""
                ],
                "method": "transfer",
                "originSender": "0xeba621d37ff117d9ce73c1579bf260aa779cb392",
                "txid": "0x88142a83918d35f30930dc88e370e69db5c9573acf2010a8e0aa5b2094094020"
            },
            {
                "_id": "614befe9a141118435521f43",
                "callFlags": "All",
                "contractHash": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "hexStringParams": [
                    "92b39c77aa60f29b57c173ced917f17fd321a6eb",
                    "b14858f18c76837415a61521c9cf69776e751f55",
                    "00e8764817000000",
                    ""
                ],
                "method": "transfer",
                "originSender": "0xeba621d37ff117d9ce73c1579bf260aa779cb392",
                "txid": "0x4b4df96e27b2d763ebbf3f89b422c2f9f3eccc863f422dcda7e2f36c936d0bbd"
            }
        ],
        "totalCount": 6
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
  "method": "GetScCallByContractHashAddress",
  "params": {"Address":"0xeba621d37ff117d9ce73c1579bf260aa779cb392","ContractHash":"0xd2a4cff31913016155e38e474a2c06d08be276cf","Limit":2},
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
    "method": "GetScCallByContractHashAddress",
    "params": {
      "Address": "0xeba621d37ff117d9ce73c1579bf260aa779cb392",
      "ContractHash": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
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
