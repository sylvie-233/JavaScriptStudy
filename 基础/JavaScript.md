# JavaScript

`Javascript官方文档：https://developer.mozilla.org/en-US/`



## 基础介绍



DOM对象继承关系：
Object -> EventTarget -> Node -> Element -> HTMLXxxElment



## 核心内容
```yaml
:
    windows:
        Element:
            classList: # css类属性列表
                add():
                contains():
                remove():
                replace():
                toggle():
        EventTarget:
        File:   
        FormData:
            append():
            delete():
            entries():
            get():
            getAll():
            has():
            keys():
            values():
        History:
        HTMLButtonElement:
        HTMLCollection:
        HTMLDivElement:
        HTMLDocument:
        HTMLElement:
            dataset: # 自定义属性data-*列表
        HTMLFormElement:
        HTMLInputElement:
        HTMLScriptElement:
        ImageData:
        Location:
        Navigator:
        Node:
        document:
            getElementById(): # 返回Element对象
            querySelector(): # css选择器
        globalThis:
        alert():
        eval():
        prompt():
    Array:
        concat():
        filter():
        flat(): 
        from():
        includes():
    AsyncFunction:
    Atomics:
    BigInt:
    Boolean:
    Date:
    Float32Array:
    Function:
        arguments:
    JSON:
    Map:
        size:
        clear():
        delete():
        get():
        set():
    Math:
    NaN:
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
    Promise:
    Proxy:
    Reflect:
        apply():
        has():
        ownKeys():
        preventExtensions():
        setPrototypeOf():
    RegExp:
    Set:
        add():
        clear():
        delete():
        has():
    String:
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


#### 文档注释
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


### 函数

箭头函数

#### 生成器

iterator



### 面向对象

class




### 模块


export、import



### 测试




#### SourceMap
```yaml
:
    mappings:
    names: 记录字面量的数组
    sources: 记录源文件的数组
    sourcesContent:
    version:
```






## BOM

浏览器操作对象


## DOM

HTML文档操作对象




