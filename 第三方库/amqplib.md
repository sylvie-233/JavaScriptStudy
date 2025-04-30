# amqplib

## 基础介绍

javascript 消息队列操作库


## 核心内容
```yaml
amqplib:
    Channel: # 通道
        ack():
        consume(): # 接收消息、监听队列
        assertExchange(): # 绑定交换机
        assertQueue():  # 绑定队列
        bindQueue(): # 绑定交换机和队列
        publish(): # 发送消息到交换机
        sendToQueue(): # 发送消息到队列 
    Connection:
        createChannel():
    connect():
```

### Connection



### Channel


### Queue