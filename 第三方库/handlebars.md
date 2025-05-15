# handlebars

## 基础介绍

hbs模板引擎

### 模板语法
```yaml
    {{ var }}:
    {{!-- comment --}}:
    {{{ html }}}:
    {{> }}: # 代码片段（include实现）
    {{# }}:
        each ... else ... /each:
            this:
            @first:
            @index:
            @last:
            @key:
        if ... else ... /if:
        list ... /list:
        unless ... /unless:
        with ... /with:
```

## 核心内容
```yaml
handlebars:
    compile(): # 编译
        (): # 页面渲染
    registerHelper(): # 注册辅助函数
        options:
            fn(): # 渲染函数
    registerPartial(): # 注册代码片段
express-handlerbars: # 兼容express的模板引擎，支持默认layouts、partials
    create():
        engine: # 引擎
    engine():
        extname:
        runtimeOptions:
```

### 条件渲染


### 列表渲染


### 辅助函数


### 模板插槽


### 模板引入
