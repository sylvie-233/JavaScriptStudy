# Drizzle

## 基础介绍

ts ORM框架
- drizzle orm
- drizzle kit
- drizzle studio


## drizzle-kit
```yaml
drizzle-kit:
    generate: # 生成数据库迁移文件
        --config:
        pg:
    migrate:
    pull:
    push: # 数据库迁移
        --config:
        pg:
```

数据库迁移工具



### dirzzle.config.ts
```yaml
dirzzle.config.ts:
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
    defineConfig():
        out:
        schema:
        dialect:
        dbCredential:
            url:

drizzle-orm:
    bun-sqlite:
        drizzle():
    neon-http: # neon
        drizzle():
            --- # db
            query:
                _table:
                    findMany():
            insert():
                values():
    pg-core: # postgre 核心
        integer():
        paTable(): # 表定义
            $inferInsert:
            logger:
            schema: # 所有表定义
        serial(): # 字段定义
        text():
            notNull():
            primaryKey():    
        varchar():
            notNull():
    sqlite-core: # sqlite3 核心
    sql(): # 
```