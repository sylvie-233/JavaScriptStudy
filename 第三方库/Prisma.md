# Prisma

`Prisma官方文档：https://www.prisma.io/docs/orm/overview/introduction`


## 基础介绍

nodejs ORM框架


datasource、generator、model

默认寻找/prisma文件夹下的schema.prisma文件（支持多文件.prisma）

自带studio：5555端口


### 目录结构
```yaml
/prisma:
    /migrations: # 迁移文件
        /0000000_xxxx:
            migration.sql: # sql数据库迁移文件
        migration_lock.toml:
    /schema: # 多schema文件
    schema.prisma: # 主schema
```

### prisma
```yaml
prisma:
    db:
        pull: # 根据数据库更新(.prisma)schema文件
        push:
    format: # 格式化schema文件
    generate: # 生成客户端代码（node_modules/.prisma/client）
        --schema: # 指定schema文件
    init:
        --datasource-provider:
            mysql:
    migrate: # 数据库迁移(生成迁移文件)
        --name:
        dev: # 开发数据库迁移（更新数据库、迁移sql、客户端代码）
    studio: # 可视化网站
```

#### .prisma
```yaml
database: # 数据库连接信息
    provider:
        sqlite: # sqlite3数据库
enum: # 定义枚举变量
generator: # 生成客户端代码
    output: # 定义客户端代码输出路径
    previewFeatures: # 预览功能
        driverAdapters:
        prismaSchemaFolder: # 多schema文件
    provider:
        prisma-client-js: # js客户端
    url:
model: # 模型定义
    type:
        Boolean:
        DateTime:
        Int:
        String:
        Unsupported:
            []: # 数组类型
            ?: # 可选类型
            @db: # 原始数据库类型
                Boolean():
                Char():
                Text():
                TinyInt():
                Varchar():
            @id: # 定义主键id
            @unique: # 唯一约束
            @updatedAt:
            @autoincrement(): # 主键自增
            @env(): # 环境变量
            @default(): # 默认值
                true:
                false:
            @now(): # 当前时间
            @relation(): # 模型关联（只需在其中一个模型中定义即可）
                fields: # 本身关联字段
                references: # 外表关联字段（外表主键）
            @uuzzid():
        @@map(): # 定义关联的表名
        @@unique(): # 联合约束
    env(): # 获取环境变量
```







## 核心内容
```yaml
@prisma/client:
    PrismaClient: # 操作客户端
        _model:
            create(): # 创建
            delete(): # 删除
            findMany(): # 
                data: # 数据
                    connect:
                    create: # 关联模型数据创建
                include: # 包含关联模型
                    _model:
                orderBy:
                select: # 字段投影
                skip: # 分页skip
                take: # 分页take
                where: # 条件 
                    OR:
                    contains:
                    startsWith:
            findUnique():
            update():
        $disconnect(): # 断开连接
```


### Schema


### Client



### Migrate


### CLI


### Studio

