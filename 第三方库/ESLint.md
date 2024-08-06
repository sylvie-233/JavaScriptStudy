# ESLint


## 基础介绍

代码检查工具，可用来统一代码风格

eslint可配置的信息主要分为3类：
- env：js运行的环境
- globals: 执行代码需要访问的全局变量
- rules: 开启某些规则，也可设置规则的等级




### eslint
```yaml
eslint:
    --ext: 指定源文件扩展名
    --fix: 自动修复
    --init: 生成配置文件

```

### .eslintrc.js
```yaml
:
    env: 代码环境
        es6:
        node:
    extends: 配置继承
    parser:
        "babel-eslint|"
    parserOptions:
        sourceType:
    plugins: eslint插件
    rulse: 检查规则
        block-spacing:
            "always"
        linebreak-style:
            "error|unix"
        no-console:
        quotes:
            "single"
        semi:
            "always"
        
```



## 核心内容

