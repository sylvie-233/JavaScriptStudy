# TypeScript

>
>``
>
>``
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
    --declaraion: 生成声明文件
    --help:
    --init: 初始化项目，生成配置文件tsconfig.json
    --watch:
```


#### tsconfig.json
```yaml
:
    compilerOptions: 
        allowJs: 编译js文件
        declaration: 编译生成声明文件
        lib: 使用的内置库
            "DOM|ES2015|"
        mapRoot: 生成sourcemap的目录
        module: 使用的模块系统
            "commonjs|"
        noImplicitAny: 禁止隐式推导any
        noUnusedLocals: 未使用的局部变量
        outDir: 输出目录
        rootDir: 源码目录
        sourceMap: 生成SourceMap文件
        strict: 严格模式
        strictNullChecks: 空类型检查
        target: 编译的JS目标版本
            "es5|"
    exclude: 排除编译文件
    fils: 包含编译文件
    include: 包含编译文件
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
    symbol:
    typeof: 获取变量类型（关键字）
    unknown: 更为严格的any
    void:
    Array: 数组
        push():
        reduce():
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
    bigint: 字面量以n结尾
    boolean:
    number: 
    string:
    undefined:
    void: 空类型
    Array:
    Function:

Utility Types:

```

![Ts类型层次结构](../assets/Ts类型层次结构.png)

ts能进行自动类型推断

enum枚举


interface、type自定义数据类型


Union联合类型: `(type1 | type2 | ...)`，联合类型一般和typeof结合使用，用来判断具体的类型

Literal字面量类型，literal类型在做参数限定的时候很有用（限定只能取哪些字面量），常配合联合类型使用

Type Aliase类型别名：通过`type`关键字定义类型别名

- 所有类型是`any`的子类型
- `unknown`与any一样，但unknown不能直接使用，需要typeof判断类型后使用
- `never`是所有类型的子类型
（any|unknown类似全集，never类似空集）


变量限定：`var`、`const`、`let`



#### Array

`...`扩展运算符



### 面向对象

#### Class



#### Interface




#### Decorators









#### 泛型


### Module



#### Namespace



### Declaration
```typescript
declare module "模块名称" {
    export let obj : {}
    export function func(arg: type): retType
}

declare global {} // 用于在全局作用域中声明
```


- type: 定义类型别名
- interface: 定义对象形状
- enum: 定义枚举
- namespace: 定义命名空间
- import/export: 模块导入导出


`.d.ts`：类型声明文件，为现有的javascript库提供类型注解


