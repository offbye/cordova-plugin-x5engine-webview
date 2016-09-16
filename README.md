# cordova-plugin-x5engine-webview

Makes your Cordova application use the [TBS X5  WebView](http://x5.tencent.com/index)
instead of the System WebView. Requires cordova-android 4.0 or greater.

## 腾讯浏览服务X5SDK
[腾讯浏览服务X5SDK](http://x5.tencent.com/index)是通过调用微信/手机QQ/空间的X5内核，解决系统webview兼容性差、加载速度慢、功能缺陷等问题，开发接入便捷，大小只有253K，仅需几行代码，即可解决一切令开发者们头疼的问题，为用户提供最优秀的浏览体验。

腾讯浏览服务官方只提供了如何把系统Webview替换成X5的接入文档，并没有提供Cordova集成的方法。现在Hybrid App项目经常使用很多Cordoca插件提供拍照，扫二维码，App支付宝支付等功能，因此就需要把cordova和x5结合起来。

Cordova框架现在已经很完善，Cordova的Web Engine也是基于接口开发的，因此我参考系统engine的实现，写了一个x5engine插件，解决了Cordova调用X5内核的问题。

## 问题背景
熟悉Cordova生态圈的朋友可能听说过Crosswalk，[Crosswalk](https://crosswalk-project.org/documentation/cordova.html)是Intel维护的Webkit开源项目，可以通过插件安装命令` cordova plugin add cordova-plugin-crosswalk-webview` 安装，它的缺点就是太大了，集成后apk会增加20M，安装后会占用50M空间，因此一般不推荐普通App使用Crosswalk。

### Benefits
* 同时享受Cordova平台完善的生态系统和腾讯X5内核的兼容性和稳定性，大量的Cordova插件仍然可用， Apk size只增加250k。
* 微信/手机QQ/空间装机量很大，足够覆盖大多数国内用户
* 使用X5内核的播放器增强H5视频播放能力


### Drawbacks

* Increased APK size (about 250Kb)

### Install

The following directions are for cordova-cli (most people).  

* Open an existing cordova project, with cordova-android 4.0.0+, and using the latest CLI. TBS X5  variables can be configured as an option when installing the plugin
* Add this plugin

```
$ cordova plugin add  https://github.com/offbye/cordova-plugin-x5engine-webview.git
```

* Build
```
$ cordova build android
```

### Configure
