# Prisma

## 基础介绍

ORM框架

### prisma
```yaml
prisma:
    generate:
    migrate:
        --name:
```


## 核心内容
```yaml
@prisma/client:
    PrismaClient: # 操作客户端
        _model:
            create():
            findMany():
                data:
                orderBy:
                include: 
                where:
            update():
```




### .prisma
```yaml
database: # 数据库连接信息
    provider:
generator: # 生成代码
    provider:
        url:
model: # 模型
    _type:
        DateTime:
        Int:
        String:
    _@:
        id:
        updatedAt:
        autoincrement():
        env(): # 环境变量
        default():
        now():
        relation():
            fields: # 本身关联字段
            references: # 外表关联字段（外表主键）
        unique():
        uuid():



```