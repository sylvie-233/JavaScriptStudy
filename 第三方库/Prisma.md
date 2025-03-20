# Prisma

`Prisma官方文档：https://www.prisma.io/docs/orm/overview/introduction`


## 基础介绍

nodejs ORM框架
- `prisma`
- `@prisma/client`

`prisma migrate dev`

datasource、generator、model
默认寻找/prisma文件夹下的schema.prisma文件（支持多文件.prisma）
自带studio：5555端口


### 目录结构
```yaml
/prisma:
    /migrations: # 迁移文件
        /0000000_xxxx: # 自定义迁移名称
            migration.sql: # sql数据库迁移文件
        migration_lock.toml:
    /schema: # 多schema文件
    schema.prisma: # 主schema
    seed.ts: # db seed命令执行数据填充
/node_modules:
    /.prisma: # 实际生成代码
        /client:
            default.js:
            index.d.ts: # 模型类型声明
            index.js:
    /@prisma:
        /client:
            default.js:
            index.js:

```


#### seed.ts
```typescript
import { PrismaClient } from '@prisma/client';

const prisma = new PrismaClient();

async function main() {
  await prisma.user.create({
    data: { name: 'Alice', email: 'alice@example.com' },
  });
}

main().catch(console.error).finally(() => prisma.$disconnect());
```




### prisma
```yaml
prisma:
    db:
        pull: # 根据数据库更新(.prisma)schema文件
        push: # 同步数据库（根据schema.prisma的模型结构更新数据库、不会生成迁移文件）
        seed: # 数据填充（执行prisma/seed.ts）
    debug:
    format: # 格式化schema文件
    generate: # 根据schema生成客户端代码（node_modules/.prisma/client）
        --schema: # 指定schema文件
    init: # 初始化项目（生成/prisma文件夹、.env文件）
        --datasource-provider:
            mysql:
    migrate: # 
        deploy: # 在生产环境中，应用所有未执行的迁移（不会创建新的迁移文件，只应用prisma/migrations目录下已有的迁移）
        dev: # 开发数据库迁移（创建迁移sql、更新数据库、、生成客户端代码）
            --create-only: # 仅创建迁移sql
            --name: # 指定迁移名称
        reset: # 重置数据库（删除数据库、重新运行所有迁移、重新填充测试数据）
    studio: # 可视化网站
    validate: # schema语法校验
    version:
```

#### schema.prisma
```yaml
database: # 数据库连接信息(名称可自定义)
    provider:
        mysql:
        sqlite: # sqlite3数据库
    url: # 连接url
        env(): # 获取环境变量
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
        Boolean: # 布尔
        DateTime: # 时间日期
        Int: # 整形
        String: # 字符串
        Unsupported:
            []: # 数组类型
            ?: # 可选类型
            @db: # 原始数据库类型
                Boolean():
                Char():
                Text():
                TinyInt():
                Varchar():
            @default: # 字段默认值
                true:
                false:
                autoincrement(): # 主键自增
            @id: # 主键id
            @now: # 当前时间
            @relation: # 模型关联（只需在其中一个模型中定义即可）
                fields: # 自身外键字段
                references: # 外键依赖字段
            @unique: # 唯一约束
            @updatedAt:
            @uuzzid:
        @@unique: # 联合约束
    @map: # 定义数据库表名
    @datasource: # 指定数据库定义信息
```


关联模型定义和ORM模型定义一样
一对多关联关系，只需在其中一方定义即可






## 核心内容
```yaml
@prisma/client:
    runtime:
        dmmf:
            datamodel:
                models:
    PrismaClient: # 操作客户端
        _model:
            aggregate(): # 聚合
                _avg:
                _count:
                _max:
                _min:
            count():
            create(): # 创建
            createMany(): # 创建
            delete(): # 删除
            deleteMany():
            findFirst():
            findMany(): # 
            findUnique():
            update(): # 更新数据
            updateMany(): # 更新数据
            upsert():
                data: # 数据
                    connect:
                    create: # 关联模型数据创建
                include: # 包含关联模型
                    _model:
                orderBy:
                select: # 字段投影
                skip: # 分页skip
                take: # 分页take
                where: # 查询条件
                    OR:
                    contains:
                    startsWith:
        $connect():
        $disconnect(): # 断开连接
        $executeRaw(): # 执行SQL语句（INSERT/UPDATE/DELETE）
        $queryRaw(): # 原始sql查询
        $transaction(): # 事务
```


### Schema

数据库信息、表定义文件

可使用多个schema文件：主`schema.prisma`、从`xxx.schema.prisma`
一组多从，在主schema中使用import导入其它schema中的model



### Client

生成的客户端代码


### Migrate

数据库迁移

`prisma migrate dev`：开发中最常用的命令




### Studio

可视化操作工具
