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
    --ext: # 指定源文件扩展名
    --fix: # 自动修复
    --init: # 生成配置文件

```






#### eslint.config.js
```yaml

```



#### .eslintignore
```yaml

```



#### .eslintrc
```yaml
.eslintrc:
    env: # 代码环境
        es6:
        node:
    extends: # 配置继承
        eslint:
            recommended:
        next:
        next/core-web-vitals:
    globals: # 全局声明（无需import）
    overrides: # 重写配置
    parser: # "babel-eslint|"
    parserOptions:
        sourceType:
    plugins: # eslint插件
    rules: # 检查规则
        block-spacing: # "always"
        linebreak-style: # "error|unix"
        no-console:
        no-unused-vars:
        quotes: # "single"
        semi: # "always"
        
```


### prettier
```yaml
prettier:
    --write:
```


代码格式化工具

可在`package.json`中添加`prettier`字段





#### .prettierrc
```yaml
.prettierrc:
    printWidth:
    quotes:
    semi:
    semicolons:
    singleQuote:
    tabs:
    tabWidth:
```

prettier格式化配置文件（vscode插件）



#### .prettierignore
```yaml
```




## 核心内容
```yaml
prettier:
    format():
```




## Prettier

