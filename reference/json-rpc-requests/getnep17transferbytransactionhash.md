---
description: Gets the Nep17 transfer by transaction hash
---

# GetNep17TransferByTransactionHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="TransactionHash" required="true" %}
the transaction hash
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Limit" %}
the number of items to return 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Skip" %}
the number of items to skip
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "_id": "614bf1d8a14111843552cae1",
                "blockhash": "0x8d0fffcc1938987c01b460ddcbd6c9fc01a9b83300d07c3cd680e4036b680dfc",
                "contract": "0xef4073a0f2b305a38ec4050e4d3d28bc40ea63f5",
                "decimals": 0,
                "from": "0xeba621d37ff117d9ce73c1579bf260aa779cb392",
                "frombalance": "79000000",
                "timestamp": 1627027447114,
                "to": "0x0bf916d727c75f2e51e1ab2c476304513da59701",
                "tobalance": "3000000",
                "tokenname": "NeoToken",
                "txid": "0x237aae2efdb459ade601d07db39b1b0134c19b40912933414217bc1494cd009b",
                "value": "1000000",
                "vmstate": "HALT"
            },
            {
                "_id": "614bf1d8a14111843552cae2",
                "blockhash": "0x8d0fffcc1938987c01b460ddcbd6c9fc01a9b83300d07c3cd680e4036b680dfc",
                "contract": "0xd2a4cff31913016155e38e474a2c06d08be276cf",
                "decimals": 8,
                "from": null,
                "frombalance": "0",
                "timestamp": 1627027447114,
                "to": "0xeba621d37ff117d9ce73c1579bf260aa779cb392",
                "tobalance": "5099945401484000",
                "tokenname": "GasToken",
                "txid": "0x237aae2efdb459ade601d07db39b1b0134c19b40912933414217bc1494cd009b",
                "value": "451280000000",
                "vmstate": "HALT"
            }
        ],
        "totalCount": 3
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
  "method": "GetNep17TransferByTransactionHash",
  "params": {"TransactionHash": "0x237aae2efdb459ade601d07db39b1b0134c19b40912933414217bc1494cd009b","Limit":2},
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
    "method": "GetNep17TransferByTransactionHash",
    "params": {
      "TransactionHash": "0x237aae2efdb459ade601d07db39b1b0134c19b40912933414217bc1494cd009b",
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
