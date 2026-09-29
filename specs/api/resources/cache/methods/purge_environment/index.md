---
title: Purge Cached Content by Environment
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cache](https://developers.cloudflare.com/api/resources/cache)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Purge Cached Content by Environment

POST/zones/{zone\_id}/environments/{environment\_id}/purge\_cache

Deletes cached content for one environment of the zone. Content cached for the zone’s other environments, including production, is not affected. Otherwise this works like `POST /zones/{zone_id}/purge_cache`: the next request for purged content is a cache `MISS`, and the request body takes the same fields.

Environments are part of [Version Management](https://developers.cloudflare.com/version-management/). To keep content cached and have Cloudflare revalidate it instead, use `POST /zones/{zone_id}/environments/{environment_id}/invalidate_cache`.

Purging by URL (`files`) does not work for environments that select requests by IP address, country, ASN, or threat score, and fails with error `1136`. Use `tags`, `hosts`, `prefixes`, or `purge_everything` for those environments.

### Availability and limits

Rate limits and the number of items you can send in one request depend on your plan. See [Purge cache: availability and limits](https://developers.cloudflare.com/cache/how-to/purge-cache/#availability-and-limits).

##### Security

<details>

<summary>API Token</summary>



The preferred authorization scheme for interacting with the Cloudflare API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/create-token/">Create a token</a>.

**Example:**<code>Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY</code>

</details>

<details>

<summary>API Email + API Key</summary>



The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**<code>X-Auth-Email: user@example.com</code>

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**<code>X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194</code>

</details>

##### Accepted Permissions (at least one required)

`Cache Purge`

##### P ath ParametersExpand Collapse

zone\_id: string

maxLength32

[Link to this property](#)%20cache%20%3E%20(method)%20purge_environment%20%3E%20(params)%200%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

environment\_id: string

maxLength32

[Link to this property](#)%20cache%20%3E%20(method)%20purge_environment%20%3E%20(params)%200%20%3E%20(param)%20environment_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

body: object {tags } or object {hosts } or object {prefixes } or 3 more

</summary>

One of the following:

<details>

<summary>

CachePurgeFlexPurgeByTags object {tags }

</summary>

tags: optional array of string

Cache tags. Targets all content whose <code>Cache-Tag</code> response header contains at least one of these tags. See <a href="https://developers.cloudflare.com/cache/how-to/purge-cache/purge-by-tags/">Purge cache by cache-tags</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CachePurgeFlexPurgeByHostnames object {hosts }

</summary>

hosts: optional array of string

Hostnames, such as <code>www.example.com</code>. Targets all content cached for these hostnames. See <a href="https://developers.cloudflare.com/cache/how-to/purge-cache/purge-by-hostname/">Purge cache by hostname</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CachePurgeFlexPurgeByPrefixes object {prefixes }

</summary>

prefixes: optional array of string

URL prefixes, each a hostname followed by a path, such as <code>www.example.com/blog/</code>. Targets all content whose URL starts with one of these prefixes. Do not include a scheme, query string, or fragment. See <a href="https://developers.cloudflare.com/cache/how-to/purge-cache/purge_by_prefix/">Purge cache by prefix</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CachePurgeEverything object {purge\_everything }

</summary>

purge\_everything: optional boolean

Set to <code>true</code> to target all cached content in the zone, or in the environment for the environment endpoints. Must be the only field in the request. See <a href="https://developers.cloudflare.com/cache/how-to/purge-cache/purge-everything/">Purge everything</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CachePurgeSingleFile object {files }

</summary>

files: optional array of string

Full URLs, such as <code>https://www.example.com/css/styles.css</code>. Targets the content cached for each URL. If your cache key includes request headers, send objects with <code>url</code> and <code>headers</code> instead. See <a href="https://developers.cloudflare.com/cache/how-to/purge-cache/purge-by-single-file/">Purge by single-file</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CachePurgeSingleFileWithURLAndHeaders object {files }

</summary>

<details>

<summary>

files: optional array of object {headers, url }

URLs with the request headers your cache key uses. Use this form when your cache key includes request headers, or the visitor’s device type, country, or language: send the header values each URL was cached with, such as <code>CF-Device-Type</code>, <code>CF-IPCountry</code>, or <code>Accept-Language</code>.

When you send the <code>Origin</code> header, include the scheme and hostname. Include the port unless it is the default for the scheme: 80 for <code>http</code>, 443 for <code>https</code>.

See <a href="https://developers.cloudflare.com/cache/how-to/purge-cache/purge-by-single-file/">Purge by single-file</a>.

</summary>

headers: optional map\[string]

Request headers and the values the content was cached with.

<a href="#">Link to this property</a>

url: optional string

Full URL of the content.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cache%20%3E%20(method)%20purge_environment%20%3E%20(params)%200%20%3E%20(param)%20body%20%3E%20(schema)>)

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

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cache%20%3E%20(method)%20purge_environment%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20response_info%20%3E%20(schema)">ResponseInfo</a> { code, message, documentation\_url, source }

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

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cache%20%3E%20(method)%20purge_environment%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: boolean

Indicates the API call’s success or failure.

[Link to this property](#)%20cache%20%3E%20(method)%20purge_environment%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {id }

</summary>

id: string

maxLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cache%20%3E%20(method)%20purge_environment%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Purge Cached Content by Environment

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/environments/$ENVIRONMENT_ID/purge_cache \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "tags": [
            "product-1234",
            "homepage"
          ]
        }'
```

200 example

4XX example

4XX example

```
{
  "errors": [],
  "messages": [],
  "result": {
    "id": "023e105f4ecef8ad9ca31a8372d0c353"
  },
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 1092,
      "message": "Request cannot contain \"purge_everything\" and any of \"files\", \"tags\", \"hosts\" or \"prefixes\""
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 1134,
      "message": "Unable to purge, rate limit reached. Please wait and consider throttling your request speed"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

##### Returns Examples

200 example

4XX example

4XX example

```
{
  "errors": [],
  "messages": [],
  "result": {
    "id": "023e105f4ecef8ad9ca31a8372d0c353"
  },
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 1092,
      "message": "Request cannot contain \"purge_everything\" and any of \"files\", \"tags\", \"hosts\" or \"prefixes\""
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 1134,
      "message": "Unable to purge, rate limit reached. Please wait and consider throttling your request speed"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```