---
title: Versions
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Applications](https://developers.cloudflare.com/api/resources/containers/subresources/applications)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Versions

##### [List all application versions](https://developers.cloudflare.com/api/resources/containers/subresources/applications/subresources/versions/methods/list)

GET/accounts/{account\_id}/containers/applications/{application\_id}/versions

##### ModelsExpand Collapse

<details>

<summary>

VersionListResponse object {configuration, percentage, version }

An application with the configuration of its version.

</summary>

<details>

<summary>

configuration: object {authorized\_keys, command, entrypoint, 4 more }

User-specified container configuration changes.

</summary>

<details>

<summary>

authorized\_keys: optional array of object {public\_key, name }

</summary>

public\_key: string

An SSH public key.

<a href="#">Link to this property</a>

name: optional string

Optional human readable name for this key.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

command: optional array of string

The command that runs when the container starts, passed to the entrypoint. You can override this at run-time. If you override only the command, it gets passed to the default entrypoint specified in the image.

<a href="#">Link to this property</a>

entrypoint: optional array of string

The entry point for the container, specifying the executable to run when the container starts. You can override this at run-time. If you do, the default command from the image is ignored. Specify both entrypoint and command at run-time to completely replace the image defaults.

<a href="#">Link to this property</a>

<details>

<summary>

environment\_variables: optional array of object {name, value }

Container environment variables.

</summary>

name: string

An environment variable name.

<a href="#">Link to this property</a>

value: string

An environment variable value.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

image: optional string

Image url.

<a href="#">Link to this property</a>

<details>

<summary>

instance\_type: optional "lite"or "basic"or "standard-1"or 3 more

The instance type configures vCPU, memory, and disk.

- “lite”: 1/16 vCPU, 256 MiB memory, 2 GB disk
- “basic”: 1/4 vCPU, 1 GiB memory, 4 GB disk
- “standard-1”: 1/2 vCPU, 4 GiB memory, 8 GB disk
- “standard-2”: 1 vCPU, 6 GiB memory, 12 GB disk
- “standard-3”: 2 vCPU, 8 GiB memory, 16 GB disk
- “standard-4”: 4 vCPU, 12 GiB memory, 20 GB disk

</summary>

One of the following:

"lite"

<a href="#">Link to this property</a>

"basic"

<a href="#">Link to this property</a>

"standard-1"

<a href="#">Link to this property</a>

"standard-2"

<a href="#">Link to this property</a>

"standard-3"

<a href="#">Link to this property</a>

"standard-4"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Settings for deployment observability such as logging.

</summary>

<details>

<summary>

logs: optional object {enabled }

Observability logging settings.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

percentage: number

<a href="#">Link to this property</a>

version: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.versions%20%3E%20(model)%20version_list_response%20%3E%20(schema)>)