---
agent:
  instructions: "This site offers a search API that returns relevant content across the entire site. Use the search endpoint to find information instead of crawling individual pages."
  search: "https://developers.cloudflare.com/.well-known/search?q={query}"
title: Attach Custom Domain To Bucket (Deprecated)
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[R2](https://developers.cloudflare.com/api/resources/r2)

[Buckets](https://developers.cloudflare.com/api/resources/r2/subresources/buckets)

[Domains](https://developers.cloudflare.com/api/resources/r2/subresources/buckets/subresources/domains)

[Custom](https://developers.cloudflare.com/api/resources/r2/subresources/buckets/subresources/domains/subresources/custom)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Attach Custom Domain To Bucket (Deprecated)

Deprecated: Use create instead (POST /accounts/{account\_id}/r2/buckets/{bucket\_name}/domains/custom). The /custom\_domains path will be removed.

POST/accounts/{account\_id}/r2/buckets/{bucket\_name}/custom\_domains

Registers a new custom domain for an existing R2 bucket. This endpoint does not change whether the domain is enabled; enable it with [Configure Custom Domain Settings](https://developers.cloudflare.com/api/resources/r2/subresources/buckets/subresources/domains/subresources/custom/methods/update/). A domain that was enabled on this bucket and then removed with the deprecated remove endpoint is enabled again as soon as it is attached.

Deprecated: use [Attach Custom Domain To Bucket](https://developers.cloudflare.com/api/resources/r2/subresources/buckets/subresources/domains/subresources/custom/methods/create/) (`POST /accounts/{account_id}/r2/buckets/{bucket_name}/domains/custom`) instead. This endpoint will be removed.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### P ath ParametersExpand Collapse

account\_id: string

Cloudflare account ID that owns the R2 resource.

maxLength32

[Link to this property](#)%20r2.buckets.domains.custom%20%3E%20(method)%20create_legacy%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

bucket\_name: string

Name of the bucket.

maxLength64

minLength3

[Link to this property](#)%20r2.buckets.domains.custom%20%3E%20(method)%20create_legacy%20%3E%20(params)%20default%20%3E%20(param)%20bucket_name%20%3E%20(schema)>)

##### H eader ParametersExpand Collapse

<details>

<summary>

"cf-r2-jurisdiction": optional "default" or "eu" or "us" or 2 more

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"eu"

<a href="#">Link to this property</a>

"us"

<a href="#">Link to this property</a>

"fedramp"

<a href="#">Link to this property</a>

"fedramp-high"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.buckets.domains.custom%20%3E%20(method)%20create_legacy%20%3E%20(params)%20default%20%3E%20(param)%20cf-r2-jurisdiction%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

domain: string

Name of the custom domain to be added.

[Link to this property](#)%20r2.buckets.domains.custom%20%3E%20(method)%20create_legacy%20%3E%20(params)%200%20%3E%20(param)%20domain%20%3E%20(schema)>)

zoneId: string

Zone ID of the custom domain.

[Link to this property](#)%20r2.buckets.domains.custom%20%3E%20(method)%20create_legacy%20%3E%20(params)%200%20%3E%20(param)%20zoneId%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20response_info%20%3E%20(schema)">ResponseInfo</a> { code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object { pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.buckets.domains.custom%20%3E%20(method)%20create_legacy%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

messages: array of string

[Link to this property](#)%20r2.buckets.domains.custom%20%3E%20(method)%20create_legacy%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object { domain }

</summary>

domain: string

Name of the custom domain.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.buckets.domains.custom%20%3E%20(method)%20create_legacy%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Whether the API call was successful.

[Link to this property](#)%20r2.buckets.domains.custom%20%3E%20(method)%20create_legacy%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Attach Custom Domain To Bucket (Deprecated)

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/r2/buckets/$BUCKET_NAME/custom_domains \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "domain": "prefix.example-domain.com",
          "zoneId": "36ca64a6d92827b8a6b90be344bb1bfd"
        }'
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    "string"
  ],
  "result": {
    "domain": "prefix.example-domain.com"
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    "string"
  ],
  "result": {
    "domain": "prefix.example-domain.com"
  },
  "success": true
}
```