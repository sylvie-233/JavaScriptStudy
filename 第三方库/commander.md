# Commander


## 基础介绍

nodejs命令行工具

- commander：定义命令
- inquirer：命令交互
- ora：命令交互



## 核心内容
```yaml
commander:
    program:
        command():
            action(): # 命令执行
            alias():
            description():
        parse():
        version():
    command(): # 定义命令
        action(): # 定义命令动作
        description():
    parse(): # 解析命令行参数
    version():

download-git-repo:

inquirer:
    prompt():
        choices:
        default:
        message:
        name:
        type:
            checkbox:
            confirm:
            input:
            list:
        validate():

ora:
    start():
    succeed():
```
