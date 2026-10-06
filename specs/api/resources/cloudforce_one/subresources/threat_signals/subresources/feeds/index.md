---
title: Feeds
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Feeds

##### [List Threat Signals feeds](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds/methods/list)

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds

##### [Create Threat Signals feed](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds/methods/create)

POST/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds

##### [Update Threat Signals feed](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds/methods/edit)

PATCH/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds/{feed\_id}

##### [Delete Threat Signals feed](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds/methods/delete)

DELETE/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds/{feed\_id}

##### [Trigger Threat Signals feed poll](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds/methods/poll)

POST/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds/poll

##### ModelsExpand Collapse

<details>

<summary>

FeedListResponse object {count, custom\_feed\_count, custom\_feed\_limit, 4 more }

</summary>

count: number

Number of feeds on this page.

<a href="#">Link to this property</a>

custom\_feed\_count: number

The current count of custom feeds for the account.

minimum0

<a href="#">Link to this property</a>

custom\_feed\_limit: number

The resolved custom feed limit for the account.

minimum0

<a href="#">Link to this property</a>

<details>

<summary>

feeds: array of object {id, category\_id, category\_name, 12 more }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

category\_id: string

Feed category identifier. Null when unset.

<a href="#">Link to this property</a>

category\_name: string

Display name of the feed category. Null when unset or unresolvable.

<a href="#">Link to this property</a>

created\_at: string

<a href="#">Link to this property</a>

curated\_feed\_id: string

Curated catalog feed this subscription was created from. Null for custom feeds.

<a href="#">Link to this property</a>

display\_name: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

last\_polled\_at: string

<a href="#">Link to this property</a>

poll\_interval\_s: number

<a href="#">Link to this property</a>

source\_type: string

<code>custom</code> for a feed added by URL, <code>curated</code> for a curated catalog feed.

<a href="#">Link to this property</a>

status: string

Polling health: <code>active</code>, or <code>error</code> after a failed poll.

<a href="#">Link to this property</a>

subscribed\_at: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated\_at: string

<a href="#">Link to this property</a>

url: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

page: number

<a href="#">Link to this property</a>

per\_page: number

<a href="#">Link to this property</a>

total\_count: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(model)%20feed_list_response%20%3E%20(schema)>)

<details>

<summary>

FeedCreateResponse object {id, category\_id, category\_name, 12 more }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

category\_id: string

Feed category identifier. Null when unset.

<a href="#">Link to this property</a>

category\_name: string

Display name of the feed category. Null when unset or unresolvable.

<a href="#">Link to this property</a>

created\_at: string

<a href="#">Link to this property</a>

curated\_feed\_id: string

Curated catalog feed this subscription was created from. Null for custom feeds.

<a href="#">Link to this property</a>

display\_name: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

last\_polled\_at: string

<a href="#">Link to this property</a>

poll\_interval\_s: number

<a href="#">Link to this property</a>

source\_type: string

<code>custom</code> for a feed added by URL, <code>curated</code> for a curated catalog feed.

<a href="#">Link to this property</a>

status: string

Polling health: <code>active</code>, or <code>error</code> after a failed poll.

<a href="#">Link to this property</a>

subscribed\_at: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated\_at: string

<a href="#">Link to this property</a>

url: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(model)%20feed_create_response%20%3E%20(schema)>)

<details>

<summary>

FeedEditResponse object {id, category\_id, category\_name, 12 more }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

category\_id: string

Feed category identifier. Null when unset.

<a href="#">Link to this property</a>

category\_name: string

Display name of the feed category. Null when unset or unresolvable.

<a href="#">Link to this property</a>

created\_at: string

<a href="#">Link to this property</a>

curated\_feed\_id: string

Curated catalog feed this subscription was created from. Null for custom feeds.

<a href="#">Link to this property</a>

display\_name: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

last\_polled\_at: string

<a href="#">Link to this property</a>

poll\_interval\_s: number

<a href="#">Link to this property</a>

source\_type: string

<code>custom</code> for a feed added by URL, <code>curated</code> for a curated catalog feed.

<a href="#">Link to this property</a>

status: string

Polling health: <code>active</code>, or <code>error</code> after a failed poll.

<a href="#">Link to this property</a>

subscribed\_at: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated\_at: string

<a href="#">Link to this property</a>

url: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(model)%20feed_edit_response%20%3E%20(schema)>)

<details>

<summary>

FeedDeleteResponse object {id, category\_id, category\_name, 12 more }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

category\_id: string

Feed category identifier. Null when unset.

<a href="#">Link to this property</a>

category\_name: string

Display name of the feed category. Null when unset or unresolvable.

<a href="#">Link to this property</a>

created\_at: string

<a href="#">Link to this property</a>

curated\_feed\_id: string

Curated catalog feed this subscription was created from. Null for custom feeds.

<a href="#">Link to this property</a>

display\_name: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

last\_polled\_at: string

<a href="#">Link to this property</a>

poll\_interval\_s: number

<a href="#">Link to this property</a>

source\_type: string

<code>custom</code> for a feed added by URL, <code>curated</code> for a curated catalog feed.

<a href="#">Link to this property</a>

status: string

Polling health: <code>active</code>, or <code>error</code> after a failed poll.

<a href="#">Link to this property</a>

subscribed\_at: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated\_at: string

<a href="#">Link to this property</a>

url: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(model)%20feed_delete_response%20%3E%20(schema)>)

<details>

<summary>

FeedPollResponse object {errors, feeds, triggered }

</summary>

errors: number

<a href="#">Link to this property</a>

<details>

<summary>

feeds: array of object {feed\_id, status, workflow\_id, feed\_enabled }

</summary>

feed\_id: string

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

status: "workflow\_created"or "error"

</summary>

One of the following:

"workflow\_created"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

workflow\_id: string

<a href="#">Link to this property</a>

feed\_enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

triggered: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(model)%20feed_poll_response%20%3E%20(schema)>)

#### FeedsRaw

##### [Get Threat Signals feed XML](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds/subresources/raw/methods/get)

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds/{feed\_id}/raw

##### ModelsExpand Collapse

RawGetResponse = string

[Link to this property](#)%20cloudforce_one.threat_signals.feeds.raw%20%3E%20(model)%20raw_get_response%20%3E%20(schema)>)

#### FeedsSkills

##### [Get Threat Signals feed skills](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds/subresources/skills/methods/get)

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds/{feed\_id}/skills

##### [Set Threat Signals feed skills](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds/subresources/skills/methods/update)

PUT/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds/{feed\_id}/skills

##### ModelsExpand Collapse

<details>

<summary>

SkillGetResponse object {feed\_id, skills }

</summary>

feed\_id: string

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

skills: array of object {id, config, created\_at, 7 more }

</summary>

id: string

<a href="#">Link to this property</a>

config: string

JSON-encoded skill configuration. Always null for default skills.

<a href="#">Link to this property</a>

created\_at: string

<a href="#">Link to this property</a>

is\_active: number

1 when active, 0 when inactive.

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

output\_schema: string

JSON-encoded JSON Schema the skill output must satisfy.

<a href="#">Link to this property</a>

prompt: string

<a href="#">Link to this property</a>

<details>

<summary>

source: "default"or "custom"

<code>default</code> for Cloudforce One managed skills (read-only), <code>custom</code> for account skills.

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"custom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: string

<a href="#">Link to this property</a>

updated\_at: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds.skills%20%3E%20(model)%20skill_get_response%20%3E%20(schema)>)

<details>

<summary>

SkillUpdateResponse object {feed\_id, skills }

</summary>

feed\_id: string

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

skills: array of object {position, skill\_id }

</summary>

position: number

Zero-based pipeline position.

<a href="#">Link to this property</a>

skill\_id: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds.skills%20%3E%20(model)%20skill_update_response%20%3E%20(schema)>)