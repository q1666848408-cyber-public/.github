# q1666848408-cyber-public 上传规范

> 本文档记录了将私有仓库发布为公开展示版本的完整规则。  
> 每次新增公开仓库时，请遵循此规范。

---

## 账号定位

`q1666848408-cyber-public` 是对外展示用公开账号，所有仓库均为私有源码的 **~15% skeleton 展示版本**，用于技术能力展示、招聘 / 合作参考。

**不用于：** 开源协作、外部 contribution、发布可运行完整代码。

---

## 私有 → 公开骨架规则

### 1. 保留比例
只保留约 **15%** 的内容，重点是架构和技术栈，不暴露核心实现。

### 2. 必须删除的内容

| 类型 | 示例 |
|------|------|
| Claude Code 配置 | `.claude/` 目录（agents、skills、commands） |
| 核心业务脚本 | 实际 shell/python 脚本逻辑（用 `.gitkeep` 占位） |
| 账号 / 凭证信息 | `accounts/`、API Keys、密码、IP |
| 运营数据 | `logs/`、实际内容库、渲染产物目录 |
| AI 提示词策略 | `settings/`、详细 personas、`CLAUDE.md` |
| 媒体产物 | 渲染输出视频/图片（`out/`、`output/`） |
| 依赖包 | `node_modules/` |

### 3. 必须保留的内容

| 类型 | 说明 |
|------|------|
| `README.md` | 按规范重写（见下方） |
| 配置文件 | `package.json`、`tsconfig.json`、`.gitignore` 等 |
| 目录结构 | 用空文件夹 + `.gitkeep` 展示架构 |
| 文档说明 | 子模块的 `README.md`、架构说明文档 |

---

## 命名规则

- **只用项目名，不暴露公司名**
- PascalCase + 连字符
- 示例：`Ofox-Docs`、`AI-News-TikTok`、`Content-Engine-TikTok`

---

## README 规范

每个公开仓库的 README 必须包含：

```markdown
<div align="center">

# [emoji] 项目名称

[![badge](...)](#)

**一句话描述项目功能**

> ⚠️ **Showcase Only** — ~15% skeleton. Full source is internal.

</div>

---

## Overview
## Architecture（架构图，文字版）
## Directory Structure
## Tech Stack（技术栈表格）
## Related Repos

---

MIT © [ofox.ai](https://ofox.ai)
```

---

## 仓库描述规范

- 使用英文
- 简明描述核心功能
- 结尾固定加：`Showcase only (~15% skeleton).`

---

*最后更新：2026-06*
