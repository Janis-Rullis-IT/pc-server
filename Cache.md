# Cache

# [Redis expire](https://redis.io/commands/expire)

## Expire accuracy

In Redis 2.4 the expire might not be pin-point accurate, and it could be between zero to one seconds out.
Since Redis 2.6 the expire error is from 0 to 1 milliseconds.

https://stackoverflow.com/a/64306093

The expiration cycle has been rewritten in Redis 6.0 to allow for much faster expirations that more closely match the time-to-live (TTL) property. Redis 6 expiration will no longer be based on random sampling but will take keys sorted by expire time in a radix tree
— Redis 6 release notes
