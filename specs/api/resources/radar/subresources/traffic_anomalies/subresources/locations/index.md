---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Locations
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Radar](https://developers.cloudflare.com/api/resources/radar)

[Traffic Anomalies](https://developers.cloudflare.com/api/resources/radar/subresources/traffic_anomalies)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Locations

##### [Get top locations by total traffic anomalies](https://developers.cloudflare.com/api/resources/radar/subresources/traffic_anomalies/subresources/locations/methods/get)

GET/radar/traffic\_anomalies/locations

##### ModelsExpand Collapse

<details>

<summary>

LocationGetResponse object { trafficAnomalies }

</summary>

<details>

<summary>

trafficAnomalies: array of object { clientCountryAlpha2, clientCountryName, value }

</summary>

clientCountryAlpha2: string

<a href="#">Link to this property</a>

clientCountryName: string

<a href="#">Link to this property</a>

value: string

A numeric string.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20radar.traffic_anomalies.locations%20%3E%20(model)%20location_get_response%20%3E%20(schema)>)