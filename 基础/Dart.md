# Dart

`Dart官方文档：https://dart.dev/docs`
`拉钩教育Dart教程：P21`

## 基础介绍

谷歌开发的、类型安全、面向对象的编程语言`.dart`

Flutter SDK包含Dart SDK

每行结束必须携带分号`;`
Dart万物皆对象，引用传递


### dart
```yaml
dart:

```


### pub
```yaml
pub:
    get:
```

dart包管理工具


#### pubspec.yaml
```yaml
pubspec.yaml:
    environment:
        sdk:
    dependencies: # 依赖包
    name:
```

dart包配置文件


## 核心内容
```yaml
dart:
    async:
        Future:
            catchError():
            then():
        Stream:
    cli:
    collection:
    convert:
        JsonDecoder:
        JsonEncoder:
        jsonDecoder():
        jsonEncoder():
    core: # 内置模块
        BigInt:
        Comparable:
        DateTime:
            now():
        Enum:
        Function:
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
        Map:
            keys:
            values:
            containsKey():
            containsValue():
            putIfAbsent():
            remove():
            removeWhere():
        MapEntry:
        Match:
        Null:
        Object:
        Pattern:
        Record:
        RegExp:
        Runes:
        Set:
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
            replaceAll():
            split(): # 字符串分隔
            trim(): # 空白符去除
        StringBuffer:
        Symbol:
        Type:
        Uri:
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
        print():
    developer:
    ffi:
    io:
    isolate:
    math:
    typed_data:
package:
    http:
        http.dart:
            post():
    web:
```


### 数据类型
```yaml
DataTypes:
    Runes: # 32位字符对象
    String:
    Symbol: # 标识符
    bool:
    dynamic: # 动态类型
    int:
```

`var`：声明并初始化变量、自动类型推断
`dynamic`：声明动态类型
`const`：声明常量
`final`：声明不可变量

变量默认值：null



#### 字符串
```dart
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


#### Symbol
```dart
// Symbol定义
Symbol symbol = #abc;
```

标识符


### 控制流程
```yaml
Control Flow:
    ..: # 对象级联操作运算符
    ?? / ??=: # 空类型判断
    ~/: # 整除（向下取整）
    const: # 常量
    dynamic: # 动态变量
    is / is!: # 类型判断
    var: # 自动类型推断
    for ...:
    for ... in ...: # 迭代遍历
    try ... catch ... finally ...: # 异常处理
```


#### 注释
```dart
// 单行注释

/* 多行注释 */

/// 文档注释
```

#### 异常处理


### 函数
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


#### lambda
```dart
// 闭包函数定义
bool isOdd(n) => n % 2 == 1;
```

箭头函数


#### 异步函数
```dart
Future myfunc() async {
    var x = await xxx();
    return x;
}
```

Future实现异步函数：async函数返回Future、await用于等待Future


### 面向对象
```dart
```

`new`：类实例化



### 模块



### 并发