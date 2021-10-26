---
description: Gets the extra transfer(transfer with the txid of 0) by blockhash
---

# GetExtraTransferByBlockHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="BlockHash" required="true" %}
the blockhash
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
                "_id": "614befe4a141118435521a3c",
                "blockhash": "0xf6ba8db5c013834890903a30a4ce0d65ec5da2addaf4799f15efbedaff42c56f",
                "contract": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "from": null,
                "frombalance": "0",
                "timestamp": 1626851177411,
                "to": "0x8b915b5abcb81841face2afc42982c08a7e72b81",
                "tobalance": "9151230520",
                "txid": "0x0000000000000000000000000000000000000000000000000000000000000000",
                "value": "50000000"
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
curl --location --request POST 'https://testneofura.ngd.network:444' \
--header 'Content-Type: application/json' \
--data-raw '{
  "jsonrpc": "2.0",
  "method": "GetExtraTransferByBlockHash",
  "params": {"Limit":1,"blockhash":"0xf6ba8db5c013834890903a30a4ce0d65ec5da2addaf4799f15efbedaff42c56f"},
  "id": 1
}'
```
{% endtab %}

{% tab title="Nodejs" %}
```
curl --location --request POST 'https://testneofura.ngd.network:444' \
--header 'Content-Type: application/json' \
--data-raw '{
  "jsonrpc": "2.0",
  "method": "GetExtraTransferByBlockHash",
  "params": {"Limit":1,"blockhash":"0xf6ba8db5c013834890903a30a4ce0d65ec5da2addaf4799f15efbedaff42c56f"},
  "id": 1
}'
```
{% endtab %}
{% endtabs %}
