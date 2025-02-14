# class-validator


## 基础介绍

class-validator、class-transform

模型数据校验库

## 核心内容
```yaml
class-transform:
    @Transform():
    plainToClass(): # 执行数据转换
class-validator:
    @IsNotEmpty():
        message:
    validate(): # 执行数据校验
```
