# dio


## 基础介绍

Http请求库
支持：
- 全局请求配置：
- 拦截器链：
- 重试请求：
- 取消请求：


## 核心内容
```yaml
dio/dio.dart:
    BaseOptions:
    CancelToken: # 取消请求
        cancel():
    Dio: # http客户端
        interceptors: # 拦截器配置
        options: # 客户端配置
            baseUrl:
            connectTimeout:
            receiveTimeout:
        download():
            onReceiveProgress:
        get():
        post():
            data:
            options:
            queryParameters:
    DioException: # dio异常
        message:
        response:
        type:
    DioExceptionType: # dio异常类型
        badResponse:
        cancel:
        connectionTimeout:
        receiveTimeout:
    InterceptorsWrapper: # 拦截器包装器
        onError:
        onRequest:
        onResponse:
    LogInterceptor:
    Response: # 响应结果
        data:
        statusCode:
```
