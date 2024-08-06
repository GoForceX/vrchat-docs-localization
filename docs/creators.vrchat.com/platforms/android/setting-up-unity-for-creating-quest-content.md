# 设置 Unity 以创建 Quest 内容

![Building for Mobile instructions](/creators.vrchat.com/images/setting-up-unity-for-creating-quest-content-1ac8b19-VRChat_QuestContent_QuickStart.png)

If you're starting a brand new project, this won't take long at all. However, if you're converting a Windows platform project to an Android platform project, you will have to convert your assets appropriately. This can take quite a while for larger projects.

For more details on best practices when working with dual-platform projects, read our documentation on [Cross-Platform Setup](/creators.vrchat.com/platforms/android/cross-platform-setup).

## 3 Steps to get your world on VRChat for Quest

### 1. Open Your Build Settings

You can access your [Build Settings](https://docs.unity3d.com/Manual/BuildSettings.html) from Unity's main menu by going to "File" -> "Build Settings". Or you can use the keyboard shortcut `Ctrl` + `Shift` + `B`.

### 2. Switch Platform to Android

::: warning 需要额外的设置
If the Android option isn't appearing, [you need to install Unity's Android SDK.](https://docs.unity3d.com/Manual/android-sdksetup.html)
:::

Click "Android" -> "Switch Platform". Unity will reimport your assets for Android. This will take a while for larger projects with many assets.

### 3. Publish -> New Build

That's it! Your content is now available on Quest! Note that you must **upload** your content to test it. You can't use the SDK's "Build and Test" feature for Android content.