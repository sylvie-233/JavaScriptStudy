# Sequelize

`sequelize官方文档：https://sequelize.org/docs/v6/core-concepts/model-instances/`


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
        BOOLEAN:
        DATE:
        DECIMAL:
        FLOAT:
        NOW: # 当前时间
        STRING: # 字符串
        TEXT: # 长文本
        UUID:
    Deferrable:
    Model: # 模型基类（继承）
        :
            associate():
            belongsTo():
                foreignKey():
            belongsToMany():
                through: # 多对多关联中间表模型
            build(): # 生成模型实例
            drop(): # 删除模型关联表
            hasMany():
            hasOne():
                foreignKey:
            init(): # 初始化构建表字段（定义）
                _field:
                    defaultValue:
                    primaryKey:
                    type:
                    validate:
                _options:
                    freezeTableName: # 禁止表名加复数
                    modelName:
                    sequelize: # 设置sequelize实例对象
                    tableName:
            sync(): # 数据库迁移（创建表）
                alter:
                force:
                match:
        create(): # 创建
        findAll():
        findOne():
            where():
    Op:
    Sequelize:
        _options:
            define:
                freezeTableName:
            dialect: # 数据库类型
            host:
            logging:
            storage:
        models: # 模型实例
            _modelName:
        authenticate(): # 连接测试
        close(): # 关闭连接
        define(): # 定义数据库模型
            _field:
                allowNull:
                autoIncrement:
                comment: # 字段备注
                defaultValue:
                references: # 关联模型
                    key: # 关联模型id
                    model: # 关联模型名       
                type:
                unique:
            _options:
                createdAt:
                indexes:
                timestamps: # 自动修改字段时间戳
                updatedAt:
        sync(): # 数据库迁移（创建表）

sequelize-cli:
    Migration: # 数据库迁移类
        down():
        up():
```



### 模型

模型定义的两种方式
- sequelize.define()
- 继承模型基类Model，调用init()


模型自动添加字段：`createdAt`、`updatedAt`
