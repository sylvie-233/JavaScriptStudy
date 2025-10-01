# MinIO


## 基础介绍

MinIO Node.js SDK

## 核心内容
```yaml
minio:
    Client: # minio客户端
        endPoint:
        port:
        useSSL:
        accessKey:
        secretKey:
        ---
        bucketExists():
        fGetObject():
        fPutObject():
        listBuckets():
        listObjectsV2():
        presignedGetObject():
        presignedPutObject():
        removeObject():
        setBucketPolicy():
    SseS3: # 加密
```


### Tag

标签


### Stat

对象信息

### Presigned

预签名：一个短期有效的 URL，让别人临时访问或上传对象
URL 内包含了 签名信息，服务器验证签名合法性后允许访问



### Policy
```yaml
Policy:
    Version: # 策略语法版本，固定 2012-10-17
    Statement:
        Effect: # 允许或拒绝权限
        Action: # 权限列表
            s3:DeleteObject:
            s3:GetObject:
            s3:GetBucketLocation:
            s3:ListAllMyBuckets:
            s3:PutObject:
            s3:ListBucket:
        Principal: # 指定该策略适用于哪些用户 {"AWS": ["*"]}表示匿名/所有用户
        Resource: # ARN 列表，指定策略作用的桶或对象，arn:aws:s3:::xxx
        Condition: # 限制策略生效条件，例如 IP、时间等
            IpAddress:
                aws:SourceIp:
```

策略

公共访问策略
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": ["s3:GetObject"],
            "Effect": "Allow",
            "Principal": {"AWS": ["*"]},
            "Resource": ["arn:aws:s3:::uploads/*"]
        }
    ]
}
```

Resource资源格式：
```
arn:aws:s3:::bucket_name        # 指桶本身
arn:aws:s3:::bucket_name/*      # 指桶下所有对象
arn:aws:s3:::bucket_name/prefix/* # 指桶下特定目录
```

### Encryption

加密：存储加密


### Notification

通知，事件监听（与redis、消息队列绑定）