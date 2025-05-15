# TypeORM

`typeorm官方文档：https://typeorm.io/`

## 基础介绍


ts orm框架，支持数据库迁移


### typeorm

```yaml
typeorm:
    init:
    migration:
        create: # 生成迁移文件
        generate:
        revert:
        run: # 执行迁移 
```



## 核心内容
```yaml
typeorm:
    common:
        DeepPartial:
    query-builder:
        QueryDeepPartialEntity:
    @Column: # 实体映射列
        default: # 默认值
        nullable:
        type:
            int:
        unique:
    @CreateDateColumn:
    @Entity: # 实体类
    @JoinColumn: # 指定关联列（可自动添加关联列字段），（只需指定一次）
    @JoinTable: # 指定关联中间表（只需指定一次）
        inverseJoinColumn:
            name: # 对方表的外键列名（在中间表里的）
            referencedColumnName:
        joinColumn:
            name: # 当前实体的外键列名（在中间表里的）
            referencedColumnName:
        name: # 指定中间表名
    @ManyToMany: # 多对多联表
    @ManyToOne: # 多对一联表
    @OneToOne: # 一对一联表
    @OneToMany: # 一对多联表
        cascade: # 关联表级联操作
        onDelete:
        onUpdate:
    @PrimaryGeneratedColumn: # 主键自增列
    @Tree:
    @TreeChildren:
    @TreeParent:
    @UpdateDateColumn:
    BaseEntity: # 实体基类
    DataSource: # 数据源
        database:
        entities: # 实体映射类
        host:
        logging: # 日志
        password:
        port:
        synchronize: # 自动同步实体类
        type: #
            mysql:
        username:
        ---
        manager: # 原始操作连接
            find(): # 条件查询
                where:
            findAndCount():
            findOne():
            findOneBy():
            insert():
            remove(): # 删除
            save(): # 添加、更新数据
        createQueryRunner(): # 一次性操作连接
            manager:
            commitTransaction():
            connect():
            release():
            rollbackTransaction():
            startTransaction():
        getRepository():
            createQueryBuild(): # 查询构造器
                andWhere():
                delete():
                    from():
                execute():
                getMany():
                getOne():
                groupBy():
                innerJoin():
                insert():
                    into():
                    values():
                leftJoinAndSelect():
                orderBy():
                select():
                skip():
                subQuery(): # 子查询
                    getQuery(): # 获取子查询sql
                take():
                update():
                    set():
                where():    
            find():
            findAndCount():
            findBy():
            findOne():
            findOneBy():
            insert():
            remove():
            save():
            update():
        getTreeRepository():
            findTrees():    
        initialize(): # 数据库初始化
        query(): # 原始sql查询
        transaction(): # 开启事务
           manager: 
    FindOneOptions:
    Repository: # Dao操作
        count():
        create(): # 创建实体
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




#### OneToOne
```ts
@Entity()
export class User {
  @PrimaryGeneratedColumn()
  id: number;

  @Column()
  name: string;

  @OneToOne(() => Profile, (profile) => profile.user)
  @JoinColumn() // ⚠️ 必须在拥有外键的一侧加上
  profile: Profile;
}

@Entity()
export class Profile {
  @PrimaryGeneratedColumn()
  id: number;

  @Column()
  bio: string;

  @OneToOne(() => User, (user) => user.profile)
  user: User;
}


const user = await userRepo.findOne({
  where: { id: 1 },
  relations: ['profile'],
});
```

#### OneToMany
```ts
@Entity()
export class User {
  @PrimaryGeneratedColumn()
  id: number;

  @Column()
  name: string;

  @OneToMany(() => Post, (post) => post.user)
  posts: Post[];
}

@Entity()
export class Post {
  @PrimaryGeneratedColumn()
  id: number;

  @Column()
  title: string;

  @ManyToOne(() => User, (user) => user.posts)
  user: User;
}

const user = await userRepo.findOne({
  where: { id: 1 },
  relations: ['posts'],
});
```


#### ManyToMany
```ts
@Entity()
export class Student {
  @PrimaryGeneratedColumn()
  id: number;

  @Column()
  name: string;

  @ManyToMany(() => Course, (course) => course.students)
  @JoinTable()  // ⚠️ 只能放一侧，创建 join table
  courses: Course[];
}

@Entity()
export class Course {
  @PrimaryGeneratedColumn()
  id: number;

  @Column()
  title: string;

  @ManyToMany(() => Student, (student) => student.courses)
  students: Student[];
}

const student = await studentRepo.findOne({
  where: { id: 1 },
  relations: ['courses'],
});



const student = await studentRepo.findOneBy({ id: 1 });
const course = await courseRepo.findOneBy({ id: 2 });

student.courses = [course];
await studentRepo.save(student);
```

### Repository

### QueryRunner


### QueryBuilder




### Tree

树形结构
