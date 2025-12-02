# Dart

`Dart官方文档：https://dart.dev/docs`
`Dart生态库：https://pub.dev/`
`Dart入门实战教程：P10`

## 基础介绍

谷歌开发的、类型安全、面向对象的编程语言`.dart`（类似C++、Java、Python结合）
Dart 官方（包括 Flutter 团队）刻意让 dart:xxxx 标准库保持非常小、非常稳定，避免频繁更新导致兼容性破坏（path、test、http、lints都是官方维护的第三方包）
Flutter SDK包含Dart SDK


`PUB_CACHE`: 全局缓存路径，第三方包安装
- Windows：`C:\Users\<UserName>\AppData\Local\Pub\Cache`
- macOS/Linux：`~/.pub-cache`


- 文件结构和Java类似、每行结束必须携带分号`;`
- Dart万物皆对象，引用传递
- 支持自动类型推断，变量声明、函数返回值
- 实例化对象不用写new
- dart:core包默认导入
- 字符串支持单引号、双引号
- Isolate 是 Dart 的“线程”，但不共享内存
- Dart 代码默认只有一个线程（main isolate），一切异步都是事件循环，需要真正 CPU 并发时才会创建额外的 Isolate
- 每个 Dart 文件本质上是一个 library，如果没有显式写 library xxx;，文件本身就是一个独立的 library
- 以 _ 开头的符号是私有的（private），私有符号 只能在同一个 library（或 part 文件集合）中访问，库外不可见
- library中 只有通过 export 的符号才能被包外部访问
- mixin混入可以使用with、implements实现（mixin 可以像多继承一样复用方法/属性）
- Iterable惰性计算的可迭代对象


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


#### analysis_options.yaml
```yaml
analysis_options.yaml:
    include: # 导入其它配置
        package:lints/recommended.yaml:
    analyzer: # 静态分析器配置
        exclude: # 排除文件/目录
        errors: # 控制规则错误等级（让某些规则不报错）
            dead_code:
            invalid_assignment:
            unused_import:
        language: # 控制 Dart 语言特性
            enableSuperMixins:
            strict-inference:
        strong-mode: # language旧配置
        plugins: # 插件配置
            dart_code_metrics:
    linter: # 格式化配置
        rules: # 格式化规则
            always_use_package_imports:
            avoid_print:
            camel_case_types:
            prefer_const_constructors:
            use_key_in_widget_constructors:

```

项目的统一静态分析与 Lint 配置文件


### dart
```yaml
dart:
    -h:
    -v: # 版本
    analyze:
    compile: # 编译
        exe: # 编译exe可执行程序
            -o: # 文件输出
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
            --dev: # 添加开发依赖
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
        --coverage:
        --name:
```

dart命令行工具




#### pubspec.yaml
```yaml
pubspec.yaml:
    name: # 项目名
    version: # 项目版本号
    description: # 项目描述
    environment: # 项目环境要求
        sdk: # sdk要求
    flutter:
        uses-material-design:
    dependencies: # 依赖包
    dev_dependencies: # 开发依赖
    dependency_overrides: # 依赖覆盖
    publish_to: # 发布包
```

dart包配置文件


## 核心内容
```yaml
dart:
    async: # 异步
        Future: # 异步Promise
            await(): # 批量异步Future等待
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
            first:
            isEmpty:
            isNotEmpty:
            last:
            length: # 列表长度
            reversed:
            add(): # 添加元素
            addAll():
            any():
            clear():
            contains():
            empty():
                growable():
            every():
            expand(): # 列表降维
            filled(): # 构造函数 填充构造
            fold(): # reduce迭代计算 
            forEach(): # 迭代遍历
            indexOf():
            insert(): # 插入元素
            insertAll():
            join(): #元素合并字符串
            map(): # 元素转换
            remove(): # 删除元素
            removeAt(): # 删除元素
            removeLast():
            removeRange():
            sort():
            sublist(): # 切片
            toSet():
            where(): # 条件过滤
                skip():
                take():
                toList():
        Map: # 哈希表
            entries:
            isEmpty:
            isNotEmpty:
            length:
            keys:
            values:
            addAll():
            clear():
            containsKey():
            containsValue():
            from():
            fromIterable():
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
            toList(): # 转换为List列表
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
            spawn(): # 线程运行
        ReceivePort: # 接收管道
            first: # 第一个接收元素
            sendPort: # 发送管道
            close():
            listen(): # 接收消息
        SendPort: # 发送管道
            send(): # 发送消息
    math: # 数学库
        pi:
        max():
        min():
    mirrors: # 反射
        ClassMirror: # 反射类型对象
            instanceMembers:
            metadata: # 反射元数据
            simpleName:
            newInstance(): # 创建实例对象 
        InstanceMirror: # 反射对象
            type:
            getField():
                reflectee:
            invoke(): # 
            setField():
        reflect(): # 获取反射对象InstanceMirror
        reflectClass(): # 获取反射类型对象classMirror
    typed_data:
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
// 字符串定义
String str = 'xxx';

// 多行字符串
String str = """
    多行字符串
"""


// 模板字符串（双引号字符串支持模板插值）
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
List<int> list = <int>[]
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
Map map = {'k': v};


// 类型声明
Map<String, int> scores = {
  'math': 90,
};
```

#### Enum
```dart
// 定义枚举
enum Color {
  red,
  green,
  blue,
}

// 获取枚举所有值
// [Color.red, Color.green, Color.blue]
print(Color.values); 

// 获取枚举的name
print(Color.red.name)

// 获取枚举的index
print(Color.red.index); // 0

// 自定义构造枚举
enum Color {
  red(0xff0000),
  green(0x00ff00),
  blue(0x0000ff);

  final int hex;

  const Color(this.hex);

  void printHex() => print(hex.toRadixString(16));
}
```

枚举



#### Symbol
```dart
// Symbol定义
Symbol symbol = #abc;
```

Dart 中用于表示标识符（变量名、类名、方法名）的一种对象


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
    const: # 常量定义
    dynamic: # 动态变量
    final: # 常量定义
    import: # 导入模块 
        as: # 别名
        hide:
        show:
    is / is!: # 类型判断
    late: # 变量延迟初始化
    part of: # 分库实现
        export: # 导出分库
    switch:
        case:
        default:
            break:
    typedef: # 类型别名
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

#### Exception Handler
```dart
// 异常处理定义
try {
    int result = 10 ~/ 0;
} on IntegerDivisionByZeroException {
    print("除零错误");
} on FormatException catch (e) {
    print("格式错误: $e");
} catch (e, s) {
    print("其他异常: $e");
    print("堆栈信息: $s");
}

// 自定义异常
class MyException implements Exception {
  final String message;
  MyException(this.message);
  @override
  String toString() => "MyException: $message";
}
// 抛出异常
throw MyException("自定义异常");
```

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

// [] 可选参数定义
int myfunc(int a, [int b]) {
    ...
}

// {} 命名参数定义
void greet({String name = "Guest", int age = 0}) {
    print('Hello $name, $age');
}
```

类似Java的函数声明

`void main()`：入口函数

函数可嵌套定义、闭包

箭头函数、匿名函数、立即执行函数

必填参数、可选参数、命名参数、函数参数

- 不指定参数类型，默认dynamic
- 不支持函数重载
- 函数内部还可以定义函数

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


#### Lambda
```dart
// 匿名函数定义
void test(Function func) {}

test(() {})
test(() => xxx)

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
```dart
// 定义异步函数
Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 1));
  return "data";
}
```

异步响应结果

##### Stream
```dart
// 单订阅 Stream
Stream<int> countStream() async* {
  for (var i = 0; i < 5; i++) {
    yield i;
    await Future.delayed(Duration(milliseconds: 500));
  }
}

await for (var n in countStream()) {
    print(n);
}
```

流式异步响应结果
模拟生成器


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

访问修饰符：默认共有、下划线`_`开头表示私有(包内还是可见)
getter/setter：方法前面加 get、set关键字

初始化列表：和C++一样

#### Constructor

支持C++风格的构造函数初始化列表
构造函数：
- 默认构造函数
- 普通构造函数
- 命名构造函数
- 常量构造函数（final字段、不能有函数体、新建常量对象使用const、不使用new）
- 工厂构造函数（无法实例化、默认拦截普通构造函数）


##### Named Constructor

命名构造函数


##### Const Constructor

常量构造函数
单例实现

##### Factory Constructor


工厂构造函数


#### Getter / Setter
```dart
class BankAccount {
  double _balance = 0;

  double get balance => _balance;

  set balance(double value) {
    if (value < 0) throw Exception("Balance cannot be negative");
    _balance = value;
  }
}
```

属性获取器、存储器


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

- with、implements使用
- 混入类只能继承自Object
- 不能有构造函数
- 不能继承类（但可以 implements 接口）
- 不适合作为类型（默认不代表一种类型）
- 后引入的混入覆盖前面的同名属性、方法



#### Extension
```dart
// 定义扩展函数
extension StringExtension on String {
  String capitalize() {
    // this引用对象实例
    return this.isEmpty
        ? this
        : this[0].toUpperCase() + substring(1);
  }
}

// 使用扩展函数
print("hello".capitalize()); // Hello
```


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
```dart
// 自定义注解
class Api {
  final String path;

  const Api(this.path);
}

// 使用自定义注解
@Api("/hello")
class Hello {}

// 反射获取注解
var cm = reflectClass(Hello);

for (var m in cm.metadata) {
    var a = m.reflectee as Api;
    print(a.path);
}
```

注解、元数据
要自定义一个注解，你只需要创建一个“常量类”

@注解
- @override：重写
- @required：必填参数
- @deprecated：过期


### Module
```dart
// 相对导入（包内可用）
import 'src/a.dart';

// package 导入（包外/包内都可用）
import 'package:my_package/my_package.dart';

// 部分引入
import "xxx" show xxx;
import "xxx" hide xxx;

// 导出
export 'src/a.dart';
export 'src/b.dart' show B;    // 只导出 B
export 'src/c.dart' hide _helper; // 隐藏某些成员

// 延迟引入
import "xxx" deferred as xxx;
xxx.loadLibrary(); # 执行模块加载

// 多模块，将同一个 library 拆成多文件
// lib/foo.dart
library foo;
part 'foo_part.dart';
// lib/foo_part.dart
part of foo;

// 条件导入
import 'src/io_impl.dart'
  if (dart.library.html) 'src/web_impl.dart';
```

Library -> Package -> Module
- 自定义库："xxx/xxx.dart"
- Dart SDK核心库："dart:xxx"
- 第三方库："package:xxx/xxx.dart"

每个dart文件默认都是一个模块

`import`：模块导入
`library`：模块定义

`as`：定义库别名
`show`、`hide`：模块部分引入

下划线`_`开头，表示库内私有


主库、从库（用于分文件实现库）
`library`、`part`：建立主库、引入从库（主库设置）
`part of`：和主库建立联系（从库设置）
用于在主库中默认导入从库


### Isolate

Dart 不同于传统多线程，是 轻量级 isolate 并发

#### SendPort 
#### ReceivePort



