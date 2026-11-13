---
title: State
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Security Center](https://developers.cloudflare.com/api/resources/security_center)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# State

##### [Retrieves Account State](https://developers.cloudflare.com/api/resources/security_center/subresources/state/methods/get)

GET/accounts/{account\_id}/security-center/state

##### [Updates Account State](https://developers.cloudflare.com/api/resources/security_center/subresources/state/methods/update)

PUT/accounts/{account\_id}/security-center/state

##### ModelsExpand Collapse

<details>

<summary>

StateGetResponse object {recent\_dormant\_reactivation, scans\_enabled }

</summary>

recent\_dormant\_reactivation: boolean

Whether the account was recently reactivated from a dormant state (used to show the reactivation banner).

<a href="#">Link to this property</a>

scans\_enabled: boolean

Whether on-demand and scheduled scans are enabled for the account.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20security_center.state%20%3E%20(model)%20state_get_response%20%3E%20(schema)>)

<details>

<summary>

StateUpdateResponse object {recent\_dormant\_reactivation, scans\_enabled }

</summary>

recent\_dormant\_reactivation: boolean

Whether the account was recently reactivated from a dormant state (used to show the reactivation banner).

<a href="#">Link to this property</a>

scans\_enabled: boolean

Whether on-demand and scheduled scans are enabled for the account.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20security_center.state%20%3E%20(model)%20state_update_response%20%3E%20(schema)>)