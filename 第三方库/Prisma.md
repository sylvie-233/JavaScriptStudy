# Prisma

## 基础介绍

ORM框架

### prisma
```yaml
prisma:
    generate:
    migrate: # 数据库迁移
        --name:
        dev:
    studio: # 可视化网站
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
                include: # 包含关联模型
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




### .prisma
```yaml
database: # 数据库连接信息
    provider:
        sqlite: # sqlite3数据库
generator: # 生成客户端代码
    provider:
        prisma-client-js: # js客户端
    url:
model: # 模型定义
    _type:
        Boolean:
        DateTime:
        Int:
        String:
    _@:
        autoincrement():
        env(): # 环境变量
        default(): # 默认值
        id():
        now():
        relation(): # 模型关联（只需在其中一个模型中定义即可）
            fields: # 本身关联字段
            references: # 外表关联字段（外表主键）
        unique(): # 唯一约束
        updatedAt():
        uuid():



```