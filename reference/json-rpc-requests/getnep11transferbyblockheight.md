---
description: Gets the Nep11 transfer by block height
---

# GetNep11TransferByBlockHeight

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="BlockHeight" type="int" required="true" %}
the block height
{% endswagger-parameter %}

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
                "_id": "614bfc5f30669383446d6d2f",
                "blockhash": "0x2d3ac96785404ad370f7063db1a11f5b4018ebdd6b80754394360740bcc90c95",
                "contract": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                "from": null,
                "frombalance": "0",
                "timestamp": 1627871579237,
                "to": "0x0000000000000000000000000000000000000000",
                "tobalance": "1",
                "tokenId": "U9qaPp0ehFf6afitJ+msIqcM/3T+wEWfvFz1/HOYUzw=",
                "txid": "0x0a8809c34ff72f9ce8b670c584ed6416e1b9ad80ab678b29e400c9dc37bde6be",
                "value": "1"
            }
        ],
        "totalCount": 1
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
    "method": "GetNep11TransferByBlockHeight",
    "params": {
      "BlockHeight": 69981
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
