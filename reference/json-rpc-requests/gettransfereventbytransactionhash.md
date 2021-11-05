---
description: Gets the transfer event by transaction hash
---

# GetTransferEventByTransactionHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="TransactionHash" required="true" type="String" %}
the transaction hash
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "_id": "6178d218f90696dd6846da09",
        "callFlags": "All",
        "contractHash": "0x38a2aace91f92b979207c0dd50a857c117d4785b",
        "hexStringParams": [
            "fa03cb7b40072c69ca41f0ad3606a548f1d59966",
            "bf23e929d8148a3b2993392fb8566cf9db4f34d5",
            "000000000000003635c9adc5dea00000",
            ""
        ],
        "method": "transfer",
        "originSender": "0xfa03cb7b40072c69ca41f0ad3606a548f1d59966",
        "stack": "HALT",
        "txid": "0xa69f3b6a654a537258bc0e99029ca8924cdb7161955e9a30734cbb247c9d1062",
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
  "method": "GetTransferEventByTransactionHash",
  "params": {"TransactionHash":"0xa69f3b6a654a537258bc0e99029ca8924cdb7161955e9a30734cbb247c9d1062"},
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
    "method": "GetTransferEventByTransactionHash",
    "params": {
      "TransactionHash": "0xa69f3b6a654a537258bc0e99029ca8924cdb7161955e9a30734cbb247c9d1062"
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
