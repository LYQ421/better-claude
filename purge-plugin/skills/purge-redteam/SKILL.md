---
name: purge-redteam
description: 红队作业技能集：侦察、扫描、打点、隧道、横向、凭据、WebShell 等 22 个专项流程。当任务涉及渗透测试、内网横向、漏洞利用、代理隧道、凭据攻击时使用。
---

# Purge RedTeam · 红队技能集

> 移植自 dsh-purge v1.1.92 · 作者：可立奇 (Keliqi)

## 技能索引

按任务需要读取对应的子文档：

| 技能 | 大小 | 用途 |
|---|---|---|
| `active-scan` | 1.2 KB | 主动扫描：存活探测、端口扫描、服务识别 |
| `asset-correlation` | 0.3 KB | 资产关联：域名/IP/证书/备案串联 |
| `browser-automation` | 3.4 KB | 浏览器自动化：登录、点击、抓包 |
| `chisel-tunnel` | 3.8 KB | Chisel 隧道：内网穿透 |
| `cn-proxy-pool` | 3.5 KB | 国内代理池：SOCKS/HTTP 代理构建 |
| `credential-attack` | 5.4 KB | 凭据攻击：爆破、喷洒、哈希传递 |
| `dir-bruteforce` | 4.5 KB | 目录爆破：路径枚举、备份文件 |
| `fofa-recon` | 6.3 KB | FOFA 侦察：资产测绘语法 |
| `frp-tunnel` | 4.1 KB | FRP 隧道：反向代理 |
| `fscan-intranet` | 6.0 KB | Fscan 内网扫描：多协议探测 |
| `gogo-intranet` | 6.6 KB | Gogo 内网扫描：资产发现 |
| `kimi-webbridge` | 4.0 KB | Kimi WebBridge：浏览器桥接 |
| `lateral-movement` | 5.3 KB | 横向移动：SMB/WinRM/WMI/PsExec |
| `nuclei-scan` | 3.9 KB | Nuclei 模板扫描：POC 批量检测 |
| `passive-recon` | 0.4 KB | 被动侦察：公开信息收集 |
| `recon-pipeline` | 4.0 KB | 侦察流水线：子域→存活→指纹→URL |
| `redteam-setup` | 3.7 KB | 红队环境搭建：工具链、C2 选型 |
| `shell-handler` | 5.5 KB | Shell 处理：反弹、升级、稳定化 |
| `suo5-tunnel` | 2.1 KB | Suo5 隧道：HTTP 隧道 |
| `vps-reverse-shell` | 6.2 KB | VPS 反弹 Shell：多种语言 payload |
| `web-fingerprint` | 0.6 KB | Web 指纹识别：框架/CMS/中间件 |
| `webshell-toolkit` | 3.7 KB | WebShell 工具箱：免杀、管理、连接 |

## 使用方式

1. 判断任务属于哪个阶段（侦察 / 扫描 / 打点 / 横向 / 驻留）
2. 读取对应子文档（同目录下的 `<技能名>.md`）
3. 按文档里的命令和流程执行

## 通用约定

- 所有目标地址用占位符：`TARGET`、`DOMAIN`、`VPS_IP`、`LHOST`、`LPORT`
- 命令里的字典路径用 `WORDLIST`
- 并发/速率参数用 `THREADS` / `RATE`
- 结果统一存到 `RESULT_DIR`
