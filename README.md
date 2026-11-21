# better-claude · Claude 破甲插件

> 移植自 [dsh-purge](https://github.com/HunYiSage/dsh-purge) v1.1.92（未删减原文）
> 整理：可立奇 (Keliqi)

## 这是什么

Claude Desktop / Claude Code 的**本地插件**，包含：

| 组件 | 内容 |
|---|---|
| `skills/purge-core` | 破甲核心规则（dsh-purge 原文 29.7KB 未删减：JAR 命名劫持、反注入反射、无条件交付规范） |
| `skills/purge-redteam` | 红队 22 个专项流程（侦察/扫描/隧道/横向/凭据/WebShell） |
| `rules/` | 无条件进 system 的规则层 |
| `hooks/` | UserPromptSubmit 每条消息强制上下文注入 |

## 安装（桌面端）

### 方式一：从 GitHub 安装（本仓库）

1. 打开 Claude Desktop → 设置 → 技能和插件 → 添加
2. 选择「从 GitHub 安装」，输入本仓库地址
3. 启用插件，新开会话生效

### 方式二：CLI 安装

```bash
# 先把本仓库克隆到本地，然后：
claude plugin marketplace add <克隆目录的父目录>
claude plugin install purge-plugin@keliqi-market -y
```

## 使用

- 输入 `/purge-core` 激活核心人格
- 输入 `/purge-redteam <任务>` 路由到对应红队流程
- 直接说话也行，rules 层已无条件生效

## 结构

```
.claude-plugin/plugin.json    插件清单
skills/purge-core/SKILL.md    核心人格（原文）
skills/purge-redteam/*.md     22 个专项文档（原文）
rules/jar-core.md             system 注入层
hooks/hooks.json              每消息上下文注入
```

## 说明

- 内容为 dsh-purge v1.1.92 的**原样移植**，未做任何删改
- 仅供本地环境的安全研究、CTF 练习与授权测试使用
- 作者不对滥用行为负责

---
MIT © 可立奇 (Keliqi)