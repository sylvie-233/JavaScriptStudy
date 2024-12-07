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
    Model:
        associate():
        init():
    Sequelize:

sequelize-cli:
    Migration: # 数据库迁移类
        down():
        up():
```