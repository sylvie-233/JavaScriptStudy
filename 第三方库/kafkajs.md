# kafkajs

## 基础介绍

javascript 操作kafka库

## 核心内容
```yaml
kafkajs:
    Kafka:
        clientId:
        brokers:
        admin(): # 管理端
            connect():
            createTopics():
            deleteTopics():
            describeCluster():
            listTopics():
        consumer(): # 消费者
            connect():
            disconnect():
            run(): # 消费消息
                eachMessage():
            subscribe(): # 订阅
                fromBeginning:
                topic:
        producer(): # 生产者
            transactionId: # 事务id
            --- 
            connect():
            disconnect():
            send():
                message:
                    headers:
                    value:
                topic:
            transaction(): # 开启事务
                abort(): # 事务回滚
                commit(): # 提交事务
                send():
```