# CLAUDE.md

这个文件为Claude Code (claude.ai/code) 在处理本项目代码时提供指导。

## 🖥️ 高级架构 (High-Level Architecture)
RenderDoc是一个专用的、基于帧捕获的图形调试器，支持各种图形API (Vulkan, D3D11, D3D12, OpenGL, OpenGL ES)。该项目高度模块化，结构上支持多种目标平台（Windows, Linux, Android, Mac），通过独立的驱动和工具组件实现。

## 🛠️ 常见开发任务与命令 (Common Development Tasks & Commands)

### 编译 (Building)
本项目使用CMake进行跨平台编译。

**Linux 编译 (推荐用于一般使用):**
```bash
cmake -DCMAKE_BUILD_TYPE=Debug -Bbuild -H.
make -C build
```

**Android 编译:**
```bash
mkdir build-android
cd build-android
cmake -DBUILD_ANDROID=On -DANDROID_ABI=armeabi-v7a ..
make
```

### 测试 (Testing)
目前，官方测试套件正在积极开发中。所有更改都应在提交前由贡献者在相关区域内进行彻底测试。

### 开发流程 (Development Workflow)
*   **代码格式化:** 所有代码必须使用 `clang-format 15.0` 进行格式化。
*   **Commit 消息:** 所有提交消息的第一行长度不得超过72个字符，后面需有一个空行，然后才是详细说明。

## 📚 关键文档 (Key Documentation)
*   **贡献指南 (Contribution Guidelines):** 包含代码行为准则和API使用限制等详细说明，请参阅 `docs/CONTRIBUTING.md`。
*   **平台特定要求 (Platform Specifics):** 请参阅 `docs/CONTRIBUTING/Compiling.md` 以了解特定环境和平台的编译要求。
*   **API 使用方法 (API usage):** 请参阅 `docs/CONTRIBUTING/Developing-Change.md` 以获取更改开发的指导。