# bpmn-engine


## 基础介绍



## 核心内容
```yaml
bpmn-engine:
    Engine:
        name:
        source: # 流程定义文件
        execute(): 
            execution: # 流程实例
                getState():
                on():
                    start:
                    wait: # 监听用户任务
                    end:
                    ---
                    activity: # 活动任务 
                        id: # 活动任务id（区分任务）
                        signal(): # 变量传递，触发流程执行
                once():
                restore():
                resume():
                stop():
        getDefinition():
```