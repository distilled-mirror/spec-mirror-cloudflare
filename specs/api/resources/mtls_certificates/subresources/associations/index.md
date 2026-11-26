---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Associations
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[MTLS Certificates](https://developers.cloudflare.com/api/resources/mtls_certificates)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Associations

##### [List mTLS certificate associations](https://developers.cloudflare.com/api/resources/mtls_certificates/subresources/associations/methods/get)

GET/accounts/{account\_id}/mtls\_certificates/{mtls\_certificate\_id}/associations

##### ModelsExpand Collapse

<details>

<summary>

CertificateAsssociation object { service, status }

</summary>

service: optional string

The service using the certificate.

<a href="#">Link to this property</a>

status: optional string

Certificate deployment status for the given service.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20mtls_certificates.associations%20%3E%20(model)%20certificate_asssociation%20%3E%20(schema)>)