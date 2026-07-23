# LocalShot 0.3.1（Build 15）公开测试版

本版本把直接分发版升级为 Universal 2，同一个安装包同时支持 Apple 芯片与 Intel Mac。截图、标注、OCR、翻译、长截图、区域录屏、离线授权和本地数据逻辑保持不变。

## 双架构支持

- 应用主程序同时包含 `arm64` 与 `x86_64` 两种架构，不需要按芯片下载不同版本。
- 两种架构的最低系统均为 macOS 13，只依赖 macOS 和 Swift 系统库。
- Apple 芯片 Mac 继续原生运行；Intel Mac 直接运行 x86_64 版本。
- 区域屏幕录制和原位置翻译仍需要 macOS 15 或更高版本。

## 更新兼容

- Build 15 安装包名称保留 `arm64` 标识，因此 Build 5–14 的旧更新器仍能发现并下载本版本。
- Build 15 更新器会优先选择 Universal 2 安装包，并按当前 Mac 的处理器架构跳过不兼容的历史版本。
- 覆盖安装不会主动删除截图、录屏、设置或离线授权；macOS 仍可能因应用签名身份变化要求重新允许屏幕捕获。

## 验证范围

- arm64 与 x86_64 均已完成 release 构建、最低系统和动态依赖检查。
- Universal 应用包、只读挂载后的 DMG 和 SHA-256 校验均已通过自动审计。
- x86_64 更新器与应用启动已在 Apple Silicon Mac 的 Rosetta 环境中验证；实体 Intel Mac 的完整界面回归仍建议由 Intel 用户继续反馈。

## 下载文件

- `LocalShot-0.3.1-build15-offline-license-universal2-arm64-x86_64.dmg`：Apple 芯片与 Intel Mac 通用客户安装包。
- `SHA256SUMS-v0.3.1-build15-public.txt`：安装包完整性校验值。

## 重要提示

- 当前版本未经 Apple 公证，macOS 首次启动时可能需要在“系统设置 → 隐私与安全性”中点击“仍要打开”。
- 请勿从第三方转载链接下载安装包。
- 安装、升级或激活方法见仓库中的 `INSTALL.md`。
