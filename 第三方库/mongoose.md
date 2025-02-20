# mongoose

## 基础介绍

MongoDb操作库

## 核心内容
```yaml
mongoose:
    Schema: # 定义集合结构
        _field:
            default:
            enum:
            required:
            type:
            unique:
        Types:
            Array:
            Boolean:
            Buffer:
            Date:
            Decimal128:
            Mixed: # 任意类型
            Number:
            ObjectId:
            String:
    connection:
        on():
            close:
            error:
            open:
        once():
    connect(): # 连接数据库
    disconnect():
    model(): # 操作集合对象
        create():
            ---
        deleteMany():
        deleteOne():
            ---
            deletedCount:
        exec():
        find():
        findById():
        findOne():
        insertMany():     
        limit():
        select():
        skip():
        sort():
        updateMany():
        updateOne():    
            <query>:
                $and:
                $gt:
                $lt:
                $or:
            <update>:
```