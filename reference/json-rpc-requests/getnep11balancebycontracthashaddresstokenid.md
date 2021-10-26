---
description: >-
  Gets the Nep11 balance by contract script hash user's address and tokenId of
  the Nep11 standard
---

# GetNep11BalanceByContractHashAddressTokenId

### API Format

{% swagger method="post" path="" baseUrl="" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ContractHash" required="true" %}
contract script hash
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Address" required="true" %}
user's address
{% endswagger-parameter %}

{% swagger-parameter in="body" name="TokenId" required="true" %}
tokenId of the Nep11 standard
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "_id": "614bf99ba14111843558cb34",
        "address": "0x2e9a0e6a68a4acce23ca14408bb4d0b803425394",
        "asset": "0xb3b65e5c0d2af3f98cac6e80083f6c2b90476f40",
        "balance": "1",
        "tokenid": "QmxpbmQgQm94IDIxNQ=="
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
  "method": "GetNep11BalanceByContractHashAddressTokenId",
  "params": {"ContractHash": "0xb3b65e5c0d2af3f98cac6e80083f6c2b90476f40","Address":"0x2e9a0e6a68a4acce23ca14408bb4d0b803425394","tokenId":"QmxpbmQgQm94IDIxNQ=="},
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
    "method": "GetNep11BalanceByContractHashAddressTokenId",
    "params": {
      "ContractHash": "0xb3b65e5c0d2af3f98cac6e80083f6c2b90476f40",
      "Address": "0x2e9a0e6a68a4acce23ca14408bb4d0b803425394",
      "tokenId": "QmxpbmQgQm94IDIxNQ=="
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
