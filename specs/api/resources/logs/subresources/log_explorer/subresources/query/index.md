---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Query
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Logs](https://developers.cloudflare.com/api/resources/logs)

[Log Explorer](https://developers.cloudflare.com/api/resources/logs/subresources/log_explorer)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Query

##### [Run a log query](https://developers.cloudflare.com/api/resources/logs/subresources/log_explorer/subresources/query/methods/sql)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/logs/explorer/query/sql

##### ModelsExpand Collapse

QuerySqlResponse = map\[unknown]

[Link to this property](#)%20logs.log_explorer.query%20%3E%20(model)%20query_sql_response%20%3E%20(schema)>)