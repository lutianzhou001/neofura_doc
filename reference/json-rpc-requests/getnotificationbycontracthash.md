---
description: Gets the notification by contract script hash
---

# GetNotificationByContractHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ContractHash" required="true" %}

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
                "Vmstate": "HALT",
                "_id": "61712d40770c0b0a6a3ceb24",
                "blockhash": "0xcfab421df7e15976a8878303bfb5cb0d5703b77a8a9c15e8a33cb82c49a9a5db",
                "contract": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "eventname": "Transfer",
                "index": 0,
                "state": {
                    "type": "Array",
                    "value": [
                        {
                            "type": "Any",
                            "value": null
                        },
                        {
                            "type": "ByteString",
                            "value": "ZlPI6+wR2Aei/ElqjviDj9PpLeU="
                        },
                        {
                            "type": "Integer",
                            "value": "50000000"
                        }
                    ]
                },
                "timestamp": 1634807103949,
                "txid": "0x0000000000000000000000000000000000000000000000000000000000000000"
            },
            {
                "Vmstate": "HALT",
                "_id": "61712d3050025b01612b7efb",
                "blockhash": "0xbab929e8de4cd215eb6244e5ef17ce4b128234362a9e00d2cbbf83a11383156f",
                "contract": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "eventname": "Transfer",
                "index": 0,
                "state": {
                    "type": "Array",
                    "value": [
                        {
                            "type": "Any",
                            "value": null
                        },
                        {
                            "type": "ByteString",
                            "value": "lPAUr0QjnhYz8fCJaBQQm47mzIU="
                        },
                        {
                            "type": "Integer",
                            "value": "50000000"
                        }
                    ]
                },
                "timestamp": 1634807088845,
                "txid": "0x0000000000000000000000000000000000000000000000000000000000000000"
            }
        ],
        "totalCount": 593943
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
  "method": "GetNotificationByContractHash",
  "params": {"ContractHash":"0xd2a4cff31913016155e38e474a2c06d08be276cf","Limit":2},
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
    "method": "GetNotificationByContractHash",
    "params": {
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
