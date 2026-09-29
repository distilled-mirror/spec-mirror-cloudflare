---
title: Skills
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Skills

##### [List Threat Signals skills](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills/methods/list)

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills

##### [Create Threat Signals skill](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills/methods/create)

POST/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills

##### [Get Threat Signals skill](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills/methods/get)

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills/{skill\_id}

##### [Update Threat Signals skill](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills/methods/edit)

PATCH/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills/{skill\_id}

##### [Delete Threat Signals skill](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills/methods/delete)

DELETE/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills/{skill\_id}

##### ModelsExpand Collapse

<details>

<summary>

SkillListResponse object {count, custom\_skills\_available, page, 3 more }

</summary>

count: number

Number of skills on this page.

<a href="#">Link to this property</a>

custom\_skills\_available: boolean

Whether the authenticated account may access custom-skill capabilities under Stakeout’s Threat Signals access-mode policy. This is a policy availability indicator, not a row-existence indicator. False for threat\_signals\_only mode; true for entitled, allowlisted, cfone\_internal, and service modes.

<a href="#">Link to this property</a>

page: number

<a href="#">Link to this property</a>

per\_page: number

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

total\_count: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(model)%20skill_list_response%20%3E%20(schema)>)

<details>

<summary>

SkillCreateResponse object {id, config, created\_at, 7 more }

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

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(model)%20skill_create_response%20%3E%20(schema)>)

<details>

<summary>

SkillGetResponse object {id, config, created\_at, 7 more }

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

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(model)%20skill_get_response%20%3E%20(schema)>)

<details>

<summary>

SkillEditResponse object {id, config, created\_at, 7 more }

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

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(model)%20skill_edit_response%20%3E%20(schema)>)

<details>

<summary>

SkillDeleteResponse object {id, config, created\_at, 7 more }

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

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(model)%20skill_delete_response%20%3E%20(schema)>)

#### SkillsTag Categories

##### [Get Threat Signals skill tag categories](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills/subresources/tag_categories/methods/get)

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills/{skill\_id}/tag-categories

##### [Replace Threat Signals skill tag categories](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills/subresources/tag_categories/methods/update)

PUT/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills/{skill\_id}/tag-categories

##### ModelsExpand Collapse

<details>

<summary>

TagCategoryGetResponse object {category\_uuids, skill\_id }

</summary>

category\_uuids: array of string

<a href="#">Link to this property</a>

skill\_id: "default-tagging-skill"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills.tag_categories%20%3E%20(model)%20tag_category_get_response%20%3E%20(schema)>)

<details>

<summary>

TagCategoryUpdateResponse object {category\_uuids, skill\_id }

</summary>

category\_uuids: array of string

<a href="#">Link to this property</a>

skill\_id: "default-tagging-skill"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills.tag_categories%20%3E%20(model)%20tag_category_update_response%20%3E%20(schema)>)