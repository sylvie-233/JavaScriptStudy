# PM2

## 基础介绍

nodejs 后台进程管理器

进程管理、日志管理



### pm2
```yaml
pm2:
    delete: # 关闭进程
    describe:
    ecosystem: # 生成配置文件 ecosystem.config.js
    flush: # 清除日志
    jlist:
    list:
    logs: # 查看日志
        --lines: # 指定日志行数
    monit: # 实时监控面板
    plus:
    prettylist:
    reload:
    reloadLogs:
    restart:
    save:
    scale: # LB 运行
    sendSignal: # 给应用发送系统信号
    show:
    start:
        -i:
        --cron-restart:
        --env:
        --log:
        --max-memory-restart:
        --name: # 指定appname
        --port:
        --watch: # 监听文件重启
    startup:
    status:
    stop: # 关闭进程
        all:
    update:
```


#### pm2.yml
```yaml
apps:
    env_production:
    name:
    script:
```


#### ecosystem.config.js
```yaml
ecosystem:
    apps:
        env:
        env_production:
        name:
        script:
```


pm2 启动配置文件




## 核心内容
