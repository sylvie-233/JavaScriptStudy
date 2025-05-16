# winston

## 基础介绍

javascript日志库


## 核心内容
```yaml
winston:
    format: # 格式化器
        combine():
        json():
        label():
        prettyPrint():
        printf():
        timestamp():
    loggers:
        add(): # 添加日志器
        get(): # 获取日志器
        has():  
    transports: # 传输器
        Console: # 控制台
        DailyRotateFile:
        File: # 文件
            filename:
        Http:
        Stream:
    Logger: # 日志器
        info():
    Transport:
        log():
    createLogger():
        format:
        level:
        transports:
    info():
    log():
```


### Transport






### 格式化

format


### 日志分割

