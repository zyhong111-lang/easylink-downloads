# EasyLink Downloads

EasyLink macOS / Windows 下载版的官方发布仓库。这里仅提供安装包、自动更新包、公开验签材料和发行说明。

[查看最新发行版本](https://github.com/zyhong111-lang/easylink-downloads/releases/latest)

## 1.1.26 迁移版下载

| 平台 | 安装包 |
| --- | --- |
| Mac Apple Silicon（M 系列） | [DMG](https://github.com/zyhong111-lang/easylink-downloads/releases/download/v1.1.26/EasyLink_1.1.26_aarch64.dmg) |
| Mac Intel | [DMG](https://github.com/zyhong111-lang/easylink-downloads/releases/download/v1.1.26/EasyLink_1.1.26_x64.dmg) |
| Windows x64 | [安装包](https://github.com/zyhong111-lang/easylink-downloads/releases/download/v1.1.26/EasyLink_1.1.26_x64-setup.exe) |
| Windows ARM64 | [安装包](https://github.com/zyhong111-lang/easylink-downloads/releases/download/v1.1.26/EasyLink_1.1.26_arm64-setup.exe) |

[全部文件与发行说明](https://github.com/zyhong111-lang/easylink-downloads/releases/tag/v1.1.26)。`fixed_webview2` 为自带固定 WebView2 运行时的较大 Windows 安装包。

## 旧版首次迁移

旧下载版仍内置原发布者的更新地址和密钥，需要手动覆盖安装本次迁移版一次；之后自动更新使用本仓库。

- 无需卸载或删除账户配置。
- Mac：退出原下载版，覆盖到原应用相同路径、相同名称。如果原来是 `EasyLink SS.app`，请沿用该名称覆盖，避免同时留下两个下载版。
- Windows：退出原下载版，覆盖安装到原目录。
- Mac App Store / Microsoft Store 版继续通过商店更新。

## 签名与校验

Mac 下载版使用公司 Developer ID Application 签名，通过 Apple 公证并附带公证票据。所有自动更新包均有 Ed25519 签名。

Windows 1.1.26 本次仅使用更新包签名，CA 系统发布者签名后补，安装时可能仍出现未知发布者 / SmartScreen 提示。

每个版本提供 `SHA256SUMS.txt`、`updater.pub`、更新签名及安装验收记录。公开仓库不包含私钥、会员数据或服务器凭据。

普通更新清单为 `updater/update.json`，固定 WebView2 更新清单为 `updater/update-fixed-webview2.json`。更新包通过构建、签名和隔离升级验收后发布，并在匿名下载完整校验成功后切换更新清单。
