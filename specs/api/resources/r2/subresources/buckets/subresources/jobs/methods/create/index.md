---
title: Create Bucket Job
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[R2](https://developers.cloudflare.com/api/resources/r2)

[Buckets](https://developers.cloudflare.com/api/resources/r2/subresources/buckets)

[Jobs](https://developers.cloudflare.com/api/resources/r2/subresources/buckets/subresources/jobs)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Create Bucket Job

POST/accounts/{account\_id}/r2/buckets/{bucket\_name}/jobs

Creates a background job for an R2 bucket. The `jobType` field selects the job:

- **`prefixDelete`**: deletes every object whose key begins with `prefix`. A non-empty prefix must end in `/`. An empty prefix ( `""`) empties the entire bucket.
- **`storageClassMigration`**: migrates every object in the bucket between storage classes. `sourceStorageClass` and `destinationStorageClass` must be provided together and must differ; omitting both migrates from `InfrequentAccess` to `Standard`.

Poll the returned `id` with the Get Bucket Job endpoint. Small prefix-delete jobs can finish synchronously and return `COMPLETED`. Objects uploaded after a background job starts are not affected by that job.

For prefix-delete jobs: abort active multipart uploads before submitting the request, since a synchronously completed job does not abort them, and avoid writing objects or starting multipart uploads while a bucket-emptying job is in progress. Each request creates a distinct job, and the number of active prefix-delete jobs is limited per bucket; wait for an existing job to finish before retrying a request rejected with HTTP 429. A bucket cannot be emptied while event notifications are configured (HTTP 409 / error code 10083). To protect a bucket with R2 Data Catalog enabled, send the `cf-r2-data-catalog-check` header; a conflict is returned with HTTP 409 / error code 10081.

Prefix-delete jobs require permission to delete objects; storage-class migration jobs require permission to write to the bucket.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Workers R2 Storage Write`

##### P ath ParametersExpand Collapse

account\_id: string

Cloudflare account ID that owns the R2 resource.

maxLength32

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20account_id%20%3E%20(schema)>)

bucket\_name: string

Name of the bucket.

maxLength64

minLength3

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20bucket_name%20%3E%20(schema)>)

##### H eader ParametersExpand Collapse

"cf-r2-data-catalog-check": optional string

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20cf-r2-data-catalog-check%20%3E%20(schema)>)

<details>

<summary>

"cf-r2-jurisdiction": optional "default"or "eu"or "us"or 2 more

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"eu"

<a href="#">Link to this property</a>

"us"

<a href="#">Link to this property</a>

"fedramp"

<a href="#">Link to this property</a>

"fedramp-high"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20cf-r2-jurisdiction%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

body: object {jobType, prefix } or object {jobType, destinationStorageClass, sourceStorageClass }

Request body that creates a prefix-delete job.

</summary>

One of the following:

<details>

<summary>

PrefixDelete object {jobType, prefix }

Request body that creates a prefix-delete job.

</summary>

jobType: "prefixDelete"

<a href="#">Link to this property</a>

prefix: string

Prefix matched against object keys. A non-empty value must end in <code>/</code>. An empty string empties the entire bucket.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

StorageClassMigration object {jobType, destinationStorageClass, sourceStorageClass }

Request body that creates a storage-class migration job.

</summary>

jobType: "storageClassMigration"

<a href="#">Link to this property</a>

<details>

<summary>

destinationStorageClass: optional "Standard"or "InfrequentAccess"

</summary>

One of the following:

"Standard"

<a href="#">Link to this property</a>

"InfrequentAccess"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

sourceStorageClass: optional "Standard"or "InfrequentAccess"

</summary>

One of the following:

"Standard"

<a href="#">Link to this property</a>

"InfrequentAccess"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20body%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20response_info%20%3E%20(schema)">ResponseInfo</a> { code, message, documentation\_url, source }

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

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

messages: array of string

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, jobType, prefixDelete, 3 more } or object {id, jobType, startTime, 3 more }

Descriptor of a bucket background job, discriminated by <code>jobType</code>. Returned by the Create Bucket Job, Get Bucket Job and List Bucket Jobs endpoints. A small operation can already be <code>COMPLETED</code> when it is returned.

</summary>

One of the following:

<details>

<summary>

PrefixDelete object {id, jobType, prefixDelete, 3 more }

Descriptor of a prefix-delete job. An empty prefix indicates a job that empties the whole bucket.

</summary>

id: string

Unique identifier used to poll the job.

<a href="#">Link to this property</a>

jobType: "prefixDelete"

The job kind.

<a href="#">Link to this property</a>

<details>

<summary>

prefixDelete: object {deletedObjects, prefix, isBucketClear }

Details specific to the prefix-delete job.

</summary>

deletedObjects: number

Number of objects deleted by the job so far.

<a href="#">Link to this property</a>

prefix: string

The prefix matched against object keys. An empty string means the entire bucket.

<a href="#">Link to this property</a>

isBucketClear: optional boolean

True when the job was created to clear the entire bucket. This field can be absent on jobs created before Empty Bucket job tracking was introduced.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

startTime: string

When the job was created.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

status: "ENQUEUED"or "RUNNING"or "COMPLETED"or 2 more

Lifecycle status of a bucket background job.

</summary>

One of the following:

"ENQUEUED"

<a href="#">Link to this property</a>

"RUNNING"

<a href="#">Link to this property</a>

"COMPLETED"

<a href="#">Link to this property</a>

"FAILED"

<a href="#">Link to this property</a>

"CANCELLED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

endTime: optional string

When the job finished. Absent while the job is still <code>ENQUEUED</code> or <code>RUNNING</code>.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

StorageClassMigration object {id, jobType, startTime, 3 more }

Descriptor of a bucket-wide storage-class migration job.

</summary>

id: string

Unique identifier used to poll the job.

<a href="#">Link to this property</a>

jobType: "storageClassMigration"

The job kind.

<a href="#">Link to this property</a>

startTime: string

When the job was created.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

status: "ENQUEUED"or "RUNNING"or "COMPLETED"or 2 more

Lifecycle status of a bucket background job.

</summary>

One of the following:

"ENQUEUED"

<a href="#">Link to this property</a>

"RUNNING"

<a href="#">Link to this property</a>

"COMPLETED"

<a href="#">Link to this property</a>

"FAILED"

<a href="#">Link to this property</a>

"CANCELLED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

storageClassMigration: object {destinationStorageClass, migratedObjects, sourceStorageClass, 6 more }

</summary>

<details>

<summary>

destinationStorageClass: "Standard"or "InfrequentAccess"

The storage class objects are migrated to. The source and destination storage classes always differ.

</summary>

One of the following:

"Standard"

<a href="#">Link to this property</a>

"InfrequentAccess"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

migratedObjects: number

Number of object versions migrated successfully.

minimum0

<a href="#">Link to this property</a>

<details>

<summary>

sourceStorageClass: "Standard"or "InfrequentAccess"

The storage class objects are migrated from.

</summary>

One of the following:

"Standard"

<a href="#">Link to this property</a>

"InfrequentAccess"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

failedBytes: optional number

Payload bytes belonging to failed object versions.

minimum0

<a href="#">Link to this property</a>

failedObjects: optional number

Number of object versions that failed migration.

minimum0

<a href="#">Link to this property</a>

migratedBytes: optional number

Object payload bytes migrated successfully. Present for Metadata Worker jobs.

minimum0

<a href="#">Link to this property</a>

migratedMetadataBytes: optional number

Object metadata bytes migrated successfully. Present for Metadata Worker jobs.

minimum0

<a href="#">Link to this property</a>

skippedBytes: optional number

Payload bytes belonging to skipped object versions.

minimum0

<a href="#">Link to this property</a>

skippedObjects: optional number

Number of object versions skipped.

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

endTime: optional string

When the job finished. Absent while the job is still <code>ENQUEUED</code> or <code>RUNNING</code>.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Whether the API call was successful.

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Create Bucket Job

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/r2/buckets/$BUCKET_NAME/jobs \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "jobType": "prefixDelete",
          "prefix": "path/to/"
        }'
```

200 example

200 example

200 example

409 example

429 example

```
{
  "errors": [],
  "messages": [],
  "result": {
    "endTime": "2026-07-20T12:00:00Z",
    "id": "69f94626-a3fe-47bc-9615-e791b4d53c53",
    "jobType": "prefixDelete",
    "prefixDelete": {
      "deletedObjects": 0,
      "isBucketClear": true,
      "prefix": ""
    },
    "startTime": "2026-07-20T12:00:00Z",
    "status": "COMPLETED"
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "id": "7f24658b-31d7-4b91-9a12-cb5a2c99b294",
    "jobType": "prefixDelete",
    "prefixDelete": {
      "deletedObjects": 0,
      "isBucketClear": true,
      "prefix": ""
    },
    "startTime": "2026-07-20T12:00:00Z",
    "status": "ENQUEUED"
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "id": "3c1f9a52-0b8e-4f5d-9d0e-4a1b2c3d4e5f",
    "jobType": "storageClassMigration",
    "startTime": "2026-09-04T12:00:00Z",
    "status": "ENQUEUED",
    "storageClassMigration": {
      "destinationStorageClass": "InfrequentAccess",
      "migratedObjects": 0,
      "sourceStorageClass": "Standard"
    }
  },
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 10083,
      "message": "Remove all event notification rules from bucket (example-bucket) before emptying it (account 023e105f4ecef8ad9ca31a8372d0c353)."
    }
  ],
  "messages": [
    "Request failed."
  ],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 10058,
      "message": "Too many concurrent prefix delete jobs for this bucket. Please wait for existing jobs to complete."
    }
  ],
  "messages": [
    "Request failed."
  ],
  "result": null,
  "success": false
}
```

##### Returns Examples

200 example

200 example

200 example

409 example

429 example

```
{
  "errors": [],
  "messages": [],
  "result": {
    "endTime": "2026-07-20T12:00:00Z",
    "id": "69f94626-a3fe-47bc-9615-e791b4d53c53",
    "jobType": "prefixDelete",
    "prefixDelete": {
      "deletedObjects": 0,
      "isBucketClear": true,
      "prefix": ""
    },
    "startTime": "2026-07-20T12:00:00Z",
    "status": "COMPLETED"
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "id": "7f24658b-31d7-4b91-9a12-cb5a2c99b294",
    "jobType": "prefixDelete",
    "prefixDelete": {
      "deletedObjects": 0,
      "isBucketClear": true,
      "prefix": ""
    },
    "startTime": "2026-07-20T12:00:00Z",
    "status": "ENQUEUED"
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "id": "3c1f9a52-0b8e-4f5d-9d0e-4a1b2c3d4e5f",
    "jobType": "storageClassMigration",
    "startTime": "2026-09-04T12:00:00Z",
    "status": "ENQUEUED",
    "storageClassMigration": {
      "destinationStorageClass": "InfrequentAccess",
      "migratedObjects": 0,
      "sourceStorageClass": "Standard"
    }
  },
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 10083,
      "message": "Remove all event notification rules from bucket (example-bucket) before emptying it (account 023e105f4ecef8ad9ca31a8372d0c353)."
    }
  ],
  "messages": [
    "Request failed."
  ],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 10058,
      "message": "Too many concurrent prefix delete jobs for this bucket. Please wait for existing jobs to complete."
    }
  ],
  "messages": [
    "Request failed."
  ],
  "result": null,
  "success": false
}
```