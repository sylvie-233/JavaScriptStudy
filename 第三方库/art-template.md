# art-template

## 基础介绍

javascript模板渲染引擎

可集成express：`express-art-template`


## 核心内容
```yaml
art-template:
    defaults:
        cache:
        debug:
        extname: # 文件扩展名(.art)
        htmlMinifierOptions:
        imports: # 全局变量注册
        loader: # 文件加载器
        minimize:
        root: # 文件根目录
        rules:
            test:
            use:
                code:
                output:
    extensions:
    ():
    compile():
    render():
```


### 语法结构
```yaml
:
    {{}}:
        @: # 原始输出
        block ...: # 模板插槽
        each ...: # 列表渲染
            $index:
            $value:
        extend ...: # 模板继承
        if ... else if ... /if:
        include ...: # 模板引入
        print ...: # 字符串打印
        set ...: # 定义变量
    $imports:
```


支持标准语法、原始语法两种




### Filter过滤器