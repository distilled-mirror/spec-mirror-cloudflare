---
title: Applications
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Applications

##### [List Applications associated with your account](https://developers.cloudflare.com/api/resources/containers/subresources/applications/methods/list)

GET/accounts/{account\_id}/containers/applications

##### [Create a new application](https://developers.cloudflare.com/api/resources/containers/subresources/applications/methods/create)

POST/accounts/{account\_id}/containers/applications

##### [Get a single application by id](https://developers.cloudflare.com/api/resources/containers/subresources/applications/methods/get)

GET/accounts/{account\_id}/containers/applications/{application\_id}

##### [Modify an application](https://developers.cloudflare.com/api/resources/containers/subresources/applications/methods/edit)

PATCH/accounts/{account\_id}/containers/applications/{application\_id}

##### [Delete a single application by id](https://developers.cloudflare.com/api/resources/containers/subresources/applications/methods/delete)

DELETE/accounts/{account\_id}/containers/applications/{application\_id}

##### ModelsExpand Collapse

<details>

<summary>

ApplicationListResponse = object {id, account\_id, configuration, 13 more } or object {id, account\_id, created\_at, 7 more }

The public Containers API returns an application.

</summary>

One of the following:

<details>

<summary>

CcScheduledApplication object {id, account\_id, configuration, 13 more }

Describes an application and the parameters that govern how it places its instances.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: object {image, authorized\_keys, command, 4 more }

User-specified container configuration.

</summary>

image: string

Image url.

<a href="#">Link to this property</a>

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

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

instances: number

Number of deployments to create.

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

<details>

<summary>

scheduling\_policy: "default"or "durable\_object"

The scheduling policy to use for an application.

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"durable\_object"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

version: number

<a href="#">Link to this property</a>

active\_rollout\_id: optional string

An identifier for a specific rollout within an application.

<a href="#">Link to this property</a>

<details>

<summary>

constraints: optional object {jurisdiction, regions }

</summary>

jurisdiction: optional string

Restricts placement to datacenters in the selected jurisdiction. Choose “eu”, “fedramp”, or “us”. When combined with regions, EU supports EEUR and WEUR while FedRAMP and US support ENAM and WNAM.

<a href="#">Link to this property</a>

regions: optional array of string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: optional object {namespace\_id }

Durable object configuration stored on and returned from a Cloudchamber application.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {errors, instances, summary }

</summary>

<details>

<summary>

errors: array of object {event, instance\_id }

</summary>

<details>

<summary>

event: object {id, details, message, 4 more }

An event within a Placement or a Job.

</summary>

id: string

<a href="#">Link to this property</a>

details: map\[unknown]

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

name: "SchedulerPlaced"or "NetworkingIPAssigned"or "VMStarted"or 14 more

Name of the event that describes the kind event that happened.

- SchedulerPlaced: It’s the first event that creates a container placement. It happens when the Containers runtime was able to retrieve deployment resources and start verifying everything is correct.
- NetworkingIPAssigned: It’s sent when the Containers runtime maps the IP to the container.
- VMStarted: It’s sent when the Containers runtime starts the VM. The container might remain unhealthy at this point.
- ImagePulled: It’s sent when the Containers runtime pulls the image successfully.
- ImagePullError: It’s sent when the Containers runtime is having issues pulling the image. The message and details have more information on what happened for debugging.
- VMFailedToStart: It’s sent when the Containers runtime was unable to boot the VM.
- VMStopping: It’s sent when the scheduler is stopping the VM.
- VMStopped: It’s sent when the VM finally exits.
- VMFailed: It’s sent when the scheduling of the VM failed in the current location.
- RuntimeStartFailed: It’s sent when the runtime hits an internal error.
- SSHStarted: It’s sent when the container gains network connectivity and opens the SSH port. Containers only send this event when SSH keys exist.
- CheckUpdate: Sent when the status of a health or readiness check changes. This may also affect the health status of the placement.
- DurableObjectConnected: Sent when a durable object instance connects and gains control of the deployment. This event is only sent for durable object deployments. It is sent after VMStarted.
- ContainerStarted: It’s sent when the container starts running.

</summary>

One of the following:

"SchedulerPlaced"

<a href="#">Link to this property</a>

"NetworkingIPAssigned"

<a href="#">Link to this property</a>

"VMStarted"

<a href="#">Link to this property</a>

"ImagePulled"

<a href="#">Link to this property</a>

"ImagePullError"

<a href="#">Link to this property</a>

"VMFailedToStart"

<a href="#">Link to this property</a>

"NetworkingIPAssignmentFailed"

<a href="#">Link to this property</a>

"VMRunning"

<a href="#">Link to this property</a>

"VMStopping"

<a href="#">Link to this property</a>

"VMStopped"

<a href="#">Link to this property</a>

"VMFailed"

<a href="#">Link to this property</a>

"RuntimeStartFailed"

<a href="#">Link to this property</a>

"SSHStarted"

<a href="#">Link to this property</a>

"ServiceHealthUpdates"

<a href="#">Link to this property</a>

"CheckUpdate"

<a href="#">Link to this property</a>

"DurableObjectConnected"

<a href="#">Link to this property</a>

"ContainerStarted"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusChange: map\[unknown]

<a href="#">Link to this property</a>

time: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

type: "Info"or "Error"or "Warn"or 2 more

</summary>

One of the following:

"Info"

<a href="#">Link to this property</a>

"Error"

<a href="#">Link to this property</a>

"Warn"

<a href="#">Link to this property</a>

"UserError"

<a href="#">Link to this property</a>

"SystemError"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

instance\_id: string

An instance ID represents an identifier of an instance configuration that maintains an underlying placement.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

instances: object {active, assigned }

Shows a count of application instance states.

</summary>

active: number

Number of instances whose runtime reports the container as running (container\_status = “running”). This is a subset of the placements that remain up: an instance that is already bound to a Durable Object and serving traffic is counted under “assigned” until its container\_status catches up to “running”, so container\_status can briefly lag Durable Object attachment under churn. To estimate running, Durable-Object-bound instances, sum “active” + “assigned” rather than reading “active” alone.

<a href="#">Link to this property</a>

assigned: number

Number of instances bound to a Durable Object with a running placement whose container\_status remains behind “running”. These count as live, serving instances; “active” + “assigned” approximates the running, Durable-Object-bound count.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

summary: optional "healthy"or "degraded"or "unhealthy"or "pending"

High-level health assessment. Only populated for “new\_instances” strategy. Based on a sample of target-version instances rather than a full count.

- “pending”: Zero target-version instances exist yet.
- “healthy”: Every sampled target-version instance reports running or active.
- “degraded”: Some sampled instances remain starting or scheduling.
- “unhealthy”: One or more sampled instances have failed.

</summary>

One of the following:

"healthy"

<a href="#">Link to this property</a>

"degraded"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"pending"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_instances: optional number

Maximum number of instances the application allows. This is relevant for applications that auto-scale.

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Top-level observability settings for the application. This field is mutually exclusive with configuration.observability.

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

rollout\_active\_grace\_period: optional number

Grace period for active instances to stay alive before becoming eligible for shutdown signal due to a rollout, in seconds. Defaults to 0.

maximum604800

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CcDurableObjectApplication object {id, account\_id, created\_at, 7 more }

Each Durable Object creates and manages the lifecycle of its container instance.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: object {namespace\_id }

Durable object configuration using a namespace ID.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

scheduling\_policy: "durable\_object"

Selects a Durable Object-managed application. Each Durable Object creates and manages the lifecycle of its container instance. Configure application-wide observability settings here. Deployment configuration, scaling, placement constraints, versions, and rollouts do not apply.

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: optional object {authorized\_keys, wrangler\_ssh }

Application-wide settings for a Durable Object-managed application.

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

<details>

<summary>

wrangler\_ssh: optional object {enabled, port }

Configuration properties for connecting with SSH to a container using Wrangler.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

port: optional number

maximum65535

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {instances, summary }

Aggregate current activity for the latest observed placement of each instance. Runtime snapshots feed periodic background sweeps. Counts refresh after each complete sweep. Instance listings retain their separate three-month history for failure discovery.

</summary>

<details>

<summary>

instances: object {active, starting }

Counts of observed non-terminal instances.

</summary>

active: number

Number of instances whose runtime reports running or stopping.

minimum0

<a href="#">Link to this property</a>

starting: number

Number of instances whose runtime reports starting.

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summary: optional "pending"

Present as pending until the first activity sweep completes; omitted afterward.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Application-wide logging settings for a Durable Object-managed application. The application publishes these settings to its runtime metadata. Updating them does not create a deployment or rollout.

</summary>

<details>

<summary>

logs: optional object {enabled }

Application-wide logging settings.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications%20%3E%20(model)%20application_list_response%20%3E%20(schema)>)

<details>

<summary>

ApplicationCreateResponse = object {id, account\_id, configuration, 13 more } or object {id, account\_id, created\_at, 7 more }

The public Containers API returns an application.

</summary>

One of the following:

<details>

<summary>

CcScheduledApplication object {id, account\_id, configuration, 13 more }

Describes an application and the parameters that govern how it places its instances.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: object {image, authorized\_keys, command, 4 more }

User-specified container configuration.

</summary>

image: string

Image url.

<a href="#">Link to this property</a>

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

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

instances: number

Number of deployments to create.

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

<details>

<summary>

scheduling\_policy: "default"or "durable\_object"

The scheduling policy to use for an application.

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"durable\_object"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

version: number

<a href="#">Link to this property</a>

active\_rollout\_id: optional string

An identifier for a specific rollout within an application.

<a href="#">Link to this property</a>

<details>

<summary>

constraints: optional object {jurisdiction, regions }

</summary>

jurisdiction: optional string

Restricts placement to datacenters in the selected jurisdiction. Choose “eu”, “fedramp”, or “us”. When combined with regions, EU supports EEUR and WEUR while FedRAMP and US support ENAM and WNAM.

<a href="#">Link to this property</a>

regions: optional array of string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: optional object {namespace\_id }

Durable object configuration stored on and returned from a Cloudchamber application.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {errors, instances, summary }

</summary>

<details>

<summary>

errors: array of object {event, instance\_id }

</summary>

<details>

<summary>

event: object {id, details, message, 4 more }

An event within a Placement or a Job.

</summary>

id: string

<a href="#">Link to this property</a>

details: map\[unknown]

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

name: "SchedulerPlaced"or "NetworkingIPAssigned"or "VMStarted"or 14 more

Name of the event that describes the kind event that happened.

- SchedulerPlaced: It’s the first event that creates a container placement. It happens when the Containers runtime was able to retrieve deployment resources and start verifying everything is correct.
- NetworkingIPAssigned: It’s sent when the Containers runtime maps the IP to the container.
- VMStarted: It’s sent when the Containers runtime starts the VM. The container might remain unhealthy at this point.
- ImagePulled: It’s sent when the Containers runtime pulls the image successfully.
- ImagePullError: It’s sent when the Containers runtime is having issues pulling the image. The message and details have more information on what happened for debugging.
- VMFailedToStart: It’s sent when the Containers runtime was unable to boot the VM.
- VMStopping: It’s sent when the scheduler is stopping the VM.
- VMStopped: It’s sent when the VM finally exits.
- VMFailed: It’s sent when the scheduling of the VM failed in the current location.
- RuntimeStartFailed: It’s sent when the runtime hits an internal error.
- SSHStarted: It’s sent when the container gains network connectivity and opens the SSH port. Containers only send this event when SSH keys exist.
- CheckUpdate: Sent when the status of a health or readiness check changes. This may also affect the health status of the placement.
- DurableObjectConnected: Sent when a durable object instance connects and gains control of the deployment. This event is only sent for durable object deployments. It is sent after VMStarted.
- ContainerStarted: It’s sent when the container starts running.

</summary>

One of the following:

"SchedulerPlaced"

<a href="#">Link to this property</a>

"NetworkingIPAssigned"

<a href="#">Link to this property</a>

"VMStarted"

<a href="#">Link to this property</a>

"ImagePulled"

<a href="#">Link to this property</a>

"ImagePullError"

<a href="#">Link to this property</a>

"VMFailedToStart"

<a href="#">Link to this property</a>

"NetworkingIPAssignmentFailed"

<a href="#">Link to this property</a>

"VMRunning"

<a href="#">Link to this property</a>

"VMStopping"

<a href="#">Link to this property</a>

"VMStopped"

<a href="#">Link to this property</a>

"VMFailed"

<a href="#">Link to this property</a>

"RuntimeStartFailed"

<a href="#">Link to this property</a>

"SSHStarted"

<a href="#">Link to this property</a>

"ServiceHealthUpdates"

<a href="#">Link to this property</a>

"CheckUpdate"

<a href="#">Link to this property</a>

"DurableObjectConnected"

<a href="#">Link to this property</a>

"ContainerStarted"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusChange: map\[unknown]

<a href="#">Link to this property</a>

time: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

type: "Info"or "Error"or "Warn"or 2 more

</summary>

One of the following:

"Info"

<a href="#">Link to this property</a>

"Error"

<a href="#">Link to this property</a>

"Warn"

<a href="#">Link to this property</a>

"UserError"

<a href="#">Link to this property</a>

"SystemError"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

instance\_id: string

An instance ID represents an identifier of an instance configuration that maintains an underlying placement.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

instances: object {active, assigned }

Shows a count of application instance states.

</summary>

active: number

Number of instances whose runtime reports the container as running (container\_status = “running”). This is a subset of the placements that remain up: an instance that is already bound to a Durable Object and serving traffic is counted under “assigned” until its container\_status catches up to “running”, so container\_status can briefly lag Durable Object attachment under churn. To estimate running, Durable-Object-bound instances, sum “active” + “assigned” rather than reading “active” alone.

<a href="#">Link to this property</a>

assigned: number

Number of instances bound to a Durable Object with a running placement whose container\_status remains behind “running”. These count as live, serving instances; “active” + “assigned” approximates the running, Durable-Object-bound count.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

summary: optional "healthy"or "degraded"or "unhealthy"or "pending"

High-level health assessment. Only populated for “new\_instances” strategy. Based on a sample of target-version instances rather than a full count.

- “pending”: Zero target-version instances exist yet.
- “healthy”: Every sampled target-version instance reports running or active.
- “degraded”: Some sampled instances remain starting or scheduling.
- “unhealthy”: One or more sampled instances have failed.

</summary>

One of the following:

"healthy"

<a href="#">Link to this property</a>

"degraded"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"pending"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_instances: optional number

Maximum number of instances the application allows. This is relevant for applications that auto-scale.

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Top-level observability settings for the application. This field is mutually exclusive with configuration.observability.

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

rollout\_active\_grace\_period: optional number

Grace period for active instances to stay alive before becoming eligible for shutdown signal due to a rollout, in seconds. Defaults to 0.

maximum604800

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CcDurableObjectApplication object {id, account\_id, created\_at, 7 more }

Each Durable Object creates and manages the lifecycle of its container instance.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: object {namespace\_id }

Durable object configuration using a namespace ID.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

scheduling\_policy: "durable\_object"

Selects a Durable Object-managed application. Each Durable Object creates and manages the lifecycle of its container instance. Configure application-wide observability settings here. Deployment configuration, scaling, placement constraints, versions, and rollouts do not apply.

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: optional object {authorized\_keys, wrangler\_ssh }

Application-wide settings for a Durable Object-managed application.

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

<details>

<summary>

wrangler\_ssh: optional object {enabled, port }

Configuration properties for connecting with SSH to a container using Wrangler.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

port: optional number

maximum65535

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {instances, summary }

Aggregate current activity for the latest observed placement of each instance. Runtime snapshots feed periodic background sweeps. Counts refresh after each complete sweep. Instance listings retain their separate three-month history for failure discovery.

</summary>

<details>

<summary>

instances: object {active, starting }

Counts of observed non-terminal instances.

</summary>

active: number

Number of instances whose runtime reports running or stopping.

minimum0

<a href="#">Link to this property</a>

starting: number

Number of instances whose runtime reports starting.

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summary: optional "pending"

Present as pending until the first activity sweep completes; omitted afterward.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Application-wide logging settings for a Durable Object-managed application. The application publishes these settings to its runtime metadata. Updating them does not create a deployment or rollout.

</summary>

<details>

<summary>

logs: optional object {enabled }

Application-wide logging settings.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications%20%3E%20(model)%20application_create_response%20%3E%20(schema)>)

<details>

<summary>

ApplicationGetResponse = object {id, account\_id, configuration, 13 more } or object {id, account\_id, created\_at, 7 more }

The public Containers API returns an application.

</summary>

One of the following:

<details>

<summary>

CcScheduledApplication object {id, account\_id, configuration, 13 more }

Describes an application and the parameters that govern how it places its instances.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: object {image, authorized\_keys, command, 4 more }

User-specified container configuration.

</summary>

image: string

Image url.

<a href="#">Link to this property</a>

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

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

instances: number

Number of deployments to create.

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

<details>

<summary>

scheduling\_policy: "default"or "durable\_object"

The scheduling policy to use for an application.

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"durable\_object"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

version: number

<a href="#">Link to this property</a>

active\_rollout\_id: optional string

An identifier for a specific rollout within an application.

<a href="#">Link to this property</a>

<details>

<summary>

constraints: optional object {jurisdiction, regions }

</summary>

jurisdiction: optional string

Restricts placement to datacenters in the selected jurisdiction. Choose “eu”, “fedramp”, or “us”. When combined with regions, EU supports EEUR and WEUR while FedRAMP and US support ENAM and WNAM.

<a href="#">Link to this property</a>

regions: optional array of string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: optional object {namespace\_id }

Durable object configuration stored on and returned from a Cloudchamber application.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {errors, instances, summary }

</summary>

<details>

<summary>

errors: array of object {event, instance\_id }

</summary>

<details>

<summary>

event: object {id, details, message, 4 more }

An event within a Placement or a Job.

</summary>

id: string

<a href="#">Link to this property</a>

details: map\[unknown]

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

name: "SchedulerPlaced"or "NetworkingIPAssigned"or "VMStarted"or 14 more

Name of the event that describes the kind event that happened.

- SchedulerPlaced: It’s the first event that creates a container placement. It happens when the Containers runtime was able to retrieve deployment resources and start verifying everything is correct.
- NetworkingIPAssigned: It’s sent when the Containers runtime maps the IP to the container.
- VMStarted: It’s sent when the Containers runtime starts the VM. The container might remain unhealthy at this point.
- ImagePulled: It’s sent when the Containers runtime pulls the image successfully.
- ImagePullError: It’s sent when the Containers runtime is having issues pulling the image. The message and details have more information on what happened for debugging.
- VMFailedToStart: It’s sent when the Containers runtime was unable to boot the VM.
- VMStopping: It’s sent when the scheduler is stopping the VM.
- VMStopped: It’s sent when the VM finally exits.
- VMFailed: It’s sent when the scheduling of the VM failed in the current location.
- RuntimeStartFailed: It’s sent when the runtime hits an internal error.
- SSHStarted: It’s sent when the container gains network connectivity and opens the SSH port. Containers only send this event when SSH keys exist.
- CheckUpdate: Sent when the status of a health or readiness check changes. This may also affect the health status of the placement.
- DurableObjectConnected: Sent when a durable object instance connects and gains control of the deployment. This event is only sent for durable object deployments. It is sent after VMStarted.
- ContainerStarted: It’s sent when the container starts running.

</summary>

One of the following:

"SchedulerPlaced"

<a href="#">Link to this property</a>

"NetworkingIPAssigned"

<a href="#">Link to this property</a>

"VMStarted"

<a href="#">Link to this property</a>

"ImagePulled"

<a href="#">Link to this property</a>

"ImagePullError"

<a href="#">Link to this property</a>

"VMFailedToStart"

<a href="#">Link to this property</a>

"NetworkingIPAssignmentFailed"

<a href="#">Link to this property</a>

"VMRunning"

<a href="#">Link to this property</a>

"VMStopping"

<a href="#">Link to this property</a>

"VMStopped"

<a href="#">Link to this property</a>

"VMFailed"

<a href="#">Link to this property</a>

"RuntimeStartFailed"

<a href="#">Link to this property</a>

"SSHStarted"

<a href="#">Link to this property</a>

"ServiceHealthUpdates"

<a href="#">Link to this property</a>

"CheckUpdate"

<a href="#">Link to this property</a>

"DurableObjectConnected"

<a href="#">Link to this property</a>

"ContainerStarted"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusChange: map\[unknown]

<a href="#">Link to this property</a>

time: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

type: "Info"or "Error"or "Warn"or 2 more

</summary>

One of the following:

"Info"

<a href="#">Link to this property</a>

"Error"

<a href="#">Link to this property</a>

"Warn"

<a href="#">Link to this property</a>

"UserError"

<a href="#">Link to this property</a>

"SystemError"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

instance\_id: string

An instance ID represents an identifier of an instance configuration that maintains an underlying placement.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

instances: object {active, assigned }

Shows a count of application instance states.

</summary>

active: number

Number of instances whose runtime reports the container as running (container\_status = “running”). This is a subset of the placements that remain up: an instance that is already bound to a Durable Object and serving traffic is counted under “assigned” until its container\_status catches up to “running”, so container\_status can briefly lag Durable Object attachment under churn. To estimate running, Durable-Object-bound instances, sum “active” + “assigned” rather than reading “active” alone.

<a href="#">Link to this property</a>

assigned: number

Number of instances bound to a Durable Object with a running placement whose container\_status remains behind “running”. These count as live, serving instances; “active” + “assigned” approximates the running, Durable-Object-bound count.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

summary: optional "healthy"or "degraded"or "unhealthy"or "pending"

High-level health assessment. Only populated for “new\_instances” strategy. Based on a sample of target-version instances rather than a full count.

- “pending”: Zero target-version instances exist yet.
- “healthy”: Every sampled target-version instance reports running or active.
- “degraded”: Some sampled instances remain starting or scheduling.
- “unhealthy”: One or more sampled instances have failed.

</summary>

One of the following:

"healthy"

<a href="#">Link to this property</a>

"degraded"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"pending"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_instances: optional number

Maximum number of instances the application allows. This is relevant for applications that auto-scale.

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Top-level observability settings for the application. This field is mutually exclusive with configuration.observability.

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

rollout\_active\_grace\_period: optional number

Grace period for active instances to stay alive before becoming eligible for shutdown signal due to a rollout, in seconds. Defaults to 0.

maximum604800

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CcDurableObjectApplication object {id, account\_id, created\_at, 7 more }

Each Durable Object creates and manages the lifecycle of its container instance.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: object {namespace\_id }

Durable object configuration using a namespace ID.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

scheduling\_policy: "durable\_object"

Selects a Durable Object-managed application. Each Durable Object creates and manages the lifecycle of its container instance. Configure application-wide observability settings here. Deployment configuration, scaling, placement constraints, versions, and rollouts do not apply.

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: optional object {authorized\_keys, wrangler\_ssh }

Application-wide settings for a Durable Object-managed application.

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

<details>

<summary>

wrangler\_ssh: optional object {enabled, port }

Configuration properties for connecting with SSH to a container using Wrangler.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

port: optional number

maximum65535

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {instances, summary }

Aggregate current activity for the latest observed placement of each instance. Runtime snapshots feed periodic background sweeps. Counts refresh after each complete sweep. Instance listings retain their separate three-month history for failure discovery.

</summary>

<details>

<summary>

instances: object {active, starting }

Counts of observed non-terminal instances.

</summary>

active: number

Number of instances whose runtime reports running or stopping.

minimum0

<a href="#">Link to this property</a>

starting: number

Number of instances whose runtime reports starting.

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summary: optional "pending"

Present as pending until the first activity sweep completes; omitted afterward.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Application-wide logging settings for a Durable Object-managed application. The application publishes these settings to its runtime metadata. Updating them does not create a deployment or rollout.

</summary>

<details>

<summary>

logs: optional object {enabled }

Application-wide logging settings.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications%20%3E%20(model)%20application_get_response%20%3E%20(schema)>)

<details>

<summary>

ApplicationEditResponse = object {id, account\_id, configuration, 13 more } or object {id, account\_id, created\_at, 7 more }

The public Containers API returns an application.

</summary>

One of the following:

<details>

<summary>

CcScheduledApplication object {id, account\_id, configuration, 13 more }

Describes an application and the parameters that govern how it places its instances.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: object {image, authorized\_keys, command, 4 more }

User-specified container configuration.

</summary>

image: string

Image url.

<a href="#">Link to this property</a>

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

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

instances: number

Number of deployments to create.

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

<details>

<summary>

scheduling\_policy: "default"or "durable\_object"

The scheduling policy to use for an application.

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"durable\_object"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

version: number

<a href="#">Link to this property</a>

active\_rollout\_id: optional string

An identifier for a specific rollout within an application.

<a href="#">Link to this property</a>

<details>

<summary>

constraints: optional object {jurisdiction, regions }

</summary>

jurisdiction: optional string

Restricts placement to datacenters in the selected jurisdiction. Choose “eu”, “fedramp”, or “us”. When combined with regions, EU supports EEUR and WEUR while FedRAMP and US support ENAM and WNAM.

<a href="#">Link to this property</a>

regions: optional array of string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: optional object {namespace\_id }

Durable object configuration stored on and returned from a Cloudchamber application.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {errors, instances, summary }

</summary>

<details>

<summary>

errors: array of object {event, instance\_id }

</summary>

<details>

<summary>

event: object {id, details, message, 4 more }

An event within a Placement or a Job.

</summary>

id: string

<a href="#">Link to this property</a>

details: map\[unknown]

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

name: "SchedulerPlaced"or "NetworkingIPAssigned"or "VMStarted"or 14 more

Name of the event that describes the kind event that happened.

- SchedulerPlaced: It’s the first event that creates a container placement. It happens when the Containers runtime was able to retrieve deployment resources and start verifying everything is correct.
- NetworkingIPAssigned: It’s sent when the Containers runtime maps the IP to the container.
- VMStarted: It’s sent when the Containers runtime starts the VM. The container might remain unhealthy at this point.
- ImagePulled: It’s sent when the Containers runtime pulls the image successfully.
- ImagePullError: It’s sent when the Containers runtime is having issues pulling the image. The message and details have more information on what happened for debugging.
- VMFailedToStart: It’s sent when the Containers runtime was unable to boot the VM.
- VMStopping: It’s sent when the scheduler is stopping the VM.
- VMStopped: It’s sent when the VM finally exits.
- VMFailed: It’s sent when the scheduling of the VM failed in the current location.
- RuntimeStartFailed: It’s sent when the runtime hits an internal error.
- SSHStarted: It’s sent when the container gains network connectivity and opens the SSH port. Containers only send this event when SSH keys exist.
- CheckUpdate: Sent when the status of a health or readiness check changes. This may also affect the health status of the placement.
- DurableObjectConnected: Sent when a durable object instance connects and gains control of the deployment. This event is only sent for durable object deployments. It is sent after VMStarted.
- ContainerStarted: It’s sent when the container starts running.

</summary>

One of the following:

"SchedulerPlaced"

<a href="#">Link to this property</a>

"NetworkingIPAssigned"

<a href="#">Link to this property</a>

"VMStarted"

<a href="#">Link to this property</a>

"ImagePulled"

<a href="#">Link to this property</a>

"ImagePullError"

<a href="#">Link to this property</a>

"VMFailedToStart"

<a href="#">Link to this property</a>

"NetworkingIPAssignmentFailed"

<a href="#">Link to this property</a>

"VMRunning"

<a href="#">Link to this property</a>

"VMStopping"

<a href="#">Link to this property</a>

"VMStopped"

<a href="#">Link to this property</a>

"VMFailed"

<a href="#">Link to this property</a>

"RuntimeStartFailed"

<a href="#">Link to this property</a>

"SSHStarted"

<a href="#">Link to this property</a>

"ServiceHealthUpdates"

<a href="#">Link to this property</a>

"CheckUpdate"

<a href="#">Link to this property</a>

"DurableObjectConnected"

<a href="#">Link to this property</a>

"ContainerStarted"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusChange: map\[unknown]

<a href="#">Link to this property</a>

time: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

type: "Info"or "Error"or "Warn"or 2 more

</summary>

One of the following:

"Info"

<a href="#">Link to this property</a>

"Error"

<a href="#">Link to this property</a>

"Warn"

<a href="#">Link to this property</a>

"UserError"

<a href="#">Link to this property</a>

"SystemError"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

instance\_id: string

An instance ID represents an identifier of an instance configuration that maintains an underlying placement.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

instances: object {active, assigned }

Shows a count of application instance states.

</summary>

active: number

Number of instances whose runtime reports the container as running (container\_status = “running”). This is a subset of the placements that remain up: an instance that is already bound to a Durable Object and serving traffic is counted under “assigned” until its container\_status catches up to “running”, so container\_status can briefly lag Durable Object attachment under churn. To estimate running, Durable-Object-bound instances, sum “active” + “assigned” rather than reading “active” alone.

<a href="#">Link to this property</a>

assigned: number

Number of instances bound to a Durable Object with a running placement whose container\_status remains behind “running”. These count as live, serving instances; “active” + “assigned” approximates the running, Durable-Object-bound count.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

summary: optional "healthy"or "degraded"or "unhealthy"or "pending"

High-level health assessment. Only populated for “new\_instances” strategy. Based on a sample of target-version instances rather than a full count.

- “pending”: Zero target-version instances exist yet.
- “healthy”: Every sampled target-version instance reports running or active.
- “degraded”: Some sampled instances remain starting or scheduling.
- “unhealthy”: One or more sampled instances have failed.

</summary>

One of the following:

"healthy"

<a href="#">Link to this property</a>

"degraded"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"pending"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_instances: optional number

Maximum number of instances the application allows. This is relevant for applications that auto-scale.

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Top-level observability settings for the application. This field is mutually exclusive with configuration.observability.

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

rollout\_active\_grace\_period: optional number

Grace period for active instances to stay alive before becoming eligible for shutdown signal due to a rollout, in seconds. Defaults to 0.

maximum604800

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CcDurableObjectApplication object {id, account\_id, created\_at, 7 more }

Each Durable Object creates and manages the lifecycle of its container instance.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: object {namespace\_id }

Durable object configuration using a namespace ID.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

scheduling\_policy: "durable\_object"

Selects a Durable Object-managed application. Each Durable Object creates and manages the lifecycle of its container instance. Configure application-wide observability settings here. Deployment configuration, scaling, placement constraints, versions, and rollouts do not apply.

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: optional object {authorized\_keys, wrangler\_ssh }

Application-wide settings for a Durable Object-managed application.

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

<details>

<summary>

wrangler\_ssh: optional object {enabled, port }

Configuration properties for connecting with SSH to a container using Wrangler.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

port: optional number

maximum65535

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {instances, summary }

Aggregate current activity for the latest observed placement of each instance. Runtime snapshots feed periodic background sweeps. Counts refresh after each complete sweep. Instance listings retain their separate three-month history for failure discovery.

</summary>

<details>

<summary>

instances: object {active, starting }

Counts of observed non-terminal instances.

</summary>

active: number

Number of instances whose runtime reports running or stopping.

minimum0

<a href="#">Link to this property</a>

starting: number

Number of instances whose runtime reports starting.

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summary: optional "pending"

Present as pending until the first activity sweep completes; omitted afterward.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Application-wide logging settings for a Durable Object-managed application. The application publishes these settings to its runtime metadata. Updating them does not create a deployment or rollout.

</summary>

<details>

<summary>

logs: optional object {enabled }

Application-wide logging settings.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications%20%3E%20(model)%20application_edit_response%20%3E%20(schema)>)

<details>

<summary>

ApplicationDeleteResponse object {message }

Result of starting asynchronous deletion for a Containers application.

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications%20%3E%20(model)%20application_delete_response%20%3E%20(schema)>)

#### ApplicationsInstances

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

#### ApplicationsRollouts

##### [Create a new rollout for an application](https://developers.cloudflare.com/api/resources/containers/subresources/applications/subresources/rollouts/methods/create)

POST/accounts/{account\_id}/containers/applications/{application\_id}/rollouts

##### ModelsExpand Collapse

<details>

<summary>

RolloutCreateResponse object {id, created\_at, current\_configuration, 14 more }

Represents the status and metadata of a rollout process for an application. For “rolling” strategy: includes steps and progress with instance counts. For “new\_instances” strategy: the response omits steps and progress. Use percentage, version\_distribution, and health.summary for status.

</summary>

id: string

An identifier for a specific rollout within an application.

<a href="#">Link to this property</a>

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

current\_configuration: object {authorized\_keys, command, entrypoint, 4 more }

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

current\_version: number

Current application version before the rollout.

<a href="#">Link to this property</a>

description: string

<a href="#">Link to this property</a>

<details>

<summary>

health: object {errors, instances, summary }

</summary>

<details>

<summary>

errors: array of object {event, instance\_id }

</summary>

<details>

<summary>

event: object {id, details, message, 4 more }

An event within a Placement or a Job.

</summary>

id: string

<a href="#">Link to this property</a>

details: map\[unknown]

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

name: "SchedulerPlaced"or "NetworkingIPAssigned"or "VMStarted"or 14 more

Name of the event that describes the kind event that happened.

- SchedulerPlaced: It’s the first event that creates a container placement. It happens when the Containers runtime was able to retrieve deployment resources and start verifying everything is correct.
- NetworkingIPAssigned: It’s sent when the Containers runtime maps the IP to the container.
- VMStarted: It’s sent when the Containers runtime starts the VM. The container might remain unhealthy at this point.
- ImagePulled: It’s sent when the Containers runtime pulls the image successfully.
- ImagePullError: It’s sent when the Containers runtime is having issues pulling the image. The message and details have more information on what happened for debugging.
- VMFailedToStart: It’s sent when the Containers runtime was unable to boot the VM.
- VMStopping: It’s sent when the scheduler is stopping the VM.
- VMStopped: It’s sent when the VM finally exits.
- VMFailed: It’s sent when the scheduling of the VM failed in the current location.
- RuntimeStartFailed: It’s sent when the runtime hits an internal error.
- SSHStarted: It’s sent when the container gains network connectivity and opens the SSH port. Containers only send this event when SSH keys exist.
- CheckUpdate: Sent when the status of a health or readiness check changes. This may also affect the health status of the placement.
- DurableObjectConnected: Sent when a durable object instance connects and gains control of the deployment. This event is only sent for durable object deployments. It is sent after VMStarted.
- ContainerStarted: It’s sent when the container starts running.

</summary>

One of the following:

"SchedulerPlaced"

<a href="#">Link to this property</a>

"NetworkingIPAssigned"

<a href="#">Link to this property</a>

"VMStarted"

<a href="#">Link to this property</a>

"ImagePulled"

<a href="#">Link to this property</a>

"ImagePullError"

<a href="#">Link to this property</a>

"VMFailedToStart"

<a href="#">Link to this property</a>

"NetworkingIPAssignmentFailed"

<a href="#">Link to this property</a>

"VMRunning"

<a href="#">Link to this property</a>

"VMStopping"

<a href="#">Link to this property</a>

"VMStopped"

<a href="#">Link to this property</a>

"VMFailed"

<a href="#">Link to this property</a>

"RuntimeStartFailed"

<a href="#">Link to this property</a>

"SSHStarted"

<a href="#">Link to this property</a>

"ServiceHealthUpdates"

<a href="#">Link to this property</a>

"CheckUpdate"

<a href="#">Link to this property</a>

"DurableObjectConnected"

<a href="#">Link to this property</a>

"ContainerStarted"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusChange: map\[unknown]

<a href="#">Link to this property</a>

time: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

type: "Info"or "Error"or "Warn"or 2 more

</summary>

One of the following:

"Info"

<a href="#">Link to this property</a>

"Error"

<a href="#">Link to this property</a>

"Warn"

<a href="#">Link to this property</a>

"UserError"

<a href="#">Link to this property</a>

"SystemError"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

instance\_id: string

An instance ID represents an identifier of an instance configuration that maintains an underlying placement.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

instances: object {active, assigned }

Shows a count of application instance states.

</summary>

active: number

Number of instances whose runtime reports the container as running (container\_status = “running”). This is a subset of the placements that remain up: an instance that is already bound to a Durable Object and serving traffic is counted under “assigned” until its container\_status catches up to “running”, so container\_status can briefly lag Durable Object attachment under churn. To estimate running, Durable-Object-bound instances, sum “active” + “assigned” rather than reading “active” alone.

<a href="#">Link to this property</a>

assigned: number

Number of instances bound to a Durable Object with a running placement whose container\_status remains behind “running”. These count as live, serving instances; “active” + “assigned” approximates the running, Durable-Object-bound count.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

summary: optional "healthy"or "degraded"or "unhealthy"or "pending"

High-level health assessment. Only populated for “new\_instances” strategy. Based on a sample of target-version instances rather than a full count.

- “pending”: Zero target-version instances exist yet.
- “healthy”: Every sampled target-version instance reports running or active.
- “degraded”: Some sampled instances remain starting or scheduling.
- “unhealthy”: One or more sampled instances have failed.

</summary>

One of the following:

"healthy"

<a href="#">Link to this property</a>

"degraded"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"pending"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

kind: "full\_auto"or "full\_manual"or "durable\_objects\_auto"

Kind of the rollout process.

- “full\_auto”: For rolling rollouts, starts progressing steps upon rollout creation. For new\_instances rollouts, advances percentage targets automatically after target-version health is observed.
- “full\_manual”: Requires manually progressing each step in the rollout using the UpdateRollout’s action paramater.
- “durable\_objects\_auto”: Default when the application is a DO application.

</summary>

One of the following:

"full\_auto"

<a href="#">Link to this property</a>

"full\_manual"

<a href="#">Link to this property</a>

"durable\_objects\_auto"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

last\_updated\_at: string

Timestamp of the most recent update to status, health, or progress.

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "progressing"or "completed"or 2 more

Current status of the rollout.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"progressing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"reverted"

<a href="#">Link to this property</a>

"replaced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strategy: "rolling"or "new\_instances"

The rollout strategy.

- “rolling”: Step-based rollout with health gates. Actively replaces instances to reach each step’s target percentage. Response includes steps and progress.
- “new\_instances”: Percentage control over version distribution. Version sync actively replaces instances to match the configured percentage. “full\_auto” ramps through fixed percentage targets after target-version health is observed. Response includes percentage, version\_distribution, and health.summary.

</summary>

One of the following:

"rolling"

<a href="#">Link to this property</a>

"new\_instances"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

target\_configuration: object {authorized\_keys, command, entrypoint, 4 more }

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

target\_version: number

Target application version after the rollout is complete and applied to all current instances.

<a href="#">Link to this property</a>

percentage: optional number

Current target version percentage (0-100). Only present for “new\_instances” strategy.

<a href="#">Link to this property</a>

<details>

<summary>

progress: optional object {current\_step, total\_instances, total\_steps, 2 more }

Progress details of an application rollout.

</summary>

current\_step: number

Current step being executed in the rollout process. Initialized to 0.

<a href="#">Link to this property</a>

total\_instances: number

Total number of instances the rollout affects.

<a href="#">Link to this property</a>

total\_steps: number

Total number of steps in the rollout.

<a href="#">Link to this property</a>

updated\_instances: number

Number of instances updated in the rollout process.

<a href="#">Link to this property</a>

<details>

<summary>

version\_distribution: optional object {current\_version\_instances, current\_version\_percentage, target\_version\_instances, target\_version\_percentage }

Expected distribution of instances per version, based on the current percentage split. Populated during active rollouts. Values derive from the version percentage weights rather than actual running instance counts.

</summary>

current\_version\_instances: optional number

Expected number of instances remaining on the current (old) version based on the current percentage split. Only populated for “rolling” strategy.

<a href="#">Link to this property</a>

current\_version\_percentage: optional number

The percentage of new instances being scheduled on the current version (100 - target\_version\_percentage). Only populated for “new\_instances” strategy.

<a href="#">Link to this property</a>

target\_version\_instances: optional number

Expected number of instances scheduled for the target (new) version based on the current percentage split. Only populated for “rolling” strategy.

<a href="#">Link to this property</a>

target\_version\_percentage: optional number

The active percentage of new instances being scheduled on the target version. For “rolling”, this reflects the step\_size.percentage of the current active step. For “new\_instances”, this reflects the user-set percentage.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

started\_at: optional string

Timestamp when the rollout started.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

steps: optional array of object {id, description, status, 4 more }

</summary>

id: number

The sequential order of the rollout step, automatically assigned starting from 1, based on the total number of steps in the rollout process.

<a href="#">Link to this property</a>

description: string

Description of the rollout step.

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "progressing"or "reverting"or 2 more

Status of the rollout step.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"progressing"

<a href="#">Link to this property</a>

"reverting"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"reverted"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

step\_size: object {percentage }

</summary>

percentage: number

Percentage of instances affected in this step. Min 10% and Max 100%.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

completed\_at: optional string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

reason: optional string

Reason for the step’s current status.

<a href="#">Link to this property</a>

started\_at: optional string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

version\_distribution: optional object {current\_version\_percentage, target\_version\_percentage }

Version percentage distribution. Only present for “new\_instances” strategy. For “rolling” strategy, see progress.version\_distribution instead.

</summary>

current\_version\_percentage: number

Percentage of instances on the current (old) version.

<a href="#">Link to this property</a>

target\_version\_percentage: number

Percentage of instances on the target (new) version.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(model)%20rollout_create_response%20%3E%20(schema)>)

#### ApplicationsVersions

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