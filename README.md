# 弓：无限与经验修补共存

一个面向 Minecraft Java 版 26.1.2 的轻量级 Fabric 模组，允许弓同时拥有“无限”和“经验修补”附魔。

## 安装

1. 安装 Minecraft 26.1.2 与 Fabric Loader 0.19.1 或更高版本。
2. 将 `bow-infinity-mending-26.1.2-1.0.0.jar` 放入该游戏实例的 `mods` 文件夹。
3. 启动游戏后，即可在铁砧中为同一把弓合并“无限”和“经验修补”。

本模组不需要 Fabric API，客户端与服务端均可安装。单人游戏只需安装在客户端；多人服务器需要安装在服务端，客户端可以不安装。

## 构建

需要 Java 25。

Windows：

```powershell
.\gradlew.bat build
```

Linux/macOS：

```bash
./gradlew build
```

构建产物位于 `build/libs/`。

## 实现原理

Minecraft 26.1.2 使用数据驱动的附魔互斥标签。模组覆盖 `minecraft:exclusive_set/bow`，从其中移除“经验修补”，从而让原版铁砧兼容性检查允许这两种附魔共存。

---

## English

### Bow: Infinity and Mending Compatibility

A lightweight Fabric mod for Minecraft Java Edition 26.1.2 that allows bows to have both Infinity and Mending at the same time.

### Installation

1. Install Minecraft 26.1.2 and Fabric Loader 0.19.1 or newer.
2. Place `bow-infinity-mending-26.1.2-1.0.0.jar` in the `mods` folder of your game instance.
3. Start the game. You can now combine Infinity and Mending on the same bow using an anvil.

This mod does not require Fabric API. It can be installed on both the client and server. For single-player, install it on the client. For multiplayer, it only needs to be installed on the server; clients are not required to install it.

### Building

Java 25 is required.

Windows:

```powershell
.\gradlew.bat build
```

Linux/macOS:

```bash
./gradlew build
```

The generated JAR is located in `build/libs/`.

### How It Works

Minecraft 26.1.2 uses data-driven tags to define mutually exclusive enchantments. This mod overrides `minecraft:exclusive_set/bow` and removes Mending from the tag, allowing the vanilla anvil compatibility check to accept Infinity and Mending on the same bow.

## License / 许可证

This project is licensed under the [MIT License](LICENSE).

本项目使用 [MIT License](LICENSE)。
