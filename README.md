# Bili2233

一个独立的 **LSPosed** 模块：在哔哩哔哩 Android 客户端里自动跳过**赞助广告、片头、自我推广、互动提醒**
等片段，并在进度条上把它们标出来。片段数据来自社区众包的 SponsorBlock 接口。

模块**只修改本机客户端的播放行为**（跳过 / 静音 / 绘制进度条标记），
不登录、不接管账号、不修改任何服务端请求，也不破解会员或去除广告投放。

## 功能

- **自动跳过** —— 进入片段时自动跳到末尾，可选「N 秒后跳过 + 取消」
- **手动跳过** —— 片段内显示跳过按钮，点按才跳
- **片段静音** —— 对 mute 类片段静音而非跳过
- **最小片段时长过滤** —— 太短的片段不跳，避免进度条抖动
- **进度条彩色标记** —— 9 个分类各自着色，颜色可自定义
- **剩余时长扣减** **跳过 Toast** **跳过次数统计**
- **片段提交** —— 在播放器面板里标记并提交片段

## 环境要求

| 项 | 要求 |
| --- | --- |
| Root | KernelSU / Magisk |
| 框架 | LSPosed（需支持 libxposed API 101） |
| Android | 6.0+ |
| 宿主客户端 | **哔哩哔哩国际版 `com.bilibili.app.in` 6.5.0 / versionCode 9110200** |

> 只适配了 6.5.0 这一个宿主版本，其他版本大概率静默失效。

## 安装

1. 安装本页 Release 里的 APK。
2. LSPosed → 模块 → 启用 **Bili2233** → **作用域只勾 `com.bilibili.app.in`**。
3. **强制停止哔哩哔哩**再重新打开。

装好后无需任何操作即生效。播放页右上角「⋯」→ 更多面板里的「空降助手」可打开控制面板；
设置页在模块 App 图标或「我的」页的 `Bili2233` 入口，两处是同一套 UI。

## 链接

- 源码 / 完整说明：https://github.com/ch6vip/lsposed-bili-sponsorblock
- 问题反馈：https://github.com/ch6vip/lsposed-bili-sponsorblock/issues

## ⚠️ 说明

本项目由 **AI 编写**，作者负责提需求、真机验证和发版，**不保证稳定性与持续维护**。
遇到问题、想加功能、或适配新版本，欢迎提 Issue / PR 一起贡献。

## 致谢

- [小电视空降助手 · hanydd/BilibiliSponsorBlock](https://github.com/hanydd/BilibiliSponsorBlock) —— 默认数据源 `bsbsb.top` 即该项目的服务端
- [SponsorBlock](https://sponsor.ajay.app/) —— 片段数据与 API 协议
- [BiliRoaming](https://github.com/yujincheng08/BiliRoaming) / [BiliRoamingX](https://github.com/BiliRoamingX/BiliRoamingX) —— B 站客户端改动思路
- [LSPosed](https://github.com/LSPosed/LSPosed) 与 [libxposed](https://github.com/libxposed) —— 框架与 API

## 许可

[MIT](https://github.com/ch6vip/lsposed-bili-sponsorblock/blob/master/LICENSE)
