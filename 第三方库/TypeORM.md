# TypeORM

`typeorm官方文档：https://typeorm.io/`

## 基础介绍


### typeorm

```yaml
typeorm:
    init:
```



## 核心内容
```yaml
typeorm:
    @Entiry:
    @ManyToMany: 多对多联表
    @ManyToOne: 多对一联表
    @OneToOne: 一对一联表
    @OneToMany: 一对多联表
    @PrimaryGeneratedColumn:
    BaseEntity:
    Column:
    DataSource:
        database:
        entities: 实体映射类
        host:
        logging:
        password:
        port:
        type: "postgres"
        username:
        ---
        manager:
            find():
            save():
        getRepository():
            createQueryBuild():
            find():
            findAndCount():
            findBy():
            findOneBy():
            remove():
            save():
    Repository: # Dao操作
        count():
        delete():
        find():
            order:
            skip:
            take:
            where:
        findOne():
        save():
        transaction():
        update():
    Like():
```

### DataSource




### Entity




### Relations



### Query Builder
