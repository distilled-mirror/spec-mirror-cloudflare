---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Search
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Radar](https://developers.cloudflare.com/api/resources/radar)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Search

##### [Search for locations, ASes, reports, and more](https://developers.cloudflare.com/api/resources/radar/subresources/search/methods/global)

GET/radar/search/global

##### ModelsExpand Collapse

<details>

<summary>

SearchGlobalResponse object { search }

</summary>

<details>

<summary>

search: array of object { code, name, type, entity }

</summary>

code: string

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

type: string

<a href="#">Link to this property</a>

<details>

<summary>

entity: optional object { aka, asn, category, 2 more } or object { geoId, name, parent }

Matched entity: an AS for <code>asn</code> results, a geolocation for <code>adm1</code> and <code>adm2</code>. Null for other types.

</summary>

One of the following:

<details>

<summary>

object { aka, asn, category, 2 more }

</summary>

aka: string

Alternative name of the AS.

<a href="#">Link to this property</a>

asn: number

AS number.

<a href="#">Link to this property</a>

<details>

<summary>

category: "ACCESS\_ISP" or "HOSTING\_CLOUD\_CONTENT" or "ORGANIZATION"

Inferred network type of the AS: <code>ACCESS_ISP</code> (networks connecting end users, plus transit), <code>HOSTING_CLOUD_CONTENT</code> (hosting providers, clouds and CDNs) or <code>ORGANIZATION</code> (enterprises, universities, governments, banks and IXP route servers). <code>null</code> when the AS is not classified.

</summary>

One of the following:

"ACCESS\_ISP"

<a href="#">Link to this property</a>

"HOSTING\_CLOUD\_CONTENT"

<a href="#">Link to this property</a>

"ORGANIZATION"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

country: string

Alpha-2 code of the country or territory where the AS is registered.

<a href="#">Link to this property</a>

name: string

AS name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object { geoId, name, parent }

</summary>

geoId: string

GeoNames ID of the geolocation.

<a href="#">Link to this property</a>

name: string

Localized name of the geolocation.

<a href="#">Link to this property</a>

<details>

<summary>

parent: object { code, name, type }

Parent geolocation (country for <code>adm1</code>, <code>adm1</code> for <code>adm2</code>).

</summary>

code: string

Code of the parent: alpha-2 code for a country, subdivision code for an <code>adm1</code>.

<a href="#">Link to this property</a>

name: string

Localized name of the parent geolocation.

<a href="#">Link to this property</a>

type: string

Type of the parent geolocation, such as <code>COUNTRY</code> or <code>ADM1</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20radar.search%20%3E%20(model)%20search_global_response%20%3E%20(schema)>)