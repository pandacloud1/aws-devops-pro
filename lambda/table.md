| Feature | Ephemeral Storage `/tmp` | Lambda Layers (up to 250MB total) | Amazon S3 | Amazon EFS |
|----------|--------------------------|-----------------------------------|-----------|------------|
| **Max. Size** | 10,240 MB | 5 layers per function up to 250 MB total | Elastic | Elastic |
| **Persistence** | Ephemeral | Durable | Durable | Durable |
| **Content** | Dynamic | Static | Dynamic | Dynamic |
| **Storage Type** | File System | Archive | Object | File System |
| **Operations Supported** | Any File System operation | Immutable | Atomic with Versioning | Any File System operation |
| **Pricing** | Included in Lambda | Included in Lambda | Storage + Requests + Data Transfer | Storage + Data Transfer + Throughput |
| **Sharing/Permissions** | Function Only | IAM | IAM | IAM + NFS |
| **Relative Data Access Speed from Lambda** | Fastest | Fastest | Fast | Very Fast |
| **Shared Across All Invocations** | No | Yes | Yes | Yes |
| **Typical Use Case** | Temporary scratch space during a single invocation (e.g. unzip file, transform data, cache API result) | Store and share common libraries or runtime dependencies across multiple Lambda functions | Store large, durable, versioned data objects accessible to many Lambdas and services | Shared POSIX file system for multiple Lambdas/EC2 needing simultaneous read/write access to files |
