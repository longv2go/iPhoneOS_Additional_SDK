iPhoneOS Additional SDK
------

苹果在 opensource.apple.com 上开源了很多底层库，但是这些库基本都不能直接编译，都缺少很多头文件。Additional SDK 就是为了解决这个问题而出现的。

# 安装

```
➜  images git:(master) ✗ xcrun --show-sdk-path --sdk iphoneos
/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS11.0.sdk
```

上面的命令打印出 iphoneos sdk 的默认路径，把 iPhoneOSxx.x.additional.sdk 拷贝到同级目录。

# 使用

安装的所有 sdk 可以使用 xcodebuild 打印出来，如下
```
git:(master) ✗ xcodebuild -showsdks
iOS SDKs:
  iOS additional 11.0             -sdk iphoneos.additional11.0
  iOS 11.0                        -sdk iphoneos11.0

iOS Simulator SDKs:
  Simulator - iOS 11.0            -sdk iphonesimulator11.0

macOS SDKs:

......

```

关闭已经打开的 Xcode，然后在任意打开一个工程，切换到 Build Setting 面板，在 Additional SDKs 条目中添加新的 sdk，参数就是上面的命令中 ’-sdk‘ 后面的字符串，如下图

![img](https://github.com/longv2go/iPhoneOS_Additional_SDK/raw/master/images/basesdk.png)






