- [What is ElastiCache for Redis?](#what-is-elasti-cache)
- [Comparing Memcached and Redis](#comparing-memcached-and-redis)
- [Authenticating with Redis AUTH command](#authenticating-with-redis-auth-command)

## What is ElastiCache for Redis?

---
- ElastiCache is a web service that makes it easy to set up, <i><u> manage and scale a distributed in-memory data store or cache environment </u></i> in the cloud.
- Features:
    - Automatic detection of and recovery from cache node failures
    - <b> Multi-AZ </b>for a failed primary cluster to a read replica in Redis cluster
    - Redis (cluster mode enabled) supports partitioning your data across up to 500 shards
- ElastiCache works with both the Redis and Memcached engines.

## Comparing Memcached and Redis
---
- ElastiCache supports Memcached and Redis Cache engines


## Authenticating with Redis AUTH command
---
- Users enter a token (password) on a token-protected Redis server. 
- Include the parameter `--auth-token`  (API: <u>AuthToken</u>) with the correct token to create the replication group or cluster. 
- Key Parameters:
    - <i><u> `--engine` </u></i> - Must be redis
    - <i><u> --engine-version </u></i> - Must be 3.2.6,4.0.10 or later
    - <i><u> --transit-encryption-enabled </u></i> - Required for authentication and HIPAA eligibility
    - <i><u> --auth-token </u></i> - Required for HIPAA eligibility. This value must be correct token for this token-protected Redis-server
    - <i><u> --cache-subnet-group </u></i> - Required fro HIPAA eligibility

