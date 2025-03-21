# Flutter

`Flutter官方文档：https://docs.flutter.dev/`
`Flutter移动应用：P11`


## 基础介绍

基于Dart的跨平台GUI框架

依赖JDK、Android SDK(配置ANDROID_HOME)、Flutter SDK、Android模拟器
Flutter SDK中包含了Dart SDK


资源镜像：
- PUB_HOSTED_URL:
- FLUTTER_STORAGE_BASE_URL:


### 项目结构
```yaml
项目结构:
    /.dart_tool:
    /.idea:
    /android:
    /build:
    /ios:
    /lib: # flutter主目录
        main.dart:
    /test:
    .metadata:
    analyasis_options.yaml:
    xxx.iml:
    pubspec.lock:
    pubspec.yaml:
```

#### 安装目录
```yaml
flutter:
    /.pub-cache: # 下载的公共模块
        /bin:
    /bin:
        /cache:
            /dart-sdk:
                /bin:
                    /resources:
                    /snapshots:
                    /utils:
                    dart:
                /include:
                /lib:
                /pkg:
        /internal:
        /mingit:
        dart:
        flutter:
    /dev:
    /docs:
    /engine:
    /examples:
    /packages:
```


#### pubspec.yaml
```yaml
pubspec.yaml:

```




### flutter
```yaml
flutter:
    -h:
    --version:
    channel: # 版本管理
        beta:
    create: # 创建项目
    doctor: # 环境检测
    emulator:
        --launch:
    emulators: # 所有模拟器
        --create:
        --launch:
    run: # 运行项目
        R: # 热重载
        c:
        d:
        h:
        q:
        r:
    upgrade:
```


## 核心内容
```yaml
flutter:
    animation:
    cupertinto:
    foundation:
    gestures:
    material: # 组件库
    painting:
    physics:
    rendering:
    scheduler:
    semantics:
    services:
    widgets: # 控件库
        BuildContext:
        StatefulWidget: # 有状态组件基类
        StatelessWidget: # 无状态组件基类
```


### 组件




