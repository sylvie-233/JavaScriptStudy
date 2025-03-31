# JavaScript

`Javascript官方文档：https://developer.mozilla.org/en-US/`



## 基础介绍



DOM对象继承关系：
Object -> EventTarget -> Node -> Element -> HTMLXxxElment



## 核心内容
```yaml
javascript:
    window:
        caches:
        cookieStore:
        customElements:
        document:
            addEventListener(): # 
            dispatchEvent(): # DOM分发事件
            getElementById(): # 返回Element对象
            querySelector(): # css选择器
        globalThis:
        history:
        indexedDB: # Database -> ObjectStore -> Index，操作必须在Transaction事务中
            open():
                onerror():
                onsuccess():
                onupgradeneeded():
                    event.target.result: # db对象
                        createObjectStore(): # 创建store
                            add():
                            createIndex(): # 创建索引
                                getAll():
                            delete():
                            get():
                            index():
                            put():
                        transaction(): # 开启事务
                            objectStore(): # 获取store
        innerHeight:
        innerWidth:
        localStorage:
        location:
        menubar:
        navigator:
            clipboard:
            serviceWorker:
        opener:
        outerHeight:
        outerWidth:
        screen:
        scrollX:
        scrollY:
        sessionStorage:
        alert():
        eval():
        fetch():
        getComputedStyle(): # 获取css样式
        getSelection():
        parseInt():
        parseFloat():
        prompt():
    Array: # 数组
        concat():
        filter():
        flat(): 
        from():
        includes():
    ArrayBuffer:
    AsyncFunction:
    Atomics:
    Audio:
    BigInt:
    Blob: # Binary Large Object 二进制数据
        size:
        type:
        arrayBuffer(): # 获取字节缓冲区
        bytes(): # 获取字节数组，Uint8Array
        stream(): # 获取可读流，ReadableStream
        text(): # 获取字符串
    Boolean:
    CustomEvent: # 自定义事件
    Date:
    Element: # HTML、xml基类元素，继承自node
        children:
        classList: # css类属性列表
            add():
            contains():
            remove():
            replace():
            toggle():
        getAttribute():
        removeAttribute():
        setAttribute():
    Error:
    Event: # 事件
        target:
        preventDefault():
        stopPropagation():
    EventTarget: # 事件对象 基类 
        addEventListener():
        dispatchEvent():
        removeEventListener():
    File: # 文件 
        name:
    FileReader: # 文件读取
        readAsArrayBuffer():
        readAsDataURL():
        readAsText():
    Float32Array:
    FormData:
        append():
        delete():
        entries():
        get():
        getAll():
        has():
        keys():
        values():
    Function:
        arguments: # 参数列表
    Generator:
    History: # 浏览器历史
    HTMLAnchorElement: # <a>
        href: # url
        target: # 跳转类型
            _blank:
            _self:
    HTMLAudioElement: # <audio>
    HTMLButtonElement: # <button>
    HTMLCanvasELement: # <canvas>
        height:
        width:
        getContext():
            webgl:
                COLOR_BUFFER_BIT:
                attachShader():
                bindBuffer():
                bufferData():
                clearColor():
                compileShader():
                createBuffer():
                createProgram():
                createShader():
                drawArrays():
                enableVertexAttribArray():
                getAttribLocation():
                getShaderInfoLog():
                getShaderParameter():
                linkProgram():
                shaderSource():
                useProgram():
                vertexAttribPointer():
        toBlob():
    HTMLCollection: # Element集合
    HTMLDivElement: # <div>
    HTMLDocument: # html 文档
    HTMLElement: # 继承自Element
        classList:
        className:
        dataset: # 自定义属性data-*列表
        draggable: # 可拖拽
        id:
        innerHTML:
        isContentEditable: # 内容可编辑
        outerHTML:
        style:
        tagName:
        blur():
        click():
        focus():
    HTMLFormElement: # <form>表单
        action:
        autocomplete:
        elements:
        enctype:
        method:
        checkValidity():
        requestSubmit(): # 模拟提交
        reset():
        submit(): # 手动直接提交
    HTMLImageElement: # <img>
        alt:
        src:
    HTMLInputElement: # <input>
        files:
        form:
        required:
    HTMLLabelElement: # <label>
        htmlFor:
    HTMLMediaElement: # html 媒体元素基类
        autoplay:
        controls:
        duration:
        preload:
        load():
        pause():
        play():
    HTMLScriptElement: # <script>
    HTMLSelectElement: # <select>
        multiple:
        add():
        item():
        remove():
        showPicker():
    HTMLTableElement: # <table>
        createCaption():
        createTBody():
        createTFoot():
        createTHead():
        insertRow():
    HTMLVideoElement: # <video>
    ImageData:
    Location: # 跳转和地址信息
    JSON:
    Map:
        size:
        clear():
        delete():
        get():
        set():
    Math:
    NaN:
    Navigator: # 浏览器信息对象
    Node: # 节点基类
        ATTRIBUTE_NODE:
        CDATA_SECTION_NODE:
        COMMENT_NODE:
        ELEMENT_NODE:
        TEXT_NODE:
        childNodes:
        firstChild:
        lastChild:
        nextSibling:
        nodeName:
        nodeType:
        parentNode:
        previousSibling:
        appendChild():
        cloneNode():
        hasChildNodes():
        removeChild():
    NodeList: # Node集合
    Object: # 顶级基类
        assign(): # 对象浅拷贝
        create(): # 用指定原型创建新对象，(proto, [propertiesObject])
            configurable:
            enumerable:
            value:
            writable:
        defineProperty(): # 定义属性
        defineProperties(): # 批量定义多个属性
        entries(): # k-v键值对
        freeze(): # 冻结对象，使其属性不可修改、不可添加、不可删除
        fromEntries(): # 由键值对创建对象
        getOwnPropertyDescriptors(): # 获取属性描述符
            configurable: # 可添加、删除
            enumerable: # 可枚举
            value: # 属性值
            writable: # 可修改
        getOwnPropertyNames(): # 获取对象的所有自身属性（包括不可枚举的）
        getOwnPropertySymbols():
        getPrototypeOf(): # 获取原型对象
        hasOwn(): # 属性存在判断
        is(): # 判断对象严格相等
        isExtensible(): # 检查对象是否可以扩展（添加新属性）
        isSealed(): # 检查对象是否被密封（无法添加/删除属性，但可修改现有属性）
        isFrozen(): # 检查对象是否被冻结（属性不能修改、添加、删除）
        keys(): # 可枚举属性名
        preventExtensions(): # 禁止新增属性，但可以修改和删除已有属性
        seal(): # 不可添加/删除属性，但可以修改已有属性
        setPrototypeOf(): # 设置原型对象
        values(): # 可枚举属性值
    Promise: # 异步Future Promise
        all():
        allSettled():
        any():
        catch():
        finally():
        race(): # 第一个完成的 Promise 决定最终结果
        reject():
        resolve():
        then():
    Proxy: # 对象拦截，13种
        apply(): # 函数自调用拦截，(target, thisArg, argsList)
        construct(): # (target, args, newTarget)
        defineProperty(): # (target, prop, descriptor)
        deleteProperty(): # (target, prop)
        get(): # getter，(target, prop, receiver)
        getOwnPropertyDescriptor(): # (target, prop)
        getPrototypeOf(): # (target)
        isExtensible(): # (target)
        ownKeys(): # (target)
        preventExtensions(): # (target)
        set(): # setter，(target, prop, value, receiver)
        setPrototypeOf(): # (target, prototype)
        has(): # (target, prop)
    Range:
    ReadableStream: # 可读流
        getReader():
        pipeTo():
    Reflect:
        apply():
        construct():
        deleteProperty():
        get():
        getOwnPropertyDescriptor():
        getPrototypeOf():
        has():
        isExtensible(): 
        ownKeys():
        preventExtensions():
        set():
        setPrototypeOf():
    RegExp:
    Set:
        add():
        clear():
        delete():
        has():
    String: # 字符串
    Symbol: # 符号key（常用于魔术方法key）
        hasInstance:
        isConcatSpreadable:
        iterator:
        for():
    Uint8Array:
    URL: # 
        createObjectURL(): # 创建临时可访问url，Blob，File，临时数据
        parse():
        revokeObjectURL(): # 释放 URL
        toString():
    Video:
    WeakMap:
    WeakRef:
    WeakSet:
    WebAssembly: # WASM
        instantiate(): # 实例化模块
            exports:
    WebSocket: # websocket
        readyState:
        addEventListener():
            close:
            error:
            message:
            open:
        send():
    Worker: # 子js线程，操作类似socket
        addEventListener():
            message:
        onerror():
        onmessage(): # 接收消息
        postMessage(): # 传递消息
        terminate(): # 结束
    XMLHttpRequest:
        onreadystatechange:
        readyState:
        response:
        status:
        open():
        send():   
```

### Data Types
```yaml
DataType:
    Array:
    ArrayBuffer:
    Atomics:
    Bigint:
    Boolean:
    Date:
    Error:
    Float32Array:
    Function:
        arguments:
    Map:
    Math:
    NaN:
    Number:
    Objet:
    Proxy:
    Reflect:
    RegExp:
    Set:
    String:
    Symbol:
    Uint32Array:
    Uint8Array:
    WeakMap:
    WeakRef:
    WeakSet:
```


#### String

模板字符串



#### Array

数组


#### Promise

异步Future

Promise状态：
- pending（进行中）—— 初始状态，既未 resolve 也未 reject
- fulfilled（已成功）—— resolve(value) 被调用，表示操作成功
- rejected（已失败）—— reject(error) 被调用，表示操作失败



### Control Flow
```yaml
Control Flow:
    const: # 常量定义（块级）
    delete:
    function*: # 生成器函数
    in: # 元素、属性存在判断
    import:
        meta:
    let: # 局部变量定义（块级）
    yield:
    var: # 全局变量定义 （声明提升）
    for ... of ...:
```


#### Doc Comment
```yaml
Doc Comment:
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


### Function

箭头函数

#### Generator

iterator



### Class

class




### Module


export、import



### Test




#### SourceMap
```yaml
.map:
    file: # 构建文件名称
    mappings: # 源码映射关系
    names: # 记录字面量的数组
    sources: # 记录源文件的数组
    sourcesContent: # 源码内容
    version: # source map 版本
```

源文件 -> map文件 -> 构建文件





## BOM

浏览器操作对象


## DOM

HTML文档操作对象


### Canvas



## Web Components
```jsx
class CustomGreeting extends HTMLElement {
    constructor() {
        super();
        
        // 创建影子 DOM
        const shadow = this.attachShadow({mode: 'open'});

        // 创建模板内容
        const template = document.createElement('template');
        template.innerHTML = `
            <style>
            p {
                color: blue;
                font-size: 20px;
            }
            </style>
            <p>Hello, <span></span>!</p>
        `;

        // 将模板内容克隆并添加到影子 DOM
        shadow.appendChild(template.content.cloneNode(true));

        // 获取 name 属性并设置文本内容
        const span = shadow.querySelector('span');
        span.textContent = this.getAttribute('name') || 'Guest';
    }
}

// 注册自定义元素
customElements.define('custom-greeting', CustomGreeting);

// 使用自定义 Web Component
<custom-greeting name="World"></custom-greeting>
```




## WebGL
```js
const canvas = document.getElementById('webglCanvas');
const gl = canvas.getContext('webgl');

if (!gl) {
    alert('WebGL not supported');
}

// 清除背景色
gl.clearColor(0.0, 0.0, 0.0, 1.0);
gl.clear(gl.COLOR_BUFFER_BIT);

// 定义顶点数据
const vertices = new Float32Array([
    -0.5, -0.5,  // 左下角
    0.5, -0.5,   // 右下角
    0.5, 0.5,    // 右上角
    -0.5, 0.5    // 左上角
]);

// 创建缓冲区并加载顶点数据
const vertexBuffer = gl.createBuffer();
gl.bindBuffer(gl.ARRAY_BUFFER, vertexBuffer);
gl.bufferData(gl.ARRAY_BUFFER, vertices, gl.STATIC_DRAW);

// 顶点着色器（负责将顶点坐标映射到屏幕空间）
const vertexShaderSource = `
    attribute vec2 a_position;
    void main() {
    gl_Position = vec4(a_position, 0.0, 1.0);
    }
`;

// 片段着色器（设置像素颜色）
const fragmentShaderSource = `
    void main() {
    gl_FragColor = vec4(0.0, 1.0, 0.0, 1.0); // 绿色
    }
`;

// 创建并编译着色器
function createShader(type, source) {
    const shader = gl.createShader(type);
    gl.shaderSource(shader, source);
    gl.compileShader(shader);
    if (!gl.getShaderParameter(shader, gl.COMPILE_STATUS)) {
    console.error('Shader compile error:', gl.getShaderInfoLog(shader));
    }
    return shader;
}

const vertexShader = createShader(gl.VERTEX_SHADER, vertexShaderSource);
const fragmentShader = createShader(gl.FRAGMENT_SHADER, fragmentShaderSource);

// 创建程序并链接着色器
const shaderProgram = gl.createProgram();
gl.attachShader(shaderProgram, vertexShader);
gl.attachShader(shaderProgram, fragmentShader);
gl.linkProgram(shaderProgram);

if (!gl.getProgramParameter(shaderProgram, gl.LINK_STATUS)) {
    console.error('Program link error:', gl.getProgramInfoLog(shaderProgram));
}

gl.useProgram(shaderProgram);

// 获取顶点着色器中的 a_position 属性位置
const positionLocation = gl.getAttribLocation(shaderProgram, 'a_position');
gl.vertexAttribPointer(positionLocation, 2, gl.FLOAT, false, 0, 0);
gl.enableVertexAttribArray(positionLocation);

// 绘制矩形
gl.drawArrays(gl.TRIANGLE_FAN, 0, 4);
```


基于过程式编程的渲染引擎




### Vertices

顶点数据


### Buffer

缓冲区


### Shader

着色器

#### VertexShader

顶点着色器


#### FragmentShader

片段着色器

### Program

渲染程序、可多个用于不同地方
组织数据、着色器



## WebAssembly

`.wasm`

