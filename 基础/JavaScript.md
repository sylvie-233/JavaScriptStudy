# JavaScript

`Javascript官方文档：https://developer.mozilla.org/en-US/`



## 基础介绍



DOM对象继承关系：
Object -> EventTarget -> Node -> Element -> HTMLXxxElment



## 核心内容
```yaml
javascript:
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
        HTMLCanvasELement:
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
        WebAssembly: # WASM
            instantiate(): # 实例化模块
                exports:
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
        fromEntries(): # 由键值对创建对象
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

