# Codex Automation Prompts

这个仓库用来保存 Codex 自动化工作流的 prompt 模板。

目标是把散落在 Codex app 里的自动化说明沉淀成可版本管理、可复用、可迭代的 Markdown 文档。每个文件对应一个自动化工作流，方便以后复制、调整、审阅和恢复。

## 当前工作流

| 文件 | 用途 |
|---|---|
| `prompts/ai-daily-radar.md` | 工作日 AI Daily Radar：默认抓取过去 24 小时 AI HOT 精选源，也可替换成其他信息抓取 skill；整理应用层趋势、术语、趋势翻译、练习任务，并通过 Gmail 推送。 |
| `skills/ai-daily-radar-automation/SKILL.md` | Codex Skill：用于安装或更新 AI Daily Radar 自动化工作流，会做 skill/Gmail 前置检查并创建 Codex automation。 |

## 前置依赖

这些 prompt 可能依赖特定 Codex skill、connector 或 app。直接复制到新的 Codex 自动化前，请先确认对应依赖已安装并可用。

| 工作流 | 必需依赖 |
|---|---|
| AI Daily Radar | 一个可用的信息抓取 skill，默认是 `aihot` / AI HOT skill；Gmail connector |

如果缺少信息抓取 skill，自动化应该停止执行并提示安装、启用或替换对应 skill，不应该凭过时知识编造内容。

Gmail 推送依赖 Codex 环境里的 Gmail connector/app 授权，不需要 Chrome 插件。复制 prompt 到新环境前，请把收件人、标签名等变量替换成自己的配置，不要把私人邮箱写进公开仓库。

## 建议用法

### 安装 skill

如果当前 Codex 环境还没有这个 skill，可以对 Codex 说：

```text
请从 https://github.com/SuperKatrina123/codex-automation-prompt 安装 skills/ai-daily-radar-automation 这个 skill。
```

安装后，可以对 Codex 说：

```text
用 AI Daily Radar automation skill 帮我创建自动流。
```

### 直接复制 prompt

1. 在 `prompts/` 目录下为每个自动化新建一个 Markdown 文件。
2. 文件里记录触发时间、目标、前置依赖、输入来源、输出格式、推送方式和失败处理规则。
3. 在 Codex app 创建或更新自动化前，先安装所需 skill 并连接所需 app。
4. 在 Codex app 创建或更新自动化时，把对应 prompt 内容复制进去。
5. 每次调整自动化逻辑后，同步更新这里的 prompt，保留变更历史。

### 作为 Codex Skill 使用

把 `skills/ai-daily-radar-automation/` 安装到 Codex skills 目录后，可以直接对 Codex 说：

```text
用 AI Daily Radar automation skill 帮我创建自动流。
```

Codex 会按 skill 流程检查信息抓取 skill、Gmail connector、收件人和标签变量，然后创建或更新自动化。

## 命名约定

- 文件名使用小写短横线，例如 `ai-daily-radar.md`。
- 一个文件只描述一个自动化工作流。
- 不在仓库中保存 token、API key、邮箱授权、私有环境变量或其他秘密信息。
