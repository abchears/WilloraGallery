# Willora Widgets Gallery

Windows 点击即运行的画廊演示。

Willora Widgets 是商业 Qt Widgets SDK。本仓库只发布 **Windows x64 演示程序**，用来查看控件画廊；不提供 SDK 源码、头文件或导入库。

This repository is the free Windows demo of the commercial Willora Widgets Qt SDK. It is not the SDK source.

## 环境要求

- Windows 10 或 Windows 11，64 位（x64）
- [Microsoft Visual C++ 可再发行组件（x64）](https://learn.microsoft.com/zh-cn/cpp/windows/latest-supported-vc-redist)

程序依赖 `VCRUNTIME140.dll` 和 `MSVCP140.dll`。安装包里没有 `vc_redist.x64.exe`，请安装微软提供的可再发行组件。机器上已经装过 Visual Studio，或已经有较新的 VC++ 运行库时，一般不用再装。

x64 安装包：<https://aka.ms/vs/17/release/vc_redist.x64.exe>

## 快速开始

解压后请保持目录结构。`platforms` 等插件目录，以及 `willora-runtime.license`，需要和 `WilloraGallery.exe` 放在同一文件夹。

### 下载 Release 压缩包

1. 打开 [v1.0.0 Release](https://github.com/abchears/WilloraGallery/releases/tag/v1.0.0)，下载 `WilloraGallery-Demo-ClickToRun.zip`。
2. 解压到任意目录。
3. 双击 `Start-Demo.bat`。也可以直接运行 `WilloraGallery.exe`。

### 克隆仓库

```bat
git clone https://github.com/abchears/WilloraGallery.git
cd WilloraGallery\demo
Start-Demo.bat
```

`demo\WilloraGallery.exe` 与 Release 压缩包是同一套文件。

## opengl32sw.dll（可选）

默认走系统显卡驱动（Qt 平台插件会加载 `opengl32.dll`）。压缩包不包含 `opengl32sw.dll`。

只有显卡驱动异常、窗口无法创建时，才需要把与本演示所用 Qt 5 相匹配的软件渲染库 `opengl32sw.dll` 放到 `WilloraGallery.exe` 旁边。该文件来自对应的 Qt 5 Windows 套件，本仓库不提供。普通机器不用准备它。

## 目录里有什么

| 文件 | 作用 |
| --- | --- |
| `WilloraGallery.exe` | 画廊演示 |
| `Start-Demo.bat` | 进入程序目录并启动 |
| `willora-runtime.license` | 本演示构建的运行时许可 |
| `WilloraWidgets.dll`、`WilloraFileTasks.dll`、`WilloraNetwork.dll`、`WilloraTasksCore.dll`、`WilloraWorkflows.dll` | Willora 运行库 |
| `Qt5Core.dll`、`Qt5Gui.dll`、`Qt5Network.dll`、`Qt5Svg.dll`、`Qt5Widgets.dll` | Qt 5 运行库 |
| `libEGL.dll`、`libGLESv2.dll`、`d3dcompiler_47.dll` | ANGLE 与着色器编译 |
| `platforms\qwindows.dll` | Windows 平台插件 |
| `imageformats\` | gif、icns、ico、jpeg、svg、tga、tiff、wbmp、webp |
| `styles\qwindowsvistastyle.dll` | Windows 样式 |
| `iconengines\qsvgicon.dll` | SVG 图标 |

## 未包含的内容

- Willora Widgets 商业 SDK（头文件、导入库、文档、示例工程、源码）
- `vc_redist.x64.exe`
- `opengl32sw.dll`

商业 SDK 需要另行取得授权。本仓库不能代替正式 SDK 交付。

## 许可

`demo/willora-runtime.license` 是本构建的运行时许可（许可编号 `DEMO-LICENSE-20261019A`，产品 Willora Widgets，运行时主版本 4）。该许可允许随**本演示构建**再分发其中的 Willora 运行库，不允许把 SDK 单独再分发出去。

Willora Widgets 是专有软件。本仓库不使用 MIT 许可证，也不以开源方式授权 SDK 或演示程序。请整目录使用，保留许可文件和 `platforms` 等插件目录。

随附的 Qt 与 ANGLE 动态库只为运行本演示而一同提供，权利归其各自权利人所有。

## English

Click-to-run Windows x64 gallery demo of the commercial Willora Widgets Qt SDK. The SDK itself is not in this repository.

1. Download [`WilloraGallery-Demo-ClickToRun.zip`](https://github.com/abchears/WilloraGallery/releases/tag/v1.0.0) and unzip it, or clone this repo and open `demo\`.
2. Install the [Visual C++ Redistributable (x64)](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist) when `VCRUNTIME140.dll` or `MSVCP140.dll` is missing. `vc_redist.x64.exe` is not bundled. Direct download: <https://aka.ms/vs/17/release/vc_redist.x64.exe>
3. Run `Start-Demo.bat`.

`opengl32sw.dll` is an optional Qt software OpenGL renderer and is not included. `demo/willora-runtime.license` allows runtime redistribution of this demo build only. Willora Widgets is proprietary software; this project is not MIT-licensed.
