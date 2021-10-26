---
description: Gets the blockinfos of the recent blocks
---

# GetBlockInfoList

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Limit" type="int" %}
the items limit to return
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Skip" type="int" %}
the number of items to skipitems skip to return
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "_id": "6168fe8150025b016127dd62",
                "hash": "0xc6d735b33dad4298f3397ef5d77454e68dcba064ce8897f3ac58a21e442db339",
                "index": 483825,
                "size": 697,
                "timestamp": 1634270848950,
                "transactioncount": 0
            },
            {
                "_id": "6168fe7150025b016127dd59",
                "hash": "0x5c877b9fd7b87955ad98ec63cb843164e04bd92fae5ca88e5a35eb339d47bbcc",
                "index": 483824,
                "size": 697,
                "timestamp": 1634270833849,
                "transactioncount": 0
            }
        ],
        "totalCount": 483826
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
  "method": "GetBlockInfoList",
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
    "method": "GetBlockInfoList",
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
