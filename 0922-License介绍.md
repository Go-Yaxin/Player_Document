## License 概述

音视频终端 SDK（腾讯云视立方）通过购买 License / 套餐 获得 SDK 使用授权；
计费详情参见 [SDK授权费用]()，购买方式请参见 [购买流程]()，您可以在 [腾讯云视立方控制台](https://console.cloud.tencent.com/vcube) 对各 License 进行 [新增和续期](https://cloud.tencent.com/document/product/1449/56981) 等操作。

License 通过与应用包名绑定实现对应应用的 SDK 使用授权，如一个直播 License 与应用 A 绑定后，应用 A 即可使用直播 SDK 的所有功能。

您在控制台完成 License 与应用包名的绑定后，将生成一组 License URL 和 Key，您需要在 SDK 集成过程中将其配置在您的应用中，SDK 将通过 License URL 和 Key 来获取并校验当前应用的授权情况。
一个腾讯云账号下默认生成唯一一组 License URL 和 Key，不区分 License 类型和数量，License URL 和 Key 唯一且不会变更。


更多 License 问题可参见 [License常见问题]()。



## 测试版 License

您可以登录 [腾讯云视立方控制台](https://console.cloud.tencent.com/vcube) 在线申请不同 SDK 的测试版 License，每个 License 均可申请1次，申请指引参见 [申请测试License]()，详情如下表：

| SDK 类型      | 测试版 License       | 授权体验套餐         | 规则                                                         | 申请 License                                                 |
| ------------- | :------------------- | :------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| 直播 SDK      | 直播 License         | -                    | 试用期为14天，可免费续期一次，合计28天                       | [申请测试版 License](https://cloud.tencent.com/document/product/1449/56981) |
| 短视频 SDK    | 短视频 License       | 基础版               | 试用期为14天，可免费续期一次，合计28天                       |                                                              |
| 播放器 SDK    | 视频播放 License     | -                    | 试用期为14天，可免费续期一次，合计28天                       |                                                              |
|               | 终端极速高清 License | -                    | 试用期为90天，如需更新有效期，请联系商务或 [提交工单](https://console.cloud.tencent.com/workorder/category) |                                                              |
| 腾讯特效  SDK | 腾讯特效 License     | S 系列高级套餐 S1-04 | 试用期为14天，可免费续期一次，合计28天                       | [申请授权测试版license](https://cloud.tencent.com/document/product/1449/56982) |



>?
>
>- 每个功能模块仅可申请一次，长期使用请 [购买](https://buy.cloud.tencent.com/vcube) 正式版 License。
>- 试用期内申请测试续期，则续期到期时间以申请测试时刻为准；若试用期结束后申请测试续期，则续期到期时间以申请测试续期时刻为准。
>- 当申请测试开始时间为 `2022-05-25 11:34:55` ，则14天后到期时间为 `2022-06-09 00:00:00` 。
>- 免费续期一次时，若在试用期14天内申请续期，则到期时间为 `2022-06-23 00:00:00` ；若在试用期14天结束后申请续期，申请续期的时间为 `2022-07-03 22:26:20` ，则续期的到期时间为 `2022-07-18 00:00:00` 。
>- **腾讯特效功能模块在申请之后，需要审核通过才能签发授权**，审核时间通常 1-2 个工作日。腾讯特效测试版授权到期时间以审核通过时刻为准；若试用期结束后申请测试续期，则续期到期时间以申请测试续期时刻为准。详情请参见 [申请腾讯特效测试版 License](https://cloud.tencent.com/document/product/1449/56982#.E7.BB.AD.E6.9C.9F.E6.B5.8B.E8.AF.95.E7.89.88-license.3Ca-id.3D.22renewal_test.22.3E.3C.2Fa.3E)。

## 正式版 License

正式版 License 需购买后方可获得，计费详情可参见 [SDK 授权费用]() ，不同 SDK 所需的正式版 License 如下表，不同 SDK 详情可参见 [音视频终端 SDK 子产品介绍](https://cloud.tencent.com/document/product/1449/72295)。

<img width="709" alt="image" src="https://user-images.githubusercontent.com/88317062/201603934-d06e9283-7c35-4869-9bb0-51b0aed34d05.png">

>?
>
>- **腾讯特效功能模块在申请之后，需要审核通过才能签发授权**，审核时间通常 1个- 2 个工作日。详情请参见 [申请腾讯特效正式版 License](https://cloud.tencent.com/document/product/1449/56982#formal)。

## 新旧 License 区别

旧版 License 仅支持一组 License URL 和 Key 解锁对应一个 SDK 功能（移动直播或短视频），相比腾讯云视立方 License 维护和使用较为繁琐；升级后的新版视立方 License 仅需维护一组 License URL 和 Key ，便可以管理所有腾讯云音视频的终端授权。

原移动直播 License、短视频 License 可在音视频终端 SDK（腾讯云视立方）中继续使用，对应授权解锁音视频终端 SDK（腾讯云视立方）中的*直播与短视频功能模块，**若您使用包含上述功能模块的版本时，处于有效期内的 License 无需再次购买解锁授权**。新旧 License 对应详情如下：*

<table>
<thead>
<tr>
<th colspan="2">腾讯云视立方 License</th>
<th>原 SDK License</th>
</tr>
</thead>
<tbody><tr>
<td colspan="2">直播 License</td>
<td>移动直播基础版 License</td>
</tr>
<tr>
<td rowspan="2">短视频 License</td>
<td>短视频精简版 License</td>
<td>短视频精简版 License</td>
</tr>
<tr>
<td>短视频基础版 License</td>
<td>短视频基础版 License</td>
</tr>
<tr>
<td colspan="2">视频播放 License</td>
<td>-</td>
</tr><tr>
<td colspan="2">终端极速高清 License</td>
<td>-</td>
</tr><tr>
<td colspan="2">腾讯特效 License</td>
<td>-</td>
</tr>
</tbody></table>



>?若您的应用正使用旧版 License 进行校验，可继续使用旧版 License 或改用新版 License（推荐）。未来新购买获赠的 License 进行绑定时将不再提供旧版 License 的 URL 和 Key 。
