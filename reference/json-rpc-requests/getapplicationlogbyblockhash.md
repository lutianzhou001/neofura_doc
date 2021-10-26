---
description: Gets the applicationlog by blockhash
---

# GetApplicationLogByBlockHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="BlockHash" required="true" %}
blockhash of a transaction
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
                "_id": "614befe4a141118435521a3d",
                "blockhash": "0xf6ba8db5c013834890903a30a4ce0d65ec5da2addaf4799f15efbedaff42c56f",
                "exception": null,
                "gasconsumed": 0,
                "notifications": [
                    {
                        "Vmstate": "HALT",
                        "_id": "614befe4a141118435521a3f",
                        "blockhash": "0xf6ba8db5c013834890903a30a4ce0d65ec5da2addaf4799f15efbedaff42c56f",
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
                                    "value": "gSvnpwgsmEL8Ks76QRi4vFpbkYs="
                                },
                                {
                                    "type": "Integer",
                                    "value": "50000000"
                                }
                            ]
                        },
                        "timestamp": 1626851177411,
                        "txid": "0x0000000000000000000000000000000000000000000000000000000000000000"
                    }
                ],
                "timestamp": 1626851177411,
                "trigger": "PostPersist",
                "txid": "0x0000000000000000000000000000000000000000000000000000000000000000",
                "vmstate": "HALT"
            },
            {
                "_id": "614befe4a141118435521a3e",
                "blockhash": "0xf6ba8db5c013834890903a30a4ce0d65ec5da2addaf4799f15efbedaff42c56f",
                "exception": null,
                "gasconsumed": 0,
                "notifications": [
                    {
                        "Vmstate": "HALT",
                        "_id": "614befe4a141118435521a3f",
                        "blockhash": "0xf6ba8db5c013834890903a30a4ce0d65ec5da2addaf4799f15efbedaff42c56f",
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
                                    "value": "gSvnpwgsmEL8Ks76QRi4vFpbkYs="
                                },
                                {
                                    "type": "Integer",
                                    "value": "50000000"
                                }
                            ]
                        },
                        "timestamp": 1626851177411,
                        "txid": "0x0000000000000000000000000000000000000000000000000000000000000000"
                    }
                ],
                "timestamp": 1626851177411,
                "trigger": "OnPersist",
                "txid": "0x0000000000000000000000000000000000000000000000000000000000000000",
                "vmstate": "HALT"
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
  "method": "GetApplicationLogByBlockHash",
  "params": {"BlockHash": "0xf6ba8db5c013834890903a30a4ce0d65ec5da2addaf4799f15efbedaff42c56f" },
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
    "method": "GetApplicationLogByBlockHash",
    "params": {
      "BlockHash": "0xf6ba8db5c013834890903a30a4ce0d65ec5da2addaf4799f15efbedaff42c56f"
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
