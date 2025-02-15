# puppeteer

## 基础介绍

自动化UI测试框架


## 核心内容
```yaml
puppeteer:
    launch(): # 启动浏览器
        headless:
        --- # 浏览器实例
        newPage():
            $$(): # css选择器
                click():
                getProperty():
                    jsonValue():
            goto(): # 跳转页面
            setViewport():
            waitForSelector():
```