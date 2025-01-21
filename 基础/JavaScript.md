# JavaScript

``



## 基础介绍



## 核心内容
```yaml
:
    windows:
        FormData:
            append():
            delete():
            entries():
            get():
            getAll():
            has():
            keys():
            values():
    Array:
        concat():
        filter():
        flat(): 
        from():
        includes():
    Function:
        arguments:
    Map:
        size:
        clear():
        delete():
        get():
        set():
    Object:
        assign():
        create():
            configurable:
            enumerable:
            value:
            writable:
        defineProperty():
        entries():
        fromEntries():
        getOwnPropertyDescriptors():
            configurable:
            enumerable:
            value:
            writable:
        getPrototypeOf():
        is():
        keys():
        setPrototypeOf():
        values():
    Proxy:
    Reflect:
        apply():
        has():
        ownKeys():
        preventExtensions():
        setPrototypeOf():
    Set:
        add():
        clear():
        delete():
        has():
    Symbol: # 符号key（常用于魔术方法key）
        hasInstance:
        isConcatSpreadable:
        iterator:
        for():
    XMLHttpRequest:
        onreadystatechange:
        readyState:
        response:
        status:
        open():
        send():
```

### 数据类型
```yaml
DataType:
    Array:
    Function:
        arguments:
    Number:
    String:
    Symbol:
```


#### String

模板字符串






### 控制流程
```yaml
:
    const: # 常量定义（块级）
    let: # 局部变量定义（块级）
    var: # 全局变量定义 （声明提升）
```


### 函数

箭头函数

#### 生成器

iterator



### 面向对象

class




### 模块


export、import



### 测试



### 文档注释
```yaml
文档注释:
    @author: 
        author-name:
        <contact-way>: 联系方式
    @class: 类
    @constructor: 构造方法
    @date: 日期
    @deprecated: 过时
        comments:
    @example: 样例（一般写在最后一行）
    @extends: 继承
    @inheritdoc: 继承重写
    @license: 许可证
        license-info:
    @returns: 返回类型
        {type}:
        comments:
    @param: 标注参数
        {type}:
        param-name:
        comments:
    @private: 私有成员
    @property: 对象属性定义
    @protected: 保护成员
    @public: 公共成员
    @readonly: 只读
    @throws: 异常抛出定义（一般写在return后面）
        {type}:
        comments:
    @type: 变量类型
    @typedef: 对象定义
```

第一行写描述信息，文档注释只能用`/** */`标注，单行注释`//`无用

对象类型的参数应该对每个属性写一行注释



版权声明
```javascript
/**
 * @license
 * 
 * 项目一 版本1.0.0                             仓库名  版本号
 * (c) 2023年 ISail                            版权年份 版权所属人
 * 根据Apache许可证2.0发布                      许可证 
 * 
 * SPDX-License-Identifier: Apache-2.0         许可证信息  
 * 
 * 了解更多信息，请访问:
 * https://www.apache.org/licenses/LICENSE-2.0   许可证链接
 */

```

对象类型定义
```javascript
/**
 * @typedef {object} User
 * @property {string} name
 * @property {number} age
 */
```

### SourceMap
```yaml
:
    mappings:
    names: 记录字面量的数组
    sources: 记录源文件的数组
    sourcesContent:
    version:
```






## 扩展




