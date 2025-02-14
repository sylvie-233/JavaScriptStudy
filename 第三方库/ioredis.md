# ioredis

## 基础介绍

javascript 操作 redis的库


## 核心内容
```yaml
ioredis:
    host:
    port:
    eval(): # 执行lua脚本
    get():
    hdel():
    hgetall():
    hset(): # hash#set
    llen():
    lpush():
    lrange():
    on(): # 事件监听
        message:
    publish(): # 发布channel
    rpush():
    sadd(): # set#add
    set(): # string#set
    setex(): # string#set ex 过期时间
    sismember():
    srem():
    subscribe(): # 订阅channel
```