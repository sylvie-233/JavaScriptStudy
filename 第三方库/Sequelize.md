# Sequelize


## 基础介绍

nodejs orm框架


### sequelize-cli
```yaml
sequelize:
    db:
        migrate:
    model:
        generate:
            --attributes:
            --name:
    seed:
        generate:
```


## 核心内容
```yaml
sequelize:
    DataTypes:
        DATE:
        STRING:
        TEXT:
    Model: # 模型基类（继承）
        associate():
        init(): # 初始化构建表字段
            _field:
                defaultValue:
                type:
        --- # 模型实例
        create(): # 创建
    Sequelize:
        _options:
            dialect: # 数据库类型
            host:
        authenticate(): # 连接测试
        close(): # 关闭连接
        sync():

sequelize-cli:
    Migration: # 数据库迁移类
        down():
        up():
```