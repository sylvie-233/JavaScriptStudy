# TypeScript

>
>`# TODO 2022 TypeScript 从入门到精通完全指南 P21`
>
>`# TODO TYPESCRIPT编程.pdf p38`
>


## 基础介绍

### tsc
```yaml
tsc:
    -d: 生成.d.ts声明文件
    -h: 帮助信息
    -m: 指定模块版本信息
    -p: 指定配置文件
    -v: 版本
    -w: 监听文件
    --help:
    --init: 初始化项目，生成配置文件
```


### tsconfig.json
```yaml
:
    compilerOptions: 编译选项
        lib: 使用的内置库
            "DOM|ES2015"
        module: 使用的模块系统
        outDir: 输出目录
        sourceMap:
        strict:
        target: 编译的JS目标版本
    include: 源文件列表
```





## 核心内容
```yaml
TypeScript:
    any: 任意类型
    boolean: 布尔
    enum: 枚举
    instanceof: 实例判断（关键字）
    keyof: 获取键（关键字）
    number: 数字
    object: 对象
    string: 字符串
        toUpperCase():
    typeof: 获取变量类型（关键字）
    Array: 数组
    Error: 异常
    Object: 对象
    Tuple: 元组（固定元素的数组）
DOM:
    HTMLInputElement:
```

### 数据类型
```yaml
type:
    any:
    boolean:
    number: 
    string:
    Array:

Utility Types:

```

ts能进行自动类型推断

enum枚举


interface、type自定义数据类型


Union联合类型: `(type1 | type2 | ...)`，联合类型一般和typeof结合使用，用来判断具体的类型

Literal字面量类型，literal类型在做参数限定的时候很有用（限定只能取哪些字面量），常配合联合类型使用

Type Aliase类型别名：通过type关键字定义类型别名



### 面向对象

#### Class



#### Interface




#### Decorators



#### Module





### 泛型


