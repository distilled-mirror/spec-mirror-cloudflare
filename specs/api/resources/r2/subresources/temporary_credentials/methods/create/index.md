---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Create Temporary Access Credentials
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[R2](https://developers.cloudflare.com/api/resources/r2)

[Temporary Credentials](https://developers.cloudflare.com/api/resources/r2/subresources/temporary_credentials)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Create Temporary Access Credentials

POST/accounts/{account\_id}/r2/temp-access-credentials

Creates temporary access credentials on a bucket that can be optionally scoped to prefixes or objects. The credentials grant either a permission level or an explicit list of S3 actions.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### P ath ParametersExpand Collapse

account\_id: string

Cloudflare account ID that owns the R2 resource.

maxLength32

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

bucket: string

Name of the R2 bucket.

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20bucket%20%3E%20(schema)>)

parentAccessKeyId: string

Access key ID of the parent R2 API token. The temporary credentials cannot exceed this token’s permissions.

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20parentAccessKeyId%20%3E%20(schema)>)

ttlSeconds: number

Lifetime of the temporary credentials in seconds, up to 604800 seconds (7 days).

maximum604800

minimum0

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20ttlSeconds%20%3E%20(schema)>)

<details>

<summary>

actions: optional array of "HeadBucket" or "HeadObject" or "GetObject" or 15 more

S3 actions allowed on the credentials; requests for any other action are denied. For example, <code>["GetObject", "HeadObject"]</code> allows reading objects without listing them. Exactly one of <code>permission</code> or <code>actions</code> must be provided. The parent token must have Object Read &amp; Write permission if any action writes, and Object Read otherwise.

</summary>

One of the following:

"HeadBucket"

<a href="#">Link to this property</a>

"HeadObject"

<a href="#">Link to this property</a>

"GetObject"

<a href="#">Link to this property</a>

"GetBucketLocation"

<a href="#">Link to this property</a>

"ListObjectsV1"

<a href="#">Link to this property</a>

"ListObjectsV2"

<a href="#">Link to this property</a>

"ListMultipartUploads"

<a href="#">Link to this property</a>

"ListParts"

<a href="#">Link to this property</a>

"PutObject"

<a href="#">Link to this property</a>

"DeleteObject"

<a href="#">Link to this property</a>

"DeleteObjects"

<a href="#">Link to this property</a>

"DeleteObjectsByPrefix"

<a href="#">Link to this property</a>

"CopyObject"

<a href="#">Link to this property</a>

"CreateMultipartUpload"

<a href="#">Link to this property</a>

"UploadPart"

<a href="#">Link to this property</a>

"UploadPartCopy"

<a href="#">Link to this property</a>

"AbortMultipartUpload"

<a href="#">Link to this property</a>

"CompleteMultipartUpload"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20actions%20%3E%20(schema)>)

objects: optional array of string

Optional object paths to scope the credentials to.

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20objects%20%3E%20(schema)>)

<details>

<summary>

permission: optional "admin-read-write" or "admin-read-only" or "object-read-write" or "object-read-only"

Permissions allowed on the credentials. Exactly one of <code>permission</code> or <code>actions</code> must be provided.

</summary>

One of the following:

"admin-read-write"

<a href="#">Link to this property</a>

"admin-read-only"

<a href="#">Link to this property</a>

"object-read-write"

<a href="#">Link to this property</a>

"object-read-only"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20permission%20%3E%20(schema)>)

prefixes: optional array of string

Optional prefix paths to scope the credentials to.

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20prefixes%20%3E%20(schema)>)

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

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

messages: array of string

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object { accessKeyId, secretAccessKey, sessionToken }

</summary>

accessKeyId: optional string

ID for new access key.

<a href="#">Link to this property</a>

secretAccessKey: optional string

Secret access key.

<a href="#">Link to this property</a>

sessionToken: optional string

Security token.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Whether the API call was successful.

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Create Temporary Access Credentials

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/r2/temp-access-credentials \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "bucket": "example-bucket",
          "parentAccessKeyId": "example-access-key-id",
          "ttlSeconds": 3600
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
    "accessKeyId": "example-access-key-id",
    "secretAccessKey": "example-secret-key",
    "sessionToken": "example-session-token"
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
    "accessKeyId": "example-access-key-id",
    "secretAccessKey": "example-secret-key",
    "sessionToken": "example-session-token"
  },
  "success": true
}
```