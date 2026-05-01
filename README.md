# Claude Desktop zh-CN Offline Pack

![Claude Desktop](https://img.shields.io/badge/Claude%20Desktop-1.5354.0-black)
![Platform](https://img.shields.io/badge/Platform-Windows%20x64-0078D4)
![Language](https://img.shields.io/badge/Language-zh--CN-2ea44f)
![Offline](https://img.shields.io/badge/Offline-Yes-8A2BE2)

> [!IMPORTANT]
> 这是一个非官方的 Claude Desktop Windows 版简体中文离线汉化包。
> 当前已实测适配 Claude Desktop `1.5354.0`。Claude 更新后通常需要重新安装本包。

## 项目简介

本仓库提供一个可直接分发的离线汉化包，用于把 Windows 版 Claude Desktop 切换为 `zh-CN` 界面。
安装包不联网、不下载额外依赖，包含安装、验证、回滚所需脚本，适合归档、转存和重复部署。

## 下载

- 推荐下载页：[Releases](https://github.com/Sukebeet/Nick-Claude-ZH/releases)
- 仓库文件：`Claude-Desktop-zh-CN-offline-pack-20260429-for-1.5354.0.zip`
- 文件大小：`19.51 MB`
- SHA-256：`398F72BC60EF173A3C7E5D3DA119FF1B23E029A30DDC78025AB23EA2D9809B9F`

## 功能特性

- 离线安装，不依赖联网
- 自动写入 `zh-CN` 语言资源
- 补丁处理仅靠 JSON 无法覆盖的前端硬编码英文
- 安装前自动备份，支持回滚
- 附带验证脚本，方便确认安装结果

## 兼容信息

| 项目 | 值 |
| --- | --- |
| 目标应用 | Claude Desktop |
| 已测版本 | `1.5354.0` |
| 目标平台 | `Windows x64` |
| 所需权限 | `Administrator` |
| 是否联网 | `No` |

## 快速开始

1. 下载并解压 ZIP。
2. 双击 `install-zh-cn.bat`。
3. 如需验证，运行 `scripts\verify-claude-zh-cn.ps1`。
4. Claude 更新后，重新执行安装脚本。

## 包内容

- `install-zh-cn.bat`：推荐的一键安装入口
- `install-zh-cn-local.bat`：本地安装入口
- `scripts/install-claude-zh-cn.ps1`：主安装脚本
- `scripts/verify-claude-zh-cn.ps1`：验证脚本
- `scripts/rollback-claude-zh-cn.ps1`：回滚脚本
- `payload/merged/*.json`：合并后的离线中文资源

## 说明

- 需要管理员权限，因为 Claude Desktop 安装目录通常位于 `WindowsApps`。
- 脚本会修改 Claude Desktop 的资源文件，并在安装前创建备份。
- 如果安装后仍出现英文界面，通常是缓存未刷新，重新执行安装脚本即可处理。
- 本仓库当前以发布现成离线包为主，不提供在线安装器。

## 免责声明

- 本项目与 Anthropic 无官方关联。
- 使用前建议先阅读包内 `README.md`、`docs/INSTALL-NOTES.md` 和相关脚本。
- 请仅在你理解风险的前提下，以管理员权限运行安装脚本。
