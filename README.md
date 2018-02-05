shiro-redis-tutorial
======================

This is a tutorial help you to know how to use `shiro-redis`.
This tutorial use shiro.ini to configure `shiro` and `shiro-redis`.

# How to use it?

1. Use the following comment to clone shiro-redis-tutorial to your disk:
```
git clone https://github.com/alexxiyang/shiro-redis-tutorial.git
```
2. Modify redis service connection configuration in src/main/resources/shiro.ini.
Such as `redisManager.host`, `redisManager.port`, etc.
```INI
redisManager.host = 127.0.0.1
# Redis port. Default value: 6379 (Optional)
redisManager.port = 6379
# Redis cache key/value expire time. Default value:0 .The expire time is in second (Optional)
redisManager.expire = 600
# Redis connect timeout. Timeout for jedis try to connect to redis server(In milliseconds).(Optional)
redisManager.timeout = 0
# Redis password.(Optional)
#redisManager.password =
# Redis database. Default value is 0(Optional)
#redisManager.database = 0
```

3. Run jetty
```
mvn jetty:run
```

4. Visit `http://localhost:8080`, you will see login page:

![login page](images/login_page.png)

5. Use the username and password wrote on login page to sign in.
Then you will see the successful page:

![login success](images/login_success.png)

6. Use redis client to check redis data. For example, use `Redis Desktop Manager`:

![redis data](images/redis_data.png)

It means shiro use redis as its session and cache solution successfully.

# If you found any problems

Please send email to alexxiyang@gmail.com

可以用中文