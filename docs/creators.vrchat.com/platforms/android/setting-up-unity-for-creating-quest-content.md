# 设置 Unity 以创建 Quest 内容

![针对移动端开发的指南](/creators.vrchat.com/images/setting-up-unity-for-creating-quest-content-1ac8b19-VRChat_QuestContent_QuickStart.png)

如果您正在创建一个全新的项目，这个过程只是小菜一碟。但是，如果您正在将项目从 Windows 平台迁移到 Android 平台，资源的适配工作可就不容小觑了，尤其是对于大型项目来说，这可是一项耗时的工程。

若要深入了解双平台项目的最佳实践，请参阅我们的[跨平台设置](/creators.vrchat.com/platforms/android/cross-platform-setup)文档。

## 三步让您的 VRChat 世界登陆 Quest

### 1. 打开构建（Build）设置

在 Unity 主菜单里，点击 “文件（File）” -> “构建设置（Build Settings）”访问[构建设置（Build Settings）](https://docs.unity3d.com/Manual/BuildSettings.html)，或者用快捷键 Ctrl + Shift + B 一键直达。

### 2. 将平台切换至 Android

::: warning 需要额外的设置
如果 Android 选项并未出现，[您就需要安装 Unity 的 Android SDK。](https://docs.unity3d.com/Manual/android-sdksetup.html)
:::

点击 “Android” -> “切换平台（Switch Platform）”，Unity 就会帮您为 Android 重新导入资源。对于资源较多的大型项目，这个过程可能需要一段时间。

### 3. 发布 -> 新构建

大功告成！您的世界已经可以在 Quest 上访问了！需要注意的是，测试内容时必须将其**上传**。SDK 的 “构建并测试（Build and Test）” 功能无法用于 Android 内容。