# Dart

`Dart官方文档：https://dart.dev/docs`
`Dart生态库：https://pub.dev/`
``

## 基础介绍

谷歌开发的、类型安全、面向对象的编程语言`.dart`（类似C++、Java、Python结合）

Flutter SDK包含Dart SDK


`PUB_CACHE`: 全局缓存路径，第三方包安装
- Windows：`C:\Users\<UserName>\AppData\Local\Pub\Cache`
- macOS/Linux：`~/.pub-cache`


- 文件结构和Java类似、每行结束必须携带分号`;`
- Dart万物皆对象，引用传递
- 支持自动类型推断，变量声明、函数返回值
- 实例化对象不用写new
- dart:core包默认导入

### 项目结构
```yaml
dart:
    /.dart_tool:
    /bin:
        main.dart:
    /lib:
    /test:
    analysis_options.yaml:
    pubspec.lock:
    pubspec.yaml:
```


### dart
```yaml
dart:
    -h:
    -v: # 版本
    analyze:
    compile:
    create: # 创建dart项目
        --force:
        -t: # 指定项目模板
            console:
    devtools:
    doc:
    fix: 
    format: # 代码格式化
    info: # dart环境信息
    pub: # dart包管理工具
        -h:
        -v:
        add: # 添加依赖
        bump:
        cache:
        deps:
        downgrade:
        get: # 下载第三方库
        global:
        login:
        logout:
        outdated:
        publish:
        remove:
        token:
        unpack:
        upgrade:
        workspace:
    run: # 运行dart程序
    test: # 测试
```

dart命令行工具




#### pubspec.yaml
```yaml
pubspec.yaml:
    name: # 项目名
    description: # 项目描述
    version: # 项目版本号
    environment: # 项目环境要求
        sdk: # sdk要求
    dependencies: # 依赖包
    dev_dependencies: # 开发依赖
    flutter:
        uses-material-design:
```

dart包配置文件


## 核心内容
```yaml
dart:
    async: # 异步
        Future: # 异步Promise
            catchError():
            then():
        Stream: # 连续异步Promise
    cli:
    collection: # 集合
        LinkedHashMap: # 
        HashMap:
        HashSet:
        Queue: # 队列
            addAll():
            removeFirst():
        SplayTreeMap:
    convert: # 转换
        JsonDecoder:
        JsonEncoder:
        utf8:
            encode():
            decode():
        base64Decode():
        base64Encode():
        jsonDecoder():
        jsonEncoder():
    core: # 内置模块（默认导入）
        @override: # 重写
        @patch: # external实现
        @required:
        BigInt:
        Comparable:
        DateTime: # 日期时间
            millisecondsSinceEpoch: # 毫秒
            month:
            add():
            difference():
                inDays:
                inHours:
            isAfter():
            isAtSameMomentAs():
            isBefore():
            now():
            parse():
            utc():
        Duration: # 时间间隔
            hour:
        Enum: # 枚举
            index: # 枚举索引
            values: # 所有枚举值
        Function: # 函数
        List: # 列表
            length: # 列表长度
            reversed:
            add(): # 添加元素
            addAll():
            any():
            clear():
            empty():
                growable():
            every():
            expand(): # 列表降维
            filled(): # 填充构造
            fold(): # reduce迭代计算 
            forEach(): # 迭代遍历
            insert(): # 插入元素
            insertAll():
            join(): #元素合并字符串
            map(): # 元素转换
            remove(): # 删除元素
            removeAt(): # 删除元素
            toSet():
            where():
                toList():
        Map: # 哈希表
            keys:
            values:
            containsKey():
            containsValue():
            from():
            putIfAbsent():
            remove():
            removeWhere():
        MapEntry:
        Match:
        Null:
        Object: # 基类
            runtimeType:
            hashCode():
            noSuchMethod():
            toString():
        Pattern:
        Record:
        RegExp: # 正则表达式
            hasMatch():
        Runes:
        Set: # 集合
            first:
            last:
            add(): # 添加元素
            addAll():
            clear():
            difference(): # 差集
            intersection(): # 交集
            remove():
            toList():
            union(): # 并集
        Stream:
        String: # 字符串
            length:
            runes:
            contains():
            fromCharCodes():
            hasMatch():
            indexOf():
            isEmpty():
            padLeft(): # 左边填充
            replaceAll():
            split(): # 字符串分隔
            trim(): # 空白符去除
        StringBuffer:
        Symbol:
        Type:
        Uri: # uri链接
            parse():
        WeakReference:
        bool: # 布尔（不存在隐式类型转换）
        double: # 浮点数
            toInt():
        dynamic: # 动态类型
        int: # 整数
        num: # 数字类型
            compareTo(): # 数字比较
            isNaN():
            remainder(): # 余数
            round(): # 四舍五入
            toString():
            toStringAsFixed():
        identical(): # 对象标识，判断对象是否相等
        print(): # 控制台输出
    developer:
    ffi:
    io: # I/O
        Directory: # 目录
            list():
        File: # 文件
            readAsString():
            writeAsString():
        Process: # 进程
            run(): # 运行子进程
    isolate: # 并发库
        Isolate:
            kill():
            spawn():    
        ReceivePort: # 接收管道
            sendPort:
            close():
            listen(): # 接收消息
        SendPort: # 发送管道
            send(): # 发送消息
    math: # 数学库
        pi:
        max():
        min():
    mirrors: # 反射
    typed_data:
package: # 第三方库
    http:
        http:
            post():
    web:
```


### Data Types
```yaml
DataTypes:
    Runes: # 32位字符对象
    String:
    bool: # 
    int:
    double: # 浮点数
    num: # int、double父类
    Null: # 空类型
    Enum:
    Symbol: # 标识符
    dynamic: # 动态类型，ts中的any
    Object:
    Type: # 类型
```

`var`：声明并初始化变量、自动类型推断
`dynamic`：声明动态类型
`const`：声明常量
`final`：声明不可变量

变量默认值：null



#### String
```dart
// 多行字符串
String str = """
    多行字符串
"""


// 模板字符串
String str = "$xxx";

// 字符串拼接
String str = "a" + "b";
```

支持单引号、双引号、三引号（多行字符串）

默认UTF-16编码




#### List
```dart
// list声明
List list = []

// list类型限定
List list = <int>[]
```

支持扩展预算符：`...`（解构）


#### Set
```dart
// set声明
Set set = {};
```



#### Map
```dart
// Map声明
Map map = {k: v};
```

#### Enum
```dart

```

枚举



#### Symbol
```dart
// Symbol定义
Symbol symbol = #abc;
```

标识符


### Control Flow
```yaml
Control Flow:
    ..: # 对象级联操作运算符
    ?:: # 三元运算符
    ??: # 空类型合并
    ~/: # 整除（向下取整）
    async:
        await:
    class: # 类
        external: # 外部实现
        final:
        get: # getter
        set: # setter
        static: # 静态
        super:
        this:
        with: # 混入mixin
    const: # 常量
    dynamic: # 动态变量
    final: # 常量
    import: # 导入模块 
        as: # 别名
        hide:
        show:
    part of: # 分库实现
        export: # 导出分库
    typedef: # 类型别名
    is / is!: # 类型判断
    var: # 自动类型推断
    for ...:
    for ... in ...: # 迭代遍历
    try ... catch ... finally ...: # 异常处理
```


#### Comment
```dart
// 单行注释

/* 多行注释 */

/// 文档注释
```

#### Exception

`throw`：抛出异常


### Function
```dart
// 函数定义
int add(int a, int b) {
    return a + b;
}

// 匿名函数定义
var add = (int a, int b) {
    return a + b;
};

// 可选参数
int myfunc(int a, [int b]) {
    ...
}
```

类似Java的函数声明

`void main()`：入口函数

函数可嵌套定义、闭包

箭头函数、匿名函数、立即执行函数

必填参数、可选参数、命名参数、函数参数

不指定参数类型，默认dynamic

不支持函数重载

#### Param


##### Optional Param
```dart
void myfunc([int a, int b]) {}

void myfunc({int a, int b}) {}
```

可选参数
位置可选参数、命名可选参数


只有可选参数才支持默认值


##### Function Param
```dart
void test(int add(int a, int b)) {}
```

支持传递函数签名


#### Anonymous
```dart
void test(Function func) {}

test(() {})
test(() => xxx)
```

匿名函数

#### Lambda
```dart
// 闭包函数定义
bool isOdd(n) => n % 2 == 1;
```

箭头函数


#### Async
```dart
Future myfunc() async {
    var x = await xxx();
    return x;
}
```

Future实现异步函数：async函数返回Future、await用于等待Future


##### Future

##### Stream


#### Generic
```dart
// 定义泛型函数
T getData<T>(T value) {
    return value;
}
```




### Class
```dart
class Person {
    // 属性定义
    String name = "233";
    // 默认构造函数
    Person() {}
    // 命名构造函数
    Person.empty() {}
    // 常量构造函数
    const Person() {}
    // 工厂构造函数
    factory Person() {}
    // 方法定义
    void myfunc() {}
}
```

Object为所有类的父类

`new`：类实例化

`this`：自身实例引用
`super`：父类实例引用

`static`: 静态属性、静态方法

`extends`：继承
`implements`：实现
`with`：混入

构造函数：
- 默认构造函数
- 普通构造函数
- 命名构造函数
- 常量构造函数（final字段、不能有函数体、新建常量对象使用const、不使用new）
- 工厂构造函数（无法实例化、默认拦截普通构造函数）

访问修饰符：默认共有、下划线`_`开头表示私有(包内还是可见)

getter/setter：方法前面加 get、set关键字

初始化列表：和C++一样

#### Constructor

支持C++风格的构造函数初始化列表


##### Named Constructor

命名构造函数


##### Const Constructor

常量构造函数
单例实现

##### Factory Constructor


工厂构造函数


#### Abstract
```dart
// 声明抽象类/接口
abstract class Person {
    void info();
}
```

抽象类、接口
extends、implements

抽象类无法实例化，可通过工厂构造函数完成实例化

一个类可实现多个接口

实现接口必须实现接口的属性、方法


#### Mixin
```dart
mixin Action {
    String name = "xxx";
    void getName() {}
}
```

mixin

混入类只能继承自Object
不能有构造函数
后引入的混入覆盖前面的同名属性、方法



#### Extension


扩展函数、方法
中缀表达式



#### Generic
```dart
// 定义泛型类
class Person<T> {
    T value;
    void setValue(T v) {
        this.value = v;
    }
}

// 泛型限定
class Person<T extends OtherClass> {}
```

默认泛型Object





#### Metadata

元数据

@注解
- @override：重写
- @required：必填参数
- @deprecated：过期


### Module
```dart
// 部分引入
import "xxx" show xxx;
import "xxx" hide xxx;

// 延迟引入
import "xxx" deferred as xxx;
xxx.loadLibrary(); # 执行模块加载
```

- 自定义库："xxx/xxx.dart"
- Dart SDK核心库："dart:xxx"
- 第三方库："package:xxx/xxx.dart"

每个dart文件默认都是一个库

`import`：模块导入
`library`：模块定义

`as`：定义库别名
`show`、`hide`：模块部分引入

下划线`_`开头，表示库内私有


主库、从库（用于分文件实现库）
`library`、`part`：建立主库、引入从库（主库设置）
`part of`：和主库建立联系（从库设置）
用于在主库中默认导入从库


### Concurrency

Dart 不同于传统多线程，是 轻量级 isolate 并发

#### SendPort 
#### ReceivePort



