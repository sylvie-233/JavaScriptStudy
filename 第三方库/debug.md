# debug


## 基础介绍

debug输出


以name进行区分，由`DEBUG`环境变量控制name模块的debug输出



## 核心内容
```yaml
debug:
    enabled:
    formatters:
    log:
    enable():
    extend(): # 继承name命名空间
```


### Formatter

输出格式化
- %O: 对象
- %o
- %s: 字符串
- %d: 数字


自定义格式化器
```js
const createDebug = require('debug')
createDebug.formatters.h = (v) => {
  return v.toString('hex')
}

// …elsewhere
const debug = createDebug('foo')
debug('this is hex: %h', new Buffer('hello world'))
//   foo this is hex: 68656c6c6f20776f726c6421 +0ms
```


### Browser

debug浏览器端支持

`localStorage.debug`设置输出的name模块