---
description: Gets the execution by trigger
---

# GetExecutionByTrigger

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Trigger" required="true" type="enum" %}
Triggers in OnPersist,PostPersist,Application,Verification,System,All
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
                "_id": "614befd9a1411184355217d2",
                "blockhash": "0xcf35068b43281d700c6c7fc160ab844e74afeda08e793d061bbd1bc1a1203bd4",
                "exception": null,
                "gasconsumed": 9977780,
                "timestamp": 1626850227986,
                "trigger": "Application",
                "txid": "0x85b55479fc43668077821234f547824d3111343aec21988f8c0aa1ff9b2ee287",
                "vmstate": "HALT"
            },
            {
                "_id": "614befdaa1411184355218d0",
                "blockhash": "0x59890b5eeb781f334a076383ff92c453a0c2f6194abe19a97d6bb1c66c15bd79",
                "exception": null,
                "gasconsumed": 9977780,
                "timestamp": 1626850648657,
                "trigger": "Application",
                "txid": "0x615c4c7ece85ce7d6cfe6d5f6d3495b5f46b43e298b79166488dbe431f067ca7",
                "vmstate": "HALT"
            }
        ],
        "totalCount": 35403
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
  "method": "GetExecutionByTrigger",
  "params": {"Trigger":"Application","Limit":2},
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
    "method": "GetExecutionByTrigger",
    "params": {
      "Trigger": "Application",
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
