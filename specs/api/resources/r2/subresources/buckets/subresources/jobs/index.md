---
title: Jobs
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[R2](https://developers.cloudflare.com/api/resources/r2)

[Buckets](https://developers.cloudflare.com/api/resources/r2/subresources/buckets)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Jobs

##### [List Bucket Jobs](https://developers.cloudflare.com/api/resources/r2/subresources/buckets/subresources/jobs/methods/list)

GET/accounts/{account\_id}/r2/buckets/{bucket\_name}/jobs

##### [Create Bucket Job](https://developers.cloudflare.com/api/resources/r2/subresources/buckets/subresources/jobs/methods/create)

POST/accounts/{account\_id}/r2/buckets/{bucket\_name}/jobs

##### [Get Bucket Job](https://developers.cloudflare.com/api/resources/r2/subresources/buckets/subresources/jobs/methods/get)

GET/accounts/{account\_id}/r2/buckets/{bucket\_name}/jobs/{job\_id}

##### ModelsExpand Collapse

<details>

<summary>

JobListResponse object {jobs, nextContinuationToken }

</summary>

<details>

<summary>

jobs: array of object {id, jobType, prefixDelete, 3 more } or object {id, jobType, startTime, 3 more }

Bucket jobs in the current page.

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

<a href="#">Link to this property</a>

nextContinuationToken: optional string

Token to pass as <code>continuationToken</code> to retrieve the next page.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(model)%20job_list_response%20%3E%20(schema)>)

<details>

<summary>

JobCreateResponse = object {id, jobType, prefixDelete, 3 more } or object {id, jobType, startTime, 3 more }

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

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(model)%20job_create_response%20%3E%20(schema)>)

<details>

<summary>

JobGetResponse = object {id, jobType, prefixDelete, 3 more } or object {id, jobType, startTime, 3 more }

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

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(model)%20job_get_response%20%3E%20(schema)>)