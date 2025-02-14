# Dart

`Dart官方文档：https://dart.dev/docs`
`拉钩教育Dart教程：P13`

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

```

dart包管理工具


## 核心内容
```yaml
dart:
    async:
    collection:
    convert:
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
            where():
                toList():
        Map:
        MapEntry:
        Match:
        Null:
        Object:
        Pattern:
        Record:
        RegExp:
        Runes:
        Set:
        Stream:
        String: # 字符串
            contains():
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
    web:
```


### 数据类型
```yaml
DataTypes:
    String:
    bool:
    dynamic: # 动态类型
    int:
```

`var`：声明并初始化变量、动态数据类型
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


#### List
```dart
// list声明
List list = []

// list类型限定
List list = <int>[]
```

支持扩展预算符：`...`（解构）



### 控制流程
```yaml
Control Flow:
    const: # 常量
    dynamic: # 动态变量
    var: # 动态变量
    for ...:
    for ... in ...: # 迭代遍历
```

#### 注释
```dart
// 单行注释

/* 多行注释 */

/// 文档注释
```



### 函数
```dart
// 函数定义
int add(int a, int b) {
    return a + b;
}
```

`void main()`：入口函数

无参函数调用可以不带括号


#### 闭包
```dart
// 闭包函数定义
bool isOdd(n) => n % 2 == 1;
```


#### 异步函数
```dart
```


### 面向对象



### 模块



### 并发