# hexo


## 基础介绍

一个快速、简洁且高效的博客框架，基于 Node.js

安装：
`npm install -g hexo-cli`



- 主题默认使用ejs模板引擎


### 项目结构
```yaml
hexo:
    /public: # 打包目录
    /scaffolds:
    /source: # 内容
        /_data: # 内容
        /_posts: # 博客

        /css:
        /img:
        /js:
    /themes: # 主题
        /language:
        /layout:
            /_partial:
                footer.ejs:
            /_widget:
        /scaffolds:
        /source:
            /css:
            /js:
        _config.yml:
    _config.yml:
    package.json:
```


#### _config.yml
```yaml
_config.yml:
    author:
    deploy: # 部署
        type:
    feed:
    inject: # 注入
        head:
        bottom:
    menu: # 菜单
    plugins:
    rss:
    search: # 搜索
    sitemap:
    theme: # 主题
    title: # 标题
    url:
```


### hexo
```yaml
hexo:
    -v:
    clean:
    deploy: # d 发布
    generate: # g 打包
    init: # 初始化项目
    new:
        page:
        post:
        theme: # 主题
    server: # s 运行
```


## 核心内容
```yaml
global:
    date:
    title:
    tags:
---
hexo:
    
```


### Theme


### Plugin