---
title: "当前支持的 Unity 版本"
---

# 当前支持的 Unity 版本

VRChat 当前推荐使用的 Unity 版本是 [**2022.3.22f1**](https://unity.com/releases/editor/whats-new/2022.3.22)。

如果您安装了 Unity Hub，您可以点击[这个链接](unityhub://2022.3.22f1)来安装正确版本的 Unity。您也可在 [Unity 编辑器版本存档](https://unity.com/releases/editor/archive)中找到 2022.3.22f1。

如果您想为 Android 或 Quest 平台创作世界和虚拟形象，可在安装界面选择“Android Build Support”。

**为了使用最新版的 VRChat SDK，必须升级至 Unity 2022。**如果您目前还停留在 Unity 2019，我们强烈推荐您进行升级。否则，您可能无法接收到未来的 SDK 更新，而且一些旧的内容可能会遇到问题。

有关如何从 Unity 2019 升级至 Unity 2022 的详细指南，请[查阅我们的文档](/creators.vrchat.com/sdk/upgrade/unity-2022)。

## 与先前版本的差异

Unity 2022 包含很多改进，例如更快的迭代时间、优化的资产导入时间、快*很多*的平台切换时间、更好的编辑器稳定性、完全的 C# 8 支持、一个快速搜索功能、[还有更多！](https://unity.com/releases/lts)

## 已知问题

* 当您第一次打开场景，并选择预制体中具有 U# 行为的 GameObject 时，该 U# 行为下方的组件的 GUI 将不会显示。取消选择并重新选择该预制件可以解决这个问题。
* Buffer Particles 不能像在 Unity 2019 里那样工作，[社区成员 hfcRed 在这里给出了一个解决方法](https://x.com/hfcRedddd/status/1696915379090604179)。
* Unity 2022 有时会导致 Rider 的调试器因 Unity 的 IMGUI 中未处理的异常而停止。
    * 若要了解更多，请参见 [这个解决方法](https://forum.unity.com/threads/rider-debugger-breaks-on-unhandled-exception.1135879/#post-7305256)与 [JetBrains 的错误跟踪器](https://youtrack.jetbrains.com/issue/RIDER-64944)。
* 空间化音频源在进入播放模式或调整其设置时会发出警告。