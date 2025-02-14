# knex

## 基础介绍


sql query builder工具(查询生成器)


## 核心内容
```yaml
knex:
    _db: # 数据库实例
        count():
        delete():
        insert():
        leftJoin():
        orderBy():
        raw(): # 原始sql
        select():
        toSQL():
            sql:
        transaction(): # 事务
            commit():
            rollback():
        update():
        where():
    _options: # 数据库配置信息
        client:
            mysql2:
        connection:
            database:
            host:
            user:
            password:
    schema:
        createTableIfNotExists(): # 创建表
            increments():
            integer():
            string():
            timestamps():
```