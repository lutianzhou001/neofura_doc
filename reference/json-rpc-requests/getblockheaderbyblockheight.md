---
description: Gets the blockheader by the blockheight
---

# GetBlockHeaderByBlockHeight

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="BlockHeight" type="int" required="true" %}
the blockheight
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "_id": "614bef0ea14111843551a810",
        "hash": "0x9d3276785e7306daf59a3f3b9e31912c095598bbfb8a4476b821b0e59be4c57a",
        "index": 0,
        "merkleroot": "0x0000000000000000000000000000000000000000000000000000000000000000",
        "nextConsensus": "0xeba621d37ff117d9ce73c1579bf260aa779cb392",
        "prevhash": "0x0000000000000000000000000000000000000000000000000000000000000000",
        "primaryindex": 0,
        "size": 113,
        "timestamp": 1468595301000,
        "version": 0,
        "witnesses": [
            {
                "invocation": "",
                "verification": "EQ=="
            }
        ]
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
    "id": 1,
    "params": {"BlockHeader":"555"},
    "method": "GetBlockHeaderByBlockHeight"
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
    "id": 1,
    "params": {
      "BlockHeader": "555"
    },
    "method": "GetBlockHeaderByBlockHeight"
  })

};
request(options, function (error, response) {
  if (error) throw new Error(error);
  console.log(response.body);
});

```
{% endtab %}
{% endtabs %}
