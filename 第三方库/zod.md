# zod


## 基础介绍

TypeScript字段校验库


## 核心内容
```yaml
zod:
    z:
        array(): # 数组
        boolean(): # 布尔
        enum(): # 枚举
        lazy():
        number(): # 数字    
            min():
        object(): # 创建对象Schema
            extend(): # 对象继承
            parse(): # 对象校验, 失败抛出异常
            pick():
            safeParse(): # 对象安全校验
                data:
                error:
                success:
        record(): # 键值对
        string(): # 字符串
            and(): # 手动组合校验规则
            default(): # 默认值
            email():
            mid():
            optional():
            refine(): # 自定义校验
            superRefine(): # 自定义安全校验
                ctx:
                    addIssue():
                        code:
                        message:
                        path:
            transform(): # 结果转换
        union(): # 联合类型
        infer<>: # 生成type对象，用于ts中
    ZodIssueCode:
        custom:
    ZodSchema:
zod-validation-error:
    fromZodError():
```