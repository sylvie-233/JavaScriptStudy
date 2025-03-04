# TypeScript

>
>``
>
>`小满TypeScript教程：P7`
>

## 基础介绍

### tsc
```yaml
tsc:
    -d: # 生成.d.ts声明文件
    -h: # 帮助信息
    -m: # 指定模块版本信息
    -p: # 指定配置文件
    -v: # 版本
    -w:  # 监听文件
    --declaraion: # 生成声明文件
    --help:
    --init: # 初始化项目，生成配置文件tsconfig.json
    --watch:
```

typescript编译命令


#### tsconfig.json
```yaml
tsconfig.json:
    compilerOptions: 
        allowJs: # 编译js文件
        declaration: # 编译生成声明文件
        lib: # 使用的内置库
            DOM:
            ES2015:
        mapRoot: # 生成sourcemap的目录
        module: # 使用的模块系统
            commonjs:
        noImplicitAny: # 禁止隐式推导any
        noUnusedLocals: # 未使用的局部变量
        outDir: # 输出目录
        rootDir: # 源码目录
        sourceMap: # 生成SourceMap文件
        strict: # 严格模式
        strictNullChecks: # 空类型检查
        target: # 编译的JS目标版本
            :es5:
    exclude: # 排除编译文件
    fils: # 包含编译文件
    include: # 包含编译文件
```





## 核心内容
```yaml
TypeScript:
    Array: # 数组
        push():
        reduce():
    Error: # 异常
    IArguments: # 函数arguments对象
    Object: # 对象
    ReadonlyArray: # 只读数组
    Tuple: # 元组（固定元素的数组）
    any: # 任意类型
    boolean: # 布尔
    enum: # 枚举
    never: # 所有类型子类
    number: # 数字
    object: # 对象
    string: # 字符串
        toUpperCase():
    symbol:
    unknown: # 更为严格的any
    void:
DOM:
    HTMLInputElement:
```

### 数据类型
```yaml
DataTypes:
    Array:
    Function:
    Infinity: # 无穷大
    NaN: # 非数字类型
    Object: # 顶层基类
    any: # 顶层类型
    bigint: # 字面量以n结尾
    boolean:
    interface:
    never: # 所有类型子类
    null:
    number: 
    object: # 非原始类型
    string:
    undefined:
    unknown: # 顶层类型
    void: # 空类型

Utility Types: # 工具类型
    Awaited: # Awaited<T>	获取 Promise<T> 解析后的类型
    ConstructorParameters: # ConstructorParameters<T>	获取构造函数的参数类型
    Exclude: # Exclude<T, U>	从 T 中排除 U 类型，用于联合类型
    Extract: # Extract<T, U>	从 T 中提取 U 类型，用于联合类型
    InstanceType: # InstanceType<T>	获取构造函数返回的实例类型
    NonNullable: # NonNullable<T>	移除 null 和 undefined
    Omit: # Omit<T, K>	从 T 中移除 K 这些属性，用于对象属性
    OmitThisParameter: # OmitThisParameter<T>	移除函数的 this 参数
    Parameters: # Parameters<T>	获取函数参数的类型
    Partial: # Partial<T>	将类型的所有属性变为可选
    Pick: # Pick<T, K>	从 T 中选择 K 这些属性，用于对象属性
    Readonly: # Readonly<T>	将类型的所有属性变为只读
    Record: # Record<K, T>	创建一个以 K 为键、T 为值的对象类型
    Required: # Required<T>	将类型的所有属性变为必填
    ReturnType: # ReturnType<T>	获取函数返回值的类型
    ThisParameterType: # ThisParameterType<T>	获取函数的 this 类型
```


支持可空类型`?:`、只读属性`readonly`
ts能进行自动类型推断
enum枚举
interface、type自定义数据类型




![Ts类型层次结构](../assets/Ts类型层次结构.png)





Union联合类型: `(type1 | type2 | ...)`，联合类型一般和typeof结合使用，用来判断具体的类型

Literal字面量类型，literal类型在做参数限定的时候很有用（限定只能取哪些字面量），常配合联合类型使用

Type Aliase类型别名：通过`type`关键字定义类型别名

- 所有类型是`any`的子类型
- `unknown`与any一样，但unknown不能直接使用，需要typeof判断类型后使用
- `never`是所有类型的子类型
（any|unknown类似全集，never类似空集）


变量限定：`var`、`const`、`let`


#### String


#### Array
```typescript
// 直接声明
let arr1: number[] = [1, 2, 3];
```

动态数组

`...`扩展运算符


#### Tuple
```typescript
// 元组声明
let tuple: [string, number] = ["Alice", 25];
```

元组
固定长度的数组



#### Set



#### Map



#### Enum

枚举



#### Utility Types


### 控制流程
```yaml
Control Flow:
    ?:: # 可空类型
    const: # 常量
    infer: # 类型推断
    instanceof: # 实例判断（关键字）
    let: # 局部变量
    keyof: # 获取键（关键字）
    readonly: # 只读属性
    typeof: # 获取变量类型（关键字）
```


#### 异常处理



### 函数


Function

支持默认参数、可选参数、变长参数
可进行函数重载、声明可有多个，实现只能有一个




### 面向对象

#### Class


成员函数第一个参数可为`this`，用于自身实例的引用



#### Interface

严格类型定义

重名接口声明，属性复合
接口继承`extends`

##### 索引签名


##### 函数签名


#### Decorators


##### ClassDecorator
```ts
const mydec: ClassDecorator = (target) => {
    ...
    target.prototype...
} 
```

类装饰器、传入类构造函数



##### PropertyDecorator

属性装饰器：`(target, propertyKey)`



##### MethodDecorator
```yaml
MethodDecorator:
    target:
    propertyKey:
    descriptor:
        value: # 方法本身
```

方法装饰器：`(target, propertyKey, descriptor)`

传入原型对象、方法名、方法描述符


##### ParameterDecorator

方法参数装饰器：`(target, propertyKey, parameterIndex)`








#### Generics




### Module



#### Namespace

命名空间



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

`/// <reference path="..." />`：引入声明文件依赖@types
`.d.ts`：类型声明文件，为现有的javascript库提供类型注解


