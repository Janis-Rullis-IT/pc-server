# Cache

# [Redis expire](https://redis.io/commands/expire)

## Expire accuracy

In Redis 2.4 the expire might not be pin-point accurate, and it could be between zero to one seconds out.
Since Redis 2.6 the expire error is from 0 to 1 milliseconds.
