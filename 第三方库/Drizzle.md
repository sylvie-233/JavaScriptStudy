# Drizzle

## 基础介绍

ts ORM框架


## drizzle-kit
```yaml
drizzle-kit:
    generate:
        --config:
        pg:
    push:
        --config:
        pg:
```

数据库迁移工具



### dirzzle.config.ts
```yaml
:
```




## 核心内容
```yaml
@neodatabase:
    serverless:
        neon():
drizzle-kit:
    Config: # 配置连接信息
        dbCredentials:
            database:
            host:
            password:
            user:
        driver:
        out: # 迁移输出
        schema: # 表定义文件

drizzle-orm:
    neon-http:
        drizzle():
            --- # db
            query:
                _table:
                    findMany():
            insert():
                values():
    pg-core:
        paTable(): # 表定义
            logger:
            schema: # 所有表定义
        serial(): # 字段定义
        text():
            notNull():
            primaryKey():    
```