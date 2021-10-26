---
description: Gets the asset info by the contact script hash
---

# GetAssetInfoByContractHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ContractHash" required="true" %}
contract script hash
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "_id": "614bf199306693834466ba2e",
        "decimals": 18,
        "firsttransfertime": 1627006322319,
        "hash": "0x38a2aace91f92b979207c0dd50a857c117d4785b",
        "holders": 13,
        "ispopular": false,
        "symbol": "fWETH",
        "tokenname": "Nep17Contract",
        "totalsupply": "100000000000000000000000000",
        "type": "Unknown"
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
  "method": "GetAssetInfoByContractHash",
  "params": {"ContractHash":"0x38a2aace91f92b979207c0dd50a857c117d4785b"},
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
    "method": "GetAssetInfoByContractHash",
    "params": {
      "ContractHash": "0x38a2aace91f92b979207c0dd50a857c117d4785b"
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
