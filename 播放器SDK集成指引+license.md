需要增加视频播放license 申请和接入的文档地址：

[点播场景](https://cloud.tencent.com/document/product/881/67112) *>* 接入文档： https://cloud.tencent.com/document/product/881/20216

​							          https://cloud.tencent.com/document/product/881/20211

[直播场景](https://cloud.tencent.com/document/product/881/67110) *>* 接入文档： https://cloud.tencent.com/document/product/881/20217

​                                         https://cloud.tencent.com/document/product/881/67108

 [Android 端集成](https://cloud.tencent.com/document/product/881/20200) *>* 超级播放器： https://cloud.tencent.com/document/product/881/20213

 [iOS 端集成](https://cloud.tencent.com/document/product/881/20199) *>* 超级播放器：https://cloud.tencent.com/document/product/881/20208





## SDK集成

### 步骤1：下载 SDK 开发包

[下载](https://vcube.cloud.tencent.com/home.html) SDK 开发包，并按照 [SDK 集成指引](https://cloud.tencent.com/document/product/1449/56987) 将 SDK 嵌入您的 App 工程中。

------新增内容------


### 步骤2：配置License授权

若您已获得“视频播放”功能模块的License授权，需在[腾讯云视立方控制台](https://console.cloud.tencent.com/vcube) 获取License URL和License Key，

<img width="1317" alt="image" src="https://user-images.githubusercontent.com/88317062/169646279-929248e3-8ded-4b9e-8b04-2b6e462054a0.png">

若您暂未获得License授权，需先参考[视频播放授权]()获取相关授权。

【Android端】

获取到License信息后，通过下面的接口初始化License，建议在Application启动的时候进行：

```java
String licenceUrl = "填入您的 License Key";
String licenseKey = "填入您的 License Key"
TXLiveBase.getInstance().setLicence(context, licenceUrl, licenseKey);
```

### 

【iOS端】

获取到License信息后，通过下面的接口初始化License，建议在Application启动的时候进行：

```objective-c
NSString *licenceURL = "填入您购买的 填入您的 License Key";
NSString *licenseKey = "填入您购买的 填入您的 License Key"
[TXLiveBase setLicenceURL:licenceURL key:licenseKey];
```


【Flutter端】

申请到license后，通过下面的接口初始化license，建议在启动的时候进行:
```dart
String licenceUrl = "填入您购买的 license 的 url";
String licenseKey = "填入您购买的 license 的 key";
SuperPlayerPlugin.setGlobalLicense(licenceUrl, licenceKey);
```
------新增内容------

### (原）步骤2：添加 View

SDK 默认提供TXCloudVideoView 用于视频渲染，我们第一步要做的就是在布局 xml 文件里加入如下一段代码

