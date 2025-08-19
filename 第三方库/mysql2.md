# mysql2

## 基础介绍

mysql连接驱动


## 核心内容
```yaml
mysql2:
    promise: # 异步api
    Connection: # 连接对象
        beginTransaction():
        commit():
        connect():
        end():
        execute():
            fields:
            results:
        query(): 
        release():
        rollback():
    createConnection(): # 创建连接
        database:
        host:
        password:
        user:
    createPool(): # 创建连接池
        ---
        getConnection():
        query():
```