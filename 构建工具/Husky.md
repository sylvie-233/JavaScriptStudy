# husky


## 基础介绍

Husky 是一个用于在 Git 钩子（如 pre-commit、pre-push 等）中运行脚本的工具，广泛用于自动化代码检查、格式化、测试等任务。它常与 Linting（代码检查）、Prettier（代码格式化）等工具结合使用，确保团队成员提交的代码符合一致的质量标准

命令`exit 1`中断git

### husky
```yaml
husky:
    add: # 添加
        .husky:
            post-commit:
            post-push:
            pre-commit:
            pre-push:
    install: # 生成.husky目录
```


## 核心内容
```yaml

```