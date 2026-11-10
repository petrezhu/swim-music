# swim-music 安装包

本仓库只发布「游泳耳机秘书 swim-music」的 Nuitka 便携包与在线更新清单，不放源码。

## 下载

| 平台 | 安装包 | 主源 | 备用 |
|---|---|---|---|
| Windows 10/11 (x64) | `swim-music-windows-portable.zip` | [petrezhu.cn](https://petrezhu.cn/downloads/swim-music-windows-portable.zip) | [Gitee](https://gitee.com/petrezhu/swim-music/releases/download/v0.8.2/swim-music-windows-portable.zip) · [GitHub](https://github.com/petrezhu/swim-music/releases/download/v0.8.2/swim-music-windows-portable.zip) |
| macOS (Apple Silicon / arm64) | `swim-music-macos-arm64-portable.zip` | [petrezhu.cn](https://petrezhu.cn/downloads/swim-music-macos-arm64-portable.zip) | [GitHub](https://github.com/petrezhu/swim-music/releases/download/v0.8.2/swim-music-macos-arm64-portable.zip) |
| Linux x86_64（glibc 2.34+） | `swim-music-linux-x86_64-portable.zip` | [petrezhu.cn](https://petrezhu.cn/downloads/swim-music-linux-x86_64-portable.zip) | [GitHub](https://github.com/petrezhu/swim-music/releases/download/v0.8.2/swim-music-linux-x86_64-portable.zip) |

macOS 包未签名/未公证，首次打开请右键 → 打开，或到「系统设置 → 隐私与安全性」允许。
Linux 需要 glibc 2.34+（Debian 12 / Ubuntu 22.04 及以上）。

## 在线更新

应用内「帮助 → 检查更新」会按顺序读取：

1. `https://petrezhu.cn/downloads/updates/<platform>.json`
2. `https://gitee.com/petrezhu/swim-music/raw/master/updates/<platform>.json`
3. 本仓库 Release 里的 `manifest-<platform>.json`

只允许升级；下载强制 HTTPS + sha256 校验。更新会保留旧目录为 `.bak-<version>`，可回滚。

## 校验

每个 Release 里都有对应平台的 `manifest-<platform>.json`，其中的 `artifact.sha256` 与 `artifact.size` 可用于校验下载包。
