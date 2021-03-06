---
description: Gets the Nep11 properties by contracthash and tokenId
---

# GetNep11PropertiesByContractHashTokenId

### API Format

{% swagger method="post" path="" baseUrl="https://testneofura.ngd.network:444" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ContractHash" required="true" type="String" %}
the contract script hash
{% endswagger-parameter %}

{% swagger-parameter in="body" name="TokenId" type="[]String" %}
tokenId
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 1,
    "result": {
        "result": [
            {
                "+nP6+q1lkLy6ibAdGfG3qKCfGNVnHvrMOTj+5IIgmXo=": {
                    "_id": "61702d93eb743bed51b918e6",
                    "asset": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                    "properties": "{\n  \"owner\": \"AAAAAAAAAAAAAAAAAAAAAAAAAAA=\",\n  \"name\": \"Pic List\",\n  \"description\": \"List of Pictures\",\n  \"image\": \"https://ipfs.io/ipfs/QmYXzX6TfgvdZSdpDRhTKK56ugvBPh86woedL1u9AQmd9h\"\n}",
                    "tokenid": "+nP6+q1lkLy6ibAdGfG3qKCfGNVnHvrMOTj+5IIgmXo="
                }
            },
            {
                "C85LNUKkJNHu802Yd0HgDxI3JJoJ/j6X/Rl0Cb8ky4c=": {
                    "_id": "61702d0beb743bed51b8fcee",
                    "asset": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                    "properties":"[\"\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \",\"\测\试\",\"NFT\测\试\",\"https://neo3.testnet.neotube.io/contract/0x4f628a187e133fa98a5fd0795df3065f219e414e\"]",
                    "tokenid": "C85LNUKkJNHu802Yd0HgDxI3JJoJ/j6X/Rl0Cb8ky4c="
                }
            },
            {
                "ekVC/9KLlVTQcowaYbijOrBmDPadXNFOe6W0M3zwdJE=": {
                    "_id": "617029e0cd1d7cf225aa48f7",
                    "asset": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                    "properties":"H(owner(                    (name(PIC(\u000bdescription(Test(image(%https://www.bejson.com/jsonviewernew/",
                    "tokenid": "ekVC/9KLlVTQcowaYbijOrBmDPadXNFOe6W0M3zwdJE="
                }
            },
            {
                "U9qaPp0ehFf6afitJ+msIqcM/3T+wEWfvFz1/HOYUzw=": {
                    "_id": "617029bceb743bed51b864fd",
                    "asset": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                    "properties":"H(owner(                    (name(PIC01(\u000bdescription(龙眼木雕草原牧羊女(image(Shttps://bafybeibncam5kafcufwlpu4dcw2lpsqswgre2ax54pxsa5tkfceycn73qi.ipfs.dweb.link/",
                    "tokenid": "U9qaPp0ehFf6afitJ+msIqcM/3T+wEWfvFz1/HOYUzw="
                }
            },
            {
                "MG3uriu8UCtAWwkG4FRDCxac590P3HrlnbF4l27+6QU=": {
                    "_id": "61701c4beb743bed51b29638",
                    "asset": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                    "properties":"{\n  \"owner\": \"AAAAAAAAAAAAAAAAAAAAAAAAAAA=\",\n  \"name\": \"NFT Test\",\n  \"description\": \"\政\协\发\言\",\n  \"image\": \"https://bafkreifsgllxeb2yrtglj7f3o2iwl6ascq7etpsyoxtgh4fgcz3vp3mi6q.ipfs.dweb.link/\"\n}",
                    "tokenid": "MG3uriu8UCtAWwkG4FRDCxac590P3HrlnbF4l27+6QU="
                }
            },
            {
                "cgYnvmxtWy2TmYHxqxtaePYbd468e98FpTd2fAIob30=": {
                    "_id": "61701b8beb743bed51b26eef",
                    "asset": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                    "properties": "{\n  \"owner\": \"AAAAAAAAAAAAAAAAAAAAAAAAAAA=\",\n  \"name\": \"NFT Test\",\n  \"description\": \"Test for NFT Smart Contract\",\n  \"image\": \"https://bafybeigbbwskbb4x2slyey2eykovr4qn6tdyrk55vq22btj2eyichnobii.ipfs.dweb.link/\"\n}",
                    "tokenid": "cgYnvmxtWy2TmYHxqxtaePYbd468e98FpTd2fAIob30="
                }
            },
            {
                "u1QPjbPg6hoxndCkGG7I6rsPn7LWAa86q+GAcN/7/14=": {
                    "_id": "617016b8eb743bed51b16d1a",
                    "asset": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                    "properties": "{\n  \"owner\": \"iSLhRspfzW9zj2r/DVkzGPF6BVk=\",\n  \"name\": \"DOC\",\n  \"description\": \"An other NFT test\",\n  \"image\": \"https://bafybeidlnk5w3khz7zpq7rqlwjg77whhli5c5i5rahyyqz4pwfhbpqnppi.ipfs.dweb.link/\"\n}",
                    "tokenid": "u1QPjbPg6hoxndCkGG7I6rsPn7LWAa86q+GAcN/7/14="
                }
            },
            {
                "X3685uxIZRNoROOSfzBXJtUWSDMF8jEONGInRzb0KDg=": {
                    "_id": "617016b0eb743bed51b16a9d",
                    "asset": "0x4f628a187e133fa98a5fd0795df3065f219e414e",
                    "properties": "{\n  \"owner\": \"iSLhRspfzW9zj2r/DVkzGPF6BVk=\",\n  \"name\": \"Test\",\n  \"description\": \"Test for NFT\",\n  \"image\": \"https://bafybeigbbwskbb4x2slyey2eykovr4qn6tdyrk55vq22btj2eyichnobii.ipfs.dweb.link/\"\n}",
                    "tokenid": "X3685uxIZRNoROOSfzBXJtUWSDMF8jEONGInRzb0KDg="
                }
            }
        ],
        "totalCount": 8
    },
    "error": null
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
    "method": "GetNep11PropertiesByContractHashTokenId",
    "params": {"ContractHash":"0x4f628a187e133fa98a5fd0795df3065f219e414e"},
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
    "method": "GetNep11PropertiesByContractHashTokenId",
    "params": {
      "ContractHash": "0x4f628a187e133fa98a5fd0795df3065f219e414e"
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
