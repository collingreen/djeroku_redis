## djeroku_redis


~~~
from djeroku_redis import redis_connection
r = redis_connection()

# any redis call now -- example: ping the server
r.ping()
~~~

djeroku_redis was originally created as a convenient way to transparently
use any of the redis addons from heroku (or localhost, or anything else),
based on memcacheify by RDegges.

However, github user dirn had already created the same thing, but better, for
the cache settings part.

In that light, this library has been renamed to djeroku_redis and is now
solely for getting a redis connection directly. dirn's django-heroku-redisify
should be used for setting up django to use redis as a cache.

Memcacheify by RDegges
https://github.com/rdegges/django-heroku-memcacheify

Redisify by dirn
https://github.com/dirn/django-heroku-redisify/blob/develop/redisify.py


Supports:
- MyRedis - https://addons.heroku.com/myredis
- OpenRedis - https://addons.heroku.com/openredis
- RedisCloud - https://addons.heroku.com/rediscloud
- RedisGreen - https://addons.heroku.com/redisgreen
- RedisToGo - https://addons.heroku.com/redistogo
- Custom - set REDIS_SERVER_URL in your environment or settings

Requires redis-py and expects to be in a django environment.
