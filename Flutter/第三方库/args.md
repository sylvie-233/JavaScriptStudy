# args


## 基础介绍


Dart 官方提供的 命令行参数解析库


## 核心内容
```yaml
args/args.dart:
    ArgParser: # 参数解析器
        arguments:
        command:
        addCommand(): # 添加子命令
            addFlag():
            addOption():
        addFlag(): # 添加 布尔开关 参数
            abbr:
            negatable:
            help:
        addOption(): # 添加 带值参数
            abbr:
            help:
            defaultsTo:
        addMultiOption(): # 添加 列表参数
        parse(): # 解析参数
```