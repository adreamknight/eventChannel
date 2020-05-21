[toc]

# demo_0519_eventchannel

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.



# EventChannel

## native 调 flutter

### swift实现

1. 初始化FlutterViewController，FlutterEventChannel
2. 实现FlutterStreamHandler子类，实现onListen()，onCancel()方法
3. 调用eventChannel.setStreamHandler(XX)，XX是第2步创建的子类

### Dart代码

1. 唤醒监听nativeMessageListener()，放在initState()里面，类似于一种声明
2. 定义监听处理nativeMessageListener()方法，里面调用eventChannel.receiveBroadcastStream().listen(evnet)，根据调过来的event（一般是字典，分别以方法名，参数等作为key）做相应处理。



## 没有flutter 调 native

