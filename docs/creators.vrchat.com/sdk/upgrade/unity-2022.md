---
title: 将项目升级到 2022
---

# 将项目升级到 2022

这个界面介绍了如何将您的 VRChat 项目从 2019.4.31f1 版本升级到 Unity 2022.3.22f1。
最新版本的 VRChat SDK 必须安装 Unity 2022 才能使用。您可以 [在这里查看升级带来的好处](/creators.vrchat.com/sdk/upgrade/current-unity-version)。

如果您在使用创作者助手，升级项目简直是小菜一碟！但是首先，最好确定您为项目都创建了备份。

## 备份您的 Unity 项目

如果您在使用 [VRChat 创作者助手](https://creators.vrchat.com/)，它会在迁移版本前自动建议您备份项目。

1. 为了备份您的项目，首先点击 管理项目（Manage Project）按钮旁边的三点菜单，然后选择“创建备份（Create Backup）”选项。这是备份项目的推荐方法，尤其推荐新创作者使用这一方法！
	- 需要注意的是，“创建备份（Create Backup）”并不会备份 `Udon`、`UdonSharp` 或 `VRChat Examples` 文件夹。如果您对这些文件夹做出了修改，请选择其他的备份方式。
	- 您也可以通过复制整个项目文件夹并重命名为一个新名称（比如 `MyProject-Backup`）来备份项目。
	- 您*可以*将整个项目导出为一个 Unity 包，但是这种方式耗时很久且可能会产生错误。我们不推荐这种方式。

![创建备份](/creators.vrchat.com/images/sdk/migrate-2019-2022/creating_backup.png)

:::danger 千万不要跳过这一步！
在向您珍贵的项目进行重大修改前进行备份绝对是一个好主意。

升级可能会失败。如果升级失败，您的备份可以被用作一个检查点。如果您保持原始项目文件安全，你可以恢复它们，再次尝试，并找出问题所在。

**没有备份，您就没有第二次尝试的机会。** 如果您犯了错误或者升级发生失败，修复项目可能会很难，甚至是**不可能**的。
:::

1. 在 Unity 2019 中打开您的项目，检查 [Unity 控制台](https://docs.unity3d.com/Manual/Console.html)或 [VRChat SDK Build 面板](/creators.vrchat.com/worlds/creating-your-first-world#step-4-configure-your-world-in-the-sdk-build-panel)中是否有任何报错或警告。
    - 如果您没有修复 Unity 2019 项目中的问题，它们可能会在 Unity 2022 中产生问题。
    - *一些*警告可以被安全的忽略，但是您最好试着搞清楚它们为什么会出现。

现在您已经准备好升级了！

:::danger 在上传之前测试您的内容

在成功用 Unity 2022 上传世界或虚拟形象之后，您就无法再用 Unity 2019 上传它们了。

:::

## 使用创作者助手 

您可以通过两种方法在创作者助手中升级项目：直接在 项目（Projects）页面中升级，或是在项目各自的 管理项目（Manage Project）页面中升级。**在继续操作前，确保您试图升级的项目当前没有打开。**

1. 进入设置（Settings），然后点击 更新（Updates）来检查创作者助手是否需要更新。若不更新，升级到 Unity 2022 的提示就不会显示。

![检查创作者助手更新](/creators.vrchat.com/images/sdk/migrate-2019-2022/updating_vcc.png)

2. 在 项目（Projects）页面，您可能会在每个项目中看到一个新的 **Unity** 列，其中包括一个版本切换器。点击它，然后点击 迁移到 Unity 2022（Migrate to Unity 2022）。

![点击正确的项目](/creators.vrchat.com/images/sdk/migrate-2019-2022/updating_vcc_via_projects.png)

或者，在任意项目上点击 **管理项目（Manage Project）**，然后您就会看到一个 升级到 2022（Upgrade to 2022）的横幅。

![通过 管理项目（Manage Project）升级](/creators.vrchat.com/images/sdk/migrate-2019-2022/manage_project_upgrade.png)

## 使用 Unity Hub

Unity Hub 是一款独立的应用程序，可让您同时无缝安装和使用多个 Unity 版本。若您不愿使用创作者助手，您也可以使用它来安装 Unity 2022。

1. 安装 [Unity Hub](https://unity.com/download)。
    - 您可以跟随 Unity 的官方[安装教程](https://learn.unity.com/tutorial/install-the-unity-hub-and-editor)。
    - 您需要在安装 Unity Hub 后创建一个 [Unity 账户](https://id.unity.com/account/new)。
2. 访问 [Unity 下载存档](https://unity.com/releases/editor/archive)。
3. 点击 **Unity 2022.x**。
4. 向下滚动直到看到 Unity 2022.3.22，然后点击蓝色的 **Unity Hub** 按钮。
   - 不要选择列表中的第一个 Unity 版本！
   - 您也可以到[当前支持的 Unity 版本页面](/creators.vrchat.com/sdk/upgrade/current-unity-version)找到下载正确版本 Unity 的链接。

![在 Unity 下载存档中选择正确的版本并安装](/creators.vrchat.com/images/sdk/migrate-2019-2022/unity_webpage_search.png)

![同意浏览器弹窗以打开 Unity Hub](/creators.vrchat.com/images/sdk/migrate-2019-2022/browser-prompt-unity-hub.png)

5. 在您的浏览器中点击 **Open Unity Hub**。

![如果你想为 Android 设备开发内容，需要打开 Android 构建支持（Android Build Support）](/creators.vrchat.com/images/sdk/migrate-2019-2022/unity_version_hub_upgrade_android.png)

6. 在 Unity 安装界面中选择 **Android 构建支持（Android Build Support）**。
	- 如果您并未计划在 Android 或 Quest 平台上传内容，可以跳过此步。
	- 安装之后，您可通过在 Unity Hub 中选择 [添加模块（Add modules）](https://docs.unity3d.com/hub/manual/AddModules.html) 来完成这一步骤。
7. 点击 **继续（Continue）** 来安装 Unity 2022.3.22。

## 管理多个 Unity 版本

您可轻松查看电脑上可与创作者助手配合使用的 Unity 版本。您还可以更改用于打开所有*新*项目的 Unity 版本。

1. 在创作者助手中，进入**设置（Settings）**。
2. 在 **Unity 编辑器**下，使用下拉菜单来更改默认的 Unity 编辑器。这*不会*影响已经创建的任何项目。
3. 如果您还没有安装 Unity 2022.3.22，[跟随上面的操作进行](unity-2022.md#使用创作者助手)。
4. 如果您没有看到已经安装的 Unity 版本，可以试试使用刷新按钮或直接使用文件按钮查找路径。

## 包

如果您试着为 2022 项目添加包，时刻记住：

- 每一个精选包都有能在 2022 版本工作的版本。
- 其他包*可能*可以工作，但是有一些包可能需要作者发布新的版本！
- 使用过期的包可能会产生很多问题，因此请确保您导入的任何内容都与 Unity 2022 兼容。

# 疑难解答

- 在上传之前测试您的世界。查看 Unity 的控制台中是否有报错，并在 VRChat 中测试您的世界是否正常工作。
    - 在成功使用 Unity 2022 上传世界后，您将无法再使用 Unity 2019 上传这个世界。
- 在使用 VRChat 的 SDK 前，[确保您激活了您的 Unity 个人版许可（Unity Personal license）](https://support.unity.com/hc/en-us/articles/211438683-How-do-I-activate-my-license-)。Unity 免费供个人使用。
- 若要进一步了解 Unity Hub，请访问 [Unity 文档](https://docs.unity3d.com/hub/manual/index.html)。
- 如果您遇到与 SDK 本身有关的问题，请阅读我们的 [SDK 疑难解答](/creators.vrchat.com/sdk/sdk-troubleshooting) 页面。