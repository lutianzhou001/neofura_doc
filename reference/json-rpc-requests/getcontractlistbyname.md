---
description: Gets the contract list by name (fuzzy search supported)
---

# GetContractListByName

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Name" required="true" %}
the contract name
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Limit" type="int" %}
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
                "Transaction": [
                    {
                        "sender": "NTAv9Q5p9Vsckku56sbWSHQBkg3c5ntBk1"
                    }
                ],
                "createtime": 1631174537099,
                "hash": "0x89d9839aa840a0bc55b64501faeac3ab037f471d",
                "id": 142,
                "name": "PriceFeedService",
                "updatecounter": 0
            },
            {
                "Transaction": [
                    {
                        "sender": "NN38jUtTP68pBjUx1pXEAFbZqU9anjqGT1"
                    }
                ],
                "createtime": 1631165194829,
                "hash": "0xd30ed1c087d8b8077275f2c7be90f80b5a9c5d8d",
                "id": 137,
                "name": "PriceFeedService",
                "updatecounter": 0
            }
        ],
        "totalCount": 2
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
  "method": "GetContractListByName",
  "params": {"Name":"PriceFeedService"},
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
    "method": "GetContractListByName",
    "params": {
      "Name": "PriceFeedService"
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
