---
description: Gets the Nep11 transfer By transactionhash
---

# GetNep11TransferByTransactionHash

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="TransactionHash" required="true" %}
the transactionhash
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
                "_id": "614bf4b630669383446822b0",
                "blockhash": "0x645cc9744225cc8222ff18ec112e2e260cbeae0efad1094b9bc98930afb84304",
                "contract": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                "decimals": 8,
                "from": null,
                "frombalance": "0",
                "timestamp": 1627284349560,
                "to": "0x59057af11833590dff6a8f736fcd5fca46e12289",
                "tobalance": "1",
                "tokenId": "X3685uxIZRNoROOSfzBXJtUWSDMF8jEONGInRzb0KDg=",
                "tokenname": "FBACC.NFT",
                "txid": "0xa15ed65858d1e73a45c5f0f9d29462fe00e1d608a8f471a293eeda80ac28294b",
                "value": "1"
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
  "method": "GetNep11TransferByTransactionHash",
  "params": {"TransactionHash": "0xa15ed65858d1e73a45c5f0f9d29462fe00e1d608a8f471a293eeda80ac28294b",
  "Limit":3 },
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
    "method": "GetNep11TransferByTransactionHash",
    "params": {
      "TransactionHash": "0xa15ed65858d1e73a45c5f0f9d29462fe00e1d608a8f471a293eeda80ac28294b",
      "Limit": 3
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
