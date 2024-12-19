# PM2

## 基础介绍

nodejs 进程管理器

进程管理、日志管理



### pm2
```yaml
pm2:
    delete: # 关闭进程
    ecosystem: # 生成配置文件
    flush: # 清除日志
    logs: # 查看日志
        --lines:
    monit:
    restart:
    save:
    scale:
    show:
    start:
        --cron-restart:
        --env:
        --max-memory-restart:
        --watch: # 监听文件重启
    startup:
    stop: # 关闭进程
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
```


pm2 启动配置文件




## 核心内容
