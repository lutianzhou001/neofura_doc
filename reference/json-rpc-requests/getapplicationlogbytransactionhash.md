---
description: Gets the applicationlog by transactionhash
---

# GetApplicationLogByTransactionHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="TransactionHash" required="true" %}
transactionhash
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "_id": "614befd9a1411184355217d2",
        "blockhash": "0xcf35068b43281d700c6c7fc160ab844e74afeda08e793d061bbd1bc1a1203bd4",
        "exception": null,
        "gasconsumed": 9977780,
        "notifications": [
            {
                "Vmstate": "HALT",
                "_id": "614befd9a1411184355217d5",
                "blockhash": "0xcf35068b43281d700c6c7fc160ab844e74afeda08e793d061bbd1bc1a1203bd4",
                "contract": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "eventname": "Transfer",
                "index": 0,
                "state": {
                    "type": "Array",
                    "value": [
                        {
                            "type": "ByteString",
                            "value": "krOcd6pg8ptXwXPO2Rfxf9Mhpus="
                        },
                        {
                            "type": "ByteString",
                            "value": "wJjkrPCyCQ3Rbss9WN5CaocVhRs="
                        },
                        {
                            "type": "Integer",
                            "value": "100000000000000"
                        }
                    ]
                },
                "timestamp": 1626850227986,
                "txid": "0x85b55479fc43668077821234f547824d3111343aec21988f8c0aa1ff9b2ee287"
            }
        ],
        "timestamp": 1626850227986,
        "trigger": "Application",
        "txid": "0x85b55479fc43668077821234f547824d3111343aec21988f8c0aa1ff9b2ee287",
        "vmstate": "HALT"
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
  "method": "GetApplicationLogByTransactionHash",
  "params": {"TransactionHash": "0x85b55479fc43668077821234f547824d3111343aec21988f8c0aa1ff9b2ee287" },
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
    "method": "GetApplicationLogByTransactionHash",
    "params": {
      "TransactionHash": "0x85b55479fc43668077821234f547824d3111343aec21988f8c0aa1ff9b2ee287"
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
