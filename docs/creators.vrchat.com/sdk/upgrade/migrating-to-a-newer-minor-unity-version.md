---
title: "Unity 次要版本升级"
---

# Unity 次要版本升级

有时，VRChat 会在 Unity 的几个次要版本内更新。比如说，VRChat 可能会从 Unity 2022.1.**1** 更新到 Unity 2022.1.**2**。

## 安装新的 Unity 版本

1. 关闭所有正打开的 Unity 项目。

2. 检查[当前支持的 Unity 版本](/creators.vrchat.com/sdk/upgrade/current-unity-version)并通过 Unity Hub 安装新版本的 Unity。
	- 尽管我们在那个页面列出了独立安装器，但是我们强烈建议使用 Unity Hub。对于这个文档，我们假设您正在使用它。

## 复制您的项目

1. 复制或备份您的项目
    - 如果您正在使用 [VRChat 创作者助手](https://creators.vrchat.com/)，它会在迁移版本前自动建议您复制项目。您可以通过“备份（Make Backup）”按钮来创建项目的备份。
    - 或者，复制整个项目文件夹并重命名为一个新名称。
	- 将整个项目导出为一个 Unity 包，但是这种方式耗时很久且可能会产生错误。

:::danger 千万不要跳过这一步！
升级可能会失败。如果您保持原始项目文件安全，你可以恢复它们，再次尝试，并找出问题所在。

没有备份，您就没有第二次尝试的机会。如果您犯了错误或者升级发生失败，修复项目可能会很难，甚至是不可能的。
:::

如果您是一个高级用户，并且知道如何使用例如 [Git](https://git-scm.com/) 的版本控制工具，您应该使用它。

## 打开您的项目

1. 在新版本中打开您项目的副本。
    - 您将会收到一些升级警告。这是正常的！请点击肯定的按钮。

2. 一段时间之后，迁移就会结束。就是这样！

## 可选的信息和提示

次要版本升级并不是总需要 SDK 更新。如果是的话，这就是您做这件事的时候。

1. 在升级后关闭您的项目。
2. 使用[创作者助手](https://vcc.docs.vrchat.com/)来升级您的 SDK。

#### Unity 警告

这里有一些可能会在迁移过程中弹出的 Unity 警告，您可以安全的略过它们。这些是您可能会看到的：

![migrating-to-a-newer-minor-unity-version-f3995eb-image_10.png](/creators.vrchat.com/images/sdk/migrating-to-a-newer-minor-unity-version-f3995eb-image_10.png)

![migrating-to-a-newer-minor-unity-version-b20553b-image_11.png](/creators.vrchat.com/images/sdk/migrating-to-a-newer-minor-unity-version-b20553b-image_11.png)

#### 清理副本

如果您的项目很大，迁移可能会花费很长时间。当您的项目特别庞大时，这些文件夹是您不需要迁移的。您可以安全的从副本中删除其中任一文件夹。

```text
/Library/
/Temp/
/Obj/
/Build/
/Builds/
/Logs/
/UserSettings/
```
#### 版本警告

即使您*知道*自己使用的是正确的版本，SDK 也可能会警告您使用的版本错误。

![migrating-to-a-newer-minor-unity-version-1b8194d-2022-11-30_10-35-54_chrome.png](/creators.vrchat.com/images/sdk/migrating-to-a-newer-minor-unity-version-1b8194d-2022-11-30_10-35-54_chrome.png)

这是正常的！如果您知道实际上使用了正确的版本，您可以忽略这一消息。