[English](README.md) | 中文

# LightlyShaders v3.0

此效果与已有的 Plasma 特效一起正常工作。本 Kubuntu 分支面向 KDE Plasma 6.6.x / KWin 6.6.x，已在 Kubuntu 26.04 上测试。

![default](screenshot.png)

# 依赖关系

需要 KDE Plasma/KWin 6.6.x，以及 Qt 6、KF6、KWin、KDecoration3、X11 和 XCB 开发包。

**Kubuntu 26.04 / Ubuntu 系统**：

```bash
sudo apt update
sudo apt install \
    build-essential cmake extra-cmake-modules gettext git \
    qt6-base-dev qt6-base-private-dev qt6-tools-dev \
    libkf6config-dev libkf6configwidgets-dev libkf6coreaddons-dev \
    libkf6crash-dev libkf6globalaccel-dev libkf6guiaddons-dev \
    libkf6i18n-dev libkf6kcmutils-dev libkf6kio-dev \
    libkf6notifications-dev libkf6service-dev libkf6widgetsaddons-dev \
    libkf6windowsystem-dev kwin-dev libkdecorations3-dev libepoxy-dev \
    libx11-dev libxcb1-dev libxcb-render0-dev libxcb-shape0-dev \
    libxcb-xfixes0-dev libxcb-composite0-dev libxcb-randr0-dev \
    libxcb-shm0-dev libxcb-res0-dev libxcb-sync-dev
```

# 手动安装

```bash
git clone https://github.com/YuKongA/LightlyShaders-kubuntu
cd LightlyShaders-kubuntu; mkdir qt6build; cd qt6build
cmake ../ -DCMAKE_INSTALL_PREFIX=/usr && make
sudo make install
```

**注：** Plasma/KWin 更新后可能需要重新编译插件。如果 CMake 报告缺少 XCB 头文件，请先安装上面的完整依赖列表，再重新执行配置命令。
