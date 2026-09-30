---
title: Instances
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Applications](https://developers.cloudflare.com/api/resources/containers/subresources/applications)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Instances

##### [List container instances (deprecated)](https://developers.cloudflare.com/api/resources/containers/subresources/applications/subresources/instances/methods/list_v1)

Deprecated

GET/accounts/{account\_id}/containers/applications/{application\_id}/instances

##### [List container instances](https://developers.cloudflare.com/api/resources/containers/subresources/applications/subresources/instances/methods/list)

GET/accounts/{account\_id}/containers/applications/{application\_id}/instances-v2

##### [Get a container instance](https://developers.cloudflare.com/api/resources/containers/subresources/applications/subresources/instances/methods/get)

GET/accounts/{account\_id}/containers/applications/{application\_id}/instances/{instance\_id}

##### ModelsExpand Collapse

<details>

<summary>

InstanceListV1Response object {id, application\_id, image, 5 more }

The last-reported state of a logical container instance.

</summary>

id: string

A container instance ID (64-character hex Durable Object actor ID).

maxLength64

minLength64

<a href="#">Link to this property</a>

application\_id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

image: string

The image for the current container placement, when one is available.

<a href="#">Link to this property</a>

<details>

<summary>

status: object {state, updated\_at, exit\_code }

The latest known status of a container instance.

</summary>

<details>

<summary>

state: "provisioning"or "running"or "failed"or 5 more

The current lifecycle state of a container instance.

</summary>

One of the following:

"provisioning"

<a href="#">Link to this property</a>

"running"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"stopping"

<a href="#">Link to this property</a>

"stopped"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"inactive"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

exit\_code: optional number

The process exit code, when the runtime reports one.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

configuration: optional object {disk, memory, vcpu }

The resources allocated to the container instance.

</summary>

disk: number

Disk allocated to the container instance, in decimal MB.

minimum1

<a href="#">Link to this property</a>

memory: number

Memory allocated to the container instance, in MiB.

minimum1

<a href="#">Link to this property</a>

vcpu: number

Number of virtual CPUs allocated to the container instance.

exclusiveMinimum

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {name, region }

The location of the instance’s current container placement.

</summary>

name: string

Unique location code used to identify locations on a logical level.

<a href="#">Link to this property</a>

region: string

Represents a group of datacenters. Choose one of “AFR”, “APAC”, “EEUR”, “ENAM”, “WNAM”, “ME”, “OC”, “SAM”, or “WEUR”.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

The customer-provided instance name, when available. Its UTF-8 encoding uses at most 1,024 bytes.

<a href="#">Link to this property</a>

started\_at: optional string

The time at which the current container placement started, when one exists.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.instances%20%3E%20(model)%20instance_list_v1_response%20%3E%20(schema)>)

<details>

<summary>

InstanceListResponse object {id, application\_id, image, 5 more }

The last-reported state of a logical container instance.

</summary>

id: string

A container instance ID (64-character hex Durable Object actor ID).

maxLength64

minLength64

<a href="#">Link to this property</a>

application\_id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

image: string

The image for the current container placement, when one is available.

<a href="#">Link to this property</a>

<details>

<summary>

status: object {state, updated\_at, exit\_code }

The latest known status of a container instance.

</summary>

<details>

<summary>

state: "provisioning"or "running"or "failed"or 5 more

The current lifecycle state of a container instance.

</summary>

One of the following:

"provisioning"

<a href="#">Link to this property</a>

"running"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"stopping"

<a href="#">Link to this property</a>

"stopped"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"inactive"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

exit\_code: optional number

The process exit code, when the runtime reports one.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

configuration: optional object {disk, memory, vcpu }

The resources allocated to the container instance.

</summary>

disk: number

Disk allocated to the container instance, in decimal MB.

minimum1

<a href="#">Link to this property</a>

memory: number

Memory allocated to the container instance, in MiB.

minimum1

<a href="#">Link to this property</a>

vcpu: number

Number of virtual CPUs allocated to the container instance.

exclusiveMinimum

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {name, region }

The location of the instance’s current container placement.

</summary>

name: string

Unique location code used to identify locations on a logical level.

<a href="#">Link to this property</a>

region: string

Represents a group of datacenters. Choose one of “AFR”, “APAC”, “EEUR”, “ENAM”, “WNAM”, “ME”, “OC”, “SAM”, or “WEUR”.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

The customer-provided instance name, when available. Its UTF-8 encoding uses at most 1,024 bytes.

<a href="#">Link to this property</a>

started\_at: optional string

The time at which the current container placement started, when one exists.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.instances%20%3E%20(model)%20instance_list_response%20%3E%20(schema)>)

<details>

<summary>

InstanceGetResponse object {id, application\_id, image, 5 more }

The last-reported state of a logical container instance.

</summary>

id: string

A container instance ID (64-character hex Durable Object actor ID).

maxLength64

minLength64

<a href="#">Link to this property</a>

application\_id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

image: string

The image for the current container placement, when one is available.

<a href="#">Link to this property</a>

<details>

<summary>

status: object {state, updated\_at, exit\_code }

The latest known status of a container instance.

</summary>

<details>

<summary>

state: "provisioning"or "running"or "failed"or 5 more

The current lifecycle state of a container instance.

</summary>

One of the following:

"provisioning"

<a href="#">Link to this property</a>

"running"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"stopping"

<a href="#">Link to this property</a>

"stopped"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"inactive"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

exit\_code: optional number

The process exit code, when the runtime reports one.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

configuration: optional object {disk, memory, vcpu }

The resources allocated to the container instance.

</summary>

disk: number

Disk allocated to the container instance, in decimal MB.

minimum1

<a href="#">Link to this property</a>

memory: number

Memory allocated to the container instance, in MiB.

minimum1

<a href="#">Link to this property</a>

vcpu: number

Number of virtual CPUs allocated to the container instance.

exclusiveMinimum

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {name, region }

The location of the instance’s current container placement.

</summary>

name: string

Unique location code used to identify locations on a logical level.

<a href="#">Link to this property</a>

region: string

Represents a group of datacenters. Choose one of “AFR”, “APAC”, “EEUR”, “ENAM”, “WNAM”, “ME”, “OC”, “SAM”, or “WEUR”.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

The customer-provided instance name, when available. Its UTF-8 encoding uses at most 1,024 bytes.

<a href="#">Link to this property</a>

started\_at: optional string

The time at which the current container placement started, when one exists.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.instances%20%3E%20(model)%20instance_get_response%20%3E%20(schema)>)