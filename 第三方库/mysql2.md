# mysql2

## 基础介绍

mysql连接驱动


## 核心内容
```yaml
mysql2:
    promise:
    createConnection(): # 创建连接
        database:
        host:
        password:
        user:
        --- # Connection连接对象
        beginTransaction():
        commit():
        connect():
        execute():
            fields:
            results:
        query(): 
        release():
        rollback():
    createPool(): # 创建连接池
        ---
        getConnection():
        query():
```