# ejs

## 基础介绍

### ejs
```yaml
ejs:
    -f: # 数据文件
    -o: # 输出文件
```


## 核心内容
```yaml
ejs:
    cache:
    delimiter:
    fileLoader: # 自定义文件加载器
    compile(): # 编译模板
    render(): # 渲染模板
    renderFile(): # 渲染模板（文件）
        _options:
            cache:
            closeDelimiter: # 默认 >
            context:
            delimiter: # 默认 %
            localsName:
            openDelimiter: # 默认 <
            rmWhitespace:
            root:
            views:
```

### 模板语法
```yaml
:
    <% %>: # 控制语句
        if... else if ... else:
    <%- -%>: # 原串输出
    <%= %>: # 变量输出
    include(): # 模板引入
```