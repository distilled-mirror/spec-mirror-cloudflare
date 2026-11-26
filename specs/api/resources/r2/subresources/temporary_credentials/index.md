---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Temporary Credentials
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[R2](https://developers.cloudflare.com/api/resources/r2)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Temporary Credentials

##### [Create Temporary Access Credentials](https://developers.cloudflare.com/api/resources/r2/subresources/temporary_credentials/methods/create)

POST/accounts/{account\_id}/r2/temp-access-credentials

##### ModelsExpand Collapse

<details>

<summary>

TemporaryCredential object { bucket, parentAccessKeyId, ttlSeconds, 4 more }

</summary>

bucket: string

Name of the R2 bucket.

<a href="#">Link to this property</a>

parentAccessKeyId: string

Access key ID of the parent R2 API token. The temporary credentials cannot exceed this token’s permissions.

<a href="#">Link to this property</a>

ttlSeconds: number

Lifetime of the temporary credentials in seconds, up to 604800 seconds (7 days).

maximum604800

minimum0

<a href="#">Link to this property</a>

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

<a href="#">Link to this property</a>

objects: optional array of string

Optional object paths to scope the credentials to.

<a href="#">Link to this property</a>

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

<a href="#">Link to this property</a>

prefixes: optional array of string

Optional prefix paths to scope the credentials to.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(model)%20temporary_credential%20%3E%20(schema)>)

<details>

<summary>

TemporaryCredentialCreateResponse object { accessKeyId, secretAccessKey, sessionToken }

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

[Link to this property](#)%20r2.temporary_credentials%20%3E%20(model)%20temporary_credential_create_response%20%3E%20(schema)>)