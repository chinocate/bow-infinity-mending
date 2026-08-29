# 弓：无限与经验修补共存

一个面向 Minecraft Java 版 26.1.2 的轻量 Fabric 模组，允许弓同时拥有“无限”和“经验修补”附魔。

## 安装

1. 安装 Minecraft 26.1.2 与 Fabric Loader 0.19.1 或更高版本。
2. 将 `bow-infinity-mending-26.1.2-1.0.0.jar` 放入该游戏实例的 `mods` 文件夹。
3. 启动游戏后，可在铁砧中为同一把弓合并“无限”和“经验修补”。

本模组不需要 Fabric API，客户端与服务端均可安装。单人游戏只需安装在客户端；多人服务器需要安装在服务端，客户端可不安装。

## 构建

需要 Java 25：

```powershell
.\gradlew.bat build
```

构建产物位于 `build/libs/`。

## 实现原理

Minecraft 26.1.2 使用数据驱动的附魔互斥标签。模组覆盖 `minecraft:exclusive_set/bow`，从其中移除“经验修补”，从而让原版铁砧兼容性检查允许这两种附魔共存。
