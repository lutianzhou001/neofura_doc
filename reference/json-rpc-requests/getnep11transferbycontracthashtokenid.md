---
description: Gets the nep11 transfer by contract script hash and tokenid
---

# GetNep11TransferByContractHashTokenId

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ContractHash" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "_id": "614c1161a141118435606f33",
                "blockhash": "0x89832f94d950874d2db9d7306c3fa1483a0286a2c33f8f8e81322f095f8d7de0",
                "contract": "0x9ac0c91664ad9bbe32726094cb5f64db40b51130",
                "from": "0x03c446faee324dfa926c57261d07d0df283cb961",
                "frombalance": "0",
                "timestamp": 1629467044738,
                "to": "0x3a11aec89f04e29ae36b346ccddc3e04cd7e72b6",
                "tobalance": "1",
                "tokenId": "Hw==",
                "txid": "0x5bc7a5b4dae8070b478de5887c1553d18972749ac5045f5176439da2d7bcddd2",
                "value": "1"
            },
            {
                "_id": "614c1147a1411184356063f3",
                "blockhash": "0xddbdb6f791cc77b01466e743356b9a659c861eb0bcabe85868d7a1f2e1870f1d",
                "contract": "0x9ac0c91664ad9bbe32726094cb5f64db40b51130",
                "from": "0x3884752a244fa4c0ed3022017190d14ee4124d1d",
                "frombalance": "0",
                "timestamp": 1629459723383,
                "to": "0x03c446faee324dfa926c57261d07d0df283cb961",
                "tobalance": "1",
                "tokenId": "Hw==",
                "txid": "0xff936f40b8ba33c807c3281282989271fe3f5bd56f8687dddbb2395b7006b65c",
                "value": "1"
            },
            {
                "_id": "614c11453066938344757e05",
                "blockhash": "0xf3978643b24fd2a9c03faa91a4e2bf56abd1c3556a73bce638573ef494cae08f",
                "contract": "0x9ac0c91664ad9bbe32726094cb5f64db40b51130",
                "from": null,
                "frombalance": "0",
                "timestamp": 1629459335306,
                "to": "0x3884752a244fa4c0ed3022017190d14ee4124d1d",
                "tobalance": "1",
                "tokenId": "Hw==",
                "txid": "0xbd74efdf325dfeee5790c8723ceea7da45e45682ca51fb02c064f99e3e2ff217",
                "value": "1"
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
  "method": "GetNep11TransferByContractHashTokenId",
  "params": {"ContractHash":"0x9ac0c91664ad9bbe32726094cb5f64db40b51130","tokenId":"Hw=="},
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
    "method": "GetNep11TransferByContractHashTokenId",
    "params": {
      "ContractHash": "0x9ac0c91664ad9bbe32726094cb5f64db40b51130",
      "tokenId": "Hw=="
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
