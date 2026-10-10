# glash-lzcapp

[gangz1o/glash](https://github.com/gangz1o/clash4docker)（Mihomo 内核 + MetacubexD 面板）的懒猫微服打包。

## 访问

- 打开应用会自动跳转到 MetacubexD 面板（`/ui/`）
- 面板首次进入：后端地址保留默认（自动使用当前域名），密钥填安装向导里设置的
  「仪表盘密钥」（默认 `clash123`）
- 代理端口：HTTP `7890` / SOCKS5 `7891` / 混合 `7892`（默认允许局域网，用微服设备 IP 连接）

## 安装向导

安装时会显示设置向导：订阅地址（可留空，使用手动配置）、仪表盘密钥、订阅更新周期、
允许局域网、时区。订阅地址在启动时下载，并按周期自动刷新。

## 发布

- 每日定时检查上游镜像新版本（`gangz1o/glash` 的 SemVer tag），发现即自动发版到喵喵商店
- **重新发布同版本**（例如修复 manifest 后）：删除 GitHub Release 的 `vX.Y.Z` 与商店中的
  该版本后，手动触发 `Publish LazyCat application`，在 `version` 输入里填 `X.Y.Z`
  强制构建；会重新生成 Release 资产并重新上架

## 版权

上游 [gangz1o/clash4docker](https://github.com/gangz1o/clash4docker)（MIT）；本仓库仅为打包。
