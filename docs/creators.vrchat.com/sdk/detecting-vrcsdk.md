---
title: "检测 VRChat SDK"
---

# 检测 VRChat SDK

有很多方法可以在 Unity 项目中检测 VRChat SDK。在开发不依赖 VRChat SDK 的 Unity 工具或库，但仍想利用 [VRChat 的 SDK API](/creators.vrchat.com/sdk/public-sdk-api) 时，这会很有帮助。

## 使用版本定义（Version Defines）（建议） {#using-version-defines}

检测 VRChat SDK 的最好方式就是通过[程序集定义文件中的版本定义（Version Defines）][version-defines]。

当 `com.vrchat.base`、`com.vrchat.avatars` 或 `com.vrchat.worlds` 已安装时，您可以在程序集中定义符号。
在安装的 VRChat SDK 版本与您的工具兼容时，建议仅使用“Expression”属性来定义您的符号。
对于 VRChat SDK 的版本控制，请参考[创作者助手文档][versioning]。

由于版本定义是 UPM 包的一个功能，因此这种方式仅适用于基于 VPM 的 SDK，这些 SDK 被 Unity 视为 UPM 包。
如果你也想检测旧版的基于 `.unitypackage` 的 SDK，请使用下面的旧版方法定义与 VRCSDK 相同的符号，或者在每个文件中添加以下代码：

```csharp
#if !YOUR_VRCSDK3_AVATARS && !YOUR_VRCSDK3_WORLDS && VRC_SDK_VRCSDK3
    #if UDON
        #define YOUR_VRCSDK3_WORLDS
    #else
        #define YOUR_VRCSDK3_AVATARS
    #endif
#endif
```

[version-defines]: https://docs.unity3d.com/2019.4/Documentation/Manual/ScriptCompilationAssemblyDefinitionFiles.html#define-symbols
[versioning]: https://vcc.docs.vrchat.com/vpm/packages/#brandingbreakingbumps

## 使用旧版 VRCSDK 定义的脚本符号（已弃用） {#using-scripting-symbols}

检测 VRChat SDK 安装的另一种方法使用 VRCSDK 定义的脚本符号。
对于所有 VRCSDK 项目，`VRC_SDK_VRCSDK3` 都将被定义，对于世界项目，`UDON` 将被定义。

这种方式已被弃用，并将会被移除。不要仅仅依赖这种方式。

老版 VRChat SDK 内部使用了 `VRC_SDK_VRCSDK3` 和 `UDON` 符号。但因为这些符号在整个项目中都处于活跃状态，很多工具都依赖这些符号来检测 VRChat SDK。

现在，VRChat SDK 中所有这些符号的使用都已迁移到版本定义。请尽快迁移到版本定义！