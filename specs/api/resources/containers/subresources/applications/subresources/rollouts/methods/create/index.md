---
title: Create a new rollout for an application
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Applications](https://developers.cloudflare.com/api/resources/containers/subresources/applications)

[Rollouts](https://developers.cloudflare.com/api/resources/containers/subresources/applications/subresources/rollouts)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Create a new rollout for an application

POST/accounts/{account\_id}/containers/applications/{application\_id}/rollouts

Creates a rollout to update the application’s configuration across instances with minimal downtime. Rollouts apply only to scheduler-backed applications with `scheduling_policy: "default"`. Versions and rollouts do not apply to applications with `scheduling_policy: "durable_object"`.

##### Security

<details>

<summary>API Token</summary>



The preferred authorization scheme for interacting with the Cloudflare API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/create-token/">Create a token</a>.

**Example:**<code>Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY</code>

</details>

<details>

<summary>API Email + API Key</summary>



The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**<code>X-Auth-Email: user@example.com</code>

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**<code>X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194</code>

</details>

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

application\_id: string

An Application ID represents an identifier of an application.

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20application_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

description: string

Description of the rollout process.

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20description%20%3E%20(schema)>)

<details>

<summary>

strategy: "rolling"or "new\_instances"

Strategy used for the rollout.

- “rolling”: Step-based rollout with health gates. Actively replaces instances to reach each step’s target percentage.
- “new\_instances”: Percentage control over version distribution. Version sync actively replaces instances to match the configured percentage. The “full\_auto” kind advances through fixed percentage targets after target-version health is observed.

</summary>

One of the following:

"rolling"

<a href="#">Link to this property</a>

"new\_instances"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20strategy%20%3E%20(schema)>)

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

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20target_configuration%20%3E%20(schema)>)

<details>

<summary>

kind: optional "full\_auto"or "full\_manual"

Kind of the rollout process. Defaults to “full\_auto”.

- “full\_auto”: For rolling rollouts, starts progressing steps upon rollout creation. For new\_instances rollouts, advances percentage targets automatically after target-version health is observed.
- “full\_manual”: Requires manually progressing each step in the rollout using the UpdateRollout’s action parameter.

</summary>

One of the following:

"full\_auto"

<a href="#">Link to this property</a>

"full\_manual"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20kind%20%3E%20(schema)>)

percentage: optional number

Initial target version percentage (0-100). Version sync actively replaces instances to match. Required when strategy is “new\_instances” and kind is “full\_manual”. When strategy is “new\_instances” and kind is “full\_auto”, omitted percentage starts at 10% or the smallest percentage that targets at least one instance. Unused for “rolling”.

maximum100

minimum0

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20percentage%20%3E%20(schema)>)

<details>

<summary>

step\_percentage: optional 5or 10or 20or 3 more

Percentage of rollout to increase in each step when “steps” is absent. Applicable values: 5, 10, 20, 25, 50, 100. These create rollouts with 20, 10, 5, 4, 2, 1 steps respectively. Only valid for “rolling” strategy.

</summary>

One of the following:

5

<a href="#">Link to this property</a>

10

<a href="#">Link to this property</a>

20

<a href="#">Link to this property</a>

25

<a href="#">Link to this property</a>

50

<a href="#">Link to this property</a>

100

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20step_percentage%20%3E%20(schema)>)

<details>

<summary>

steps: optional array of object {description, step\_size }

Steps defining the rollout process, used when “step\_percentage” is absent. Specify only one of “step\_percentage” or “steps” when creating a rollout. “steps” allow granular control over each step. Only valid for “rolling” strategy.

</summary>

description: string

Description of the rollout step.

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

</details>

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20steps%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, created\_at, current\_configuration, 14 more }

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

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20containers.applications.rollouts%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Create a new rollout for an application

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/containers/applications/$APPLICATION_ID/rollouts \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "description": "description",
          "strategy": "rolling",
          "target_configuration": {}
        }'
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "id",
    "created_at": "2021-04-01T12:32:41.488Z",
    "current_configuration": {
      "authorized_keys": [
        {
          "public_key": "public_key",
          "name": "name"
        }
      ],
      "command": [
        "myapp",
        "--default-option"
      ],
      "entrypoint": [
        "/bin/bash"
      ],
      "environment_variables": [
        {
          "name": "name",
          "value": "value"
        }
      ],
      "image": "image",
      "instance_type": "lite",
      "observability": {
        "logs": {
          "enabled": true
        }
      }
    },
    "current_version": 0,
    "description": "description",
    "health": {
      "errors": [
        {
          "event": {
            "id": "id",
            "details": {
              "foo": "bar"
            },
            "message": "message",
            "name": "SchedulerPlaced",
            "statusChange": {
              "foo": "bar"
            },
            "time": "2021-04-01T12:32:41.488Z",
            "type": "Info"
          },
          "instance_id": "instance_id"
        }
      ],
      "instances": {
        "active": 0,
        "assigned": 0
      },
      "summary": "healthy"
    },
    "kind": "full_auto",
    "last_updated_at": "2021-04-01T12:32:41.488Z",
    "status": "pending",
    "strategy": "rolling",
    "target_configuration": {
      "authorized_keys": [
        {
          "public_key": "public_key",
          "name": "name"
        }
      ],
      "command": [
        "myapp",
        "--default-option"
      ],
      "entrypoint": [
        "/bin/bash"
      ],
      "environment_variables": [
        {
          "name": "name",
          "value": "value"
        }
      ],
      "image": "image",
      "instance_type": "lite",
      "observability": {
        "logs": {
          "enabled": true
        }
      }
    },
    "target_version": 0,
    "percentage": 0,
    "progress": {
      "current_step": 0,
      "total_instances": 0,
      "total_steps": 0,
      "updated_instances": 0,
      "version_distribution": {
        "current_version_instances": 0,
        "current_version_percentage": 0,
        "target_version_instances": 0,
        "target_version_percentage": 0
      }
    },
    "started_at": "2019-12-27T18:11:19.117Z",
    "steps": [
      {
        "id": 0,
        "description": "description",
        "status": "pending",
        "step_size": {
          "percentage": 0
        },
        "completed_at": "2021-04-01T12:32:41.488Z",
        "reason": "reason",
        "started_at": "2021-04-01T12:32:41.488Z"
      }
    ],
    "version_distribution": {
      "current_version_percentage": 0,
      "target_version_percentage": 0
    }
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "id",
    "created_at": "2021-04-01T12:32:41.488Z",
    "current_configuration": {
      "authorized_keys": [
        {
          "public_key": "public_key",
          "name": "name"
        }
      ],
      "command": [
        "myapp",
        "--default-option"
      ],
      "entrypoint": [
        "/bin/bash"
      ],
      "environment_variables": [
        {
          "name": "name",
          "value": "value"
        }
      ],
      "image": "image",
      "instance_type": "lite",
      "observability": {
        "logs": {
          "enabled": true
        }
      }
    },
    "current_version": 0,
    "description": "description",
    "health": {
      "errors": [
        {
          "event": {
            "id": "id",
            "details": {
              "foo": "bar"
            },
            "message": "message",
            "name": "SchedulerPlaced",
            "statusChange": {
              "foo": "bar"
            },
            "time": "2021-04-01T12:32:41.488Z",
            "type": "Info"
          },
          "instance_id": "instance_id"
        }
      ],
      "instances": {
        "active": 0,
        "assigned": 0
      },
      "summary": "healthy"
    },
    "kind": "full_auto",
    "last_updated_at": "2021-04-01T12:32:41.488Z",
    "status": "pending",
    "strategy": "rolling",
    "target_configuration": {
      "authorized_keys": [
        {
          "public_key": "public_key",
          "name": "name"
        }
      ],
      "command": [
        "myapp",
        "--default-option"
      ],
      "entrypoint": [
        "/bin/bash"
      ],
      "environment_variables": [
        {
          "name": "name",
          "value": "value"
        }
      ],
      "image": "image",
      "instance_type": "lite",
      "observability": {
        "logs": {
          "enabled": true
        }
      }
    },
    "target_version": 0,
    "percentage": 0,
    "progress": {
      "current_step": 0,
      "total_instances": 0,
      "total_steps": 0,
      "updated_instances": 0,
      "version_distribution": {
        "current_version_instances": 0,
        "current_version_percentage": 0,
        "target_version_instances": 0,
        "target_version_percentage": 0
      }
    },
    "started_at": "2019-12-27T18:11:19.117Z",
    "steps": [
      {
        "id": 0,
        "description": "description",
        "status": "pending",
        "step_size": {
          "percentage": 0
        },
        "completed_at": "2021-04-01T12:32:41.488Z",
        "reason": "reason",
        "started_at": "2021-04-01T12:32:41.488Z"
      }
    ],
    "version_distribution": {
      "current_version_percentage": 0,
      "target_version_percentage": 0
    }
  },
  "success": true
}
```