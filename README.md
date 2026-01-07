## User Data Model

This project uses DynamoDB to store user data.

Each user item has the following attributes:

- `user_id` (string, partition key): Unique identifier (UUID)
- `email` (string): User email address
- `created_at` (string): ISO-8601 timestamp of user creation

The `user_id` attribute is used as the DynamoDB partition key to ensure even
data distribution and efficient access patterns for a serverless workload.