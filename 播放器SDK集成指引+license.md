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

若您已获得相关License授权，需在[腾讯云视立方控制台](https://console.cloud.tencent.com/vcube) 获取License URL和License Key；

<img width="1317" alt="image" src="https://user-images.githubusercontent.com/88317062/169646279-929248e3-8ded-4b9e-8b04-2b6e462054a0.png">

若您暂未获得License授权，需先参考[视频播放License]()获取相关授权。

【Android端】

获取到License信息后，在调用 SDK 的相关接口前，通过下面的接口初始化License，建议在 Application类中进行如下设置：

```java
public class MApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();
        String licenceURL = ""; // 获取到的 licence url
        String licenceKey = ""; // 获取到的 licence key
        TXLiveBase.getInstance().setLicence(this, licenceURL, licenceKey);
        TXLiveBase.setListener(new TXLiveBaseListener() {
            @Override
            public void onLicenceLoaded(int result, String reason) {
                Log.i(TAG, "onLicenceLoaded: result:" + result + ", reason:" + reason);
            }
        });
    }
}
```

【iOS端】

获取到License信息后，在调用 SDK 的相关接口前，通过下面的接口初始化License，建议在 `- [AppDelegate application:didFinishLaunchingWithOptions:]` 中进行如下设置：

```objective-c
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    NSString * const licenceURL = @"<获取到的licenseUrl>";
    NSString * const licenceKey = @"<获取到的key>";
        
    //TXLiveBase 位于 "TXLiveBase.h" 头文件中
    [TXLiveBase setLicenceURL:licenceURL key:licenceKey]; 
    NSLog(@"SDK Version = %@", [TXLiveBase getSDKVersionStr]);
}
```


【Flutter端】

申请到license后，在调用 SDK 的相关接口前，通过下面的接口初始化license，建议在应用启动的时候进行:
```dart
String licenceURL = ""; // 获取到的 licence url
String licenceKey = ""; // 获取到的 licence key
SuperPlayerPlugin.setGlobalLicense(licenceURL, licenceKey);
```
------新增内容------

### (原）步骤2：添加 View

SDK 默认提供TXCloudVideoView 用于视频渲染，我们第一步要做的就是在布局 xml 文件里加入如下一段代码

