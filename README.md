# openclaw-config

`openclaw-config` 是一个可通过 `npx add-skill` 安装的技能仓库，用于排查和配置 OpenClaw（渠道、模型、安全策略、cron、memory）。

## Skill Metadata

- `name`: `openclaw-config`
- `description`: `Manage OpenClaw bot configuration - channels, agents, security, and autopilot settings`
- `version`: `3.0.0`

以上元数据位于根目录 [`SKILL.md`](./SKILL.md) 的 frontmatter 中。

## npx 安装标准（本仓库已满足）

- 根目录必须存在 `SKILL.md`
- `SKILL.md` 顶部必须有 YAML frontmatter（`name`/`description`，可选 `version`）
- 技能说明内容写在 `SKILL.md` 中，按需引用 `scripts/`、`references/`、`assets/`

当前仓库结构：

```text
openclaw-config/
├── SKILL.md
└── README.md
```

## 安装方式

### 1) 通过 GitHub 仓库安装

```bash
npx add-skill github:twodogegg/openclaw-config
```

### 2) 通过 git URL 安装（等价）

```bash
npx add-skill git@github.com:twodogegg/openclaw-config.git
```

## 安装后验证

```bash
# 查看已安装技能（不同环境命令可能略有差异）
clawdhub list

# 或在技能目录确认
ls ~/.openclaw/workspace/skills/
```

## 更新发布流程

```bash
git add SKILL.md README.md
git commit -m "docs: update openclaw-config skill"
git push origin main
```

## 兼容性说明

- 本技能文档中的命令默认面向 macOS/Linux shell（`bash/zsh`）。
- 配置文件路径默认使用 `~/.openclaw/`。
