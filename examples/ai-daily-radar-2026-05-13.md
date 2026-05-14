# AI Daily Radar｜2026-05-13

- 时间窗：过去 24 小时
- 数据源：AI HOT
- 应用层精选：12 条
- 今日主线：AI 应用层正在从“会回答”转向“能持续执行、跨应用操作、并用状态和评测约束结果”。

## 01 今日结论

- **今天最值得关注**：长时运行 agent、状态机约束、跨应用 computer use、Gmail/法律/财务等垂直集成同时出现，说明 agent 正在进入真实工作流。
- **对我意味着什么**：不要只把 AI 热点当输入材料，今天更值得练的是把一个信息信号转成可交付的小输出。
- **建议今天试什么**：做一个“状态驱动的 AI 任务模板”，把一个重复任务拆成状态、输入、工具、输出和验收标准。

## 02 趋势雷达

1. **Agent 从聊天助手变成可持续运行的任务系统**：Google ADK 强调暂停、恢复和持久上下文，Statewright 用状态机限制 agent 的执行路径，Claude Code `/goal` 和 Symphony 的“每个任务一个 Codex agent”都在把完成任务变成产品核心。

2. **AI 正在进入系统界面和具体业务软件**：Codex computer use、Android Intelligence、Gemini 智能指针、Grok 接入 Gmail、Claude 法律连接器都说明 AI 不再只是聊天框，而是在邮件、浏览器、文档、代码和业务系统里直接行动。

3. **应用层竞争开始转向上下文、评测和成本纪律**：BenchLoop、本地模型评测、token 浪费讨论、SKILL.md、模型路由和 prompt caching 都指向同一件事：会用 AI 的差距会越来越体现在“如何给上下文、如何验收、如何控制成本”。

## 03 今日术语表

| 术语 | 这是什么 | 为什么重要 | 我该怎么理解或使用 |
|---|---|---|---|
| 长时运行智能体 | 可以暂停、恢复、等待外部事件并继续执行的 agent。 | 它适合真实业务流程，而不只是一次性问答。 | 把任务拆成阶段，并为每个阶段定义状态、输入和退出条件。 |
| 状态机约束 | 用固定状态和转移规则限制 agent 的执行路径。 | 它能减少跑偏、重复操作和漏验收。 | 复杂任务先画“收集-计划-执行-检查-交付”的状态图，再让 AI 执行。 |
| Daily Active Agents | 衡量每天实际活跃并交付成果的 agent 数量。 | 它把价值指标从 token 消耗拉回到真实产出。 | 判断一个 AI 工作流有没有价值，看它每天交付什么，而不是调用了几次模型。 |
| Computer Use | AI 可以点击、输入、读取屏幕并跨应用操作。 | 它让 AI 从内容生成器变成流程执行者。 | 适合邮件整理、跨系统搬运、网页测试、数据录入和报告生成。 |
| Prompt Caching / 模型路由 | 复用重复上下文，并按任务选择不同模型。 | 它能降低成本，也能提升稳定性。 | 重复知识沉淀成 skill 或模板，简单任务不要默认使用最贵模型。 |

## 04 趋势翻译表

| 原始信号 | 应用层含义 | 可能机会 |
|---|---|---|
| Google ADK 支持长时运行 agent，Statewright 用状态机提升可靠性 | Agent 产品开始重视持久状态、失败恢复和可控执行路径。 | 把自己的重复工作流改成状态驱动模板，让 AI 明确知道何时继续、何时停止。 |
| Codex 跨应用操作、Android Intelligence、Gemini 智能指针 | AI 正在成为系统级交互层，而不是单独应用。 | 设计跨 Gmail、浏览器、文档、代码工具的个人自动化流程。 |
| Grok 接入 Gmail，Claude 进入法律行业，Codex 服务财务团队 | 垂直场景里的 AI 正在连接真实数据和业务软件。 | 为邮箱、合同、财务报告、知识库等高频场景建立专用 prompt 和验收标准。 |

## 05 今天的练习

- **练习锚点**：趋势 1“Agent 从聊天助手变成可持续运行的任务系统”；来源信号包括 Google ADK 长时运行 agent、Statewright 状态机、Claude Code `/goal`。
- **为什么今天做**：今天的核心信号都在说明，AI 工作流的下一步不是多输入信息，而是把信息转成可运行、可验收的输出流程。
- **目标**：在 60 分钟内写出一个“状态驱动的 AI 任务模板”，用于把每天 AI 信息转成一个可交付实践。
- **输入材料**：今天这份 AI Daily Radar、一个你重复做的任务、一个你希望最终产出的具体结果。
- **步骤**：
  1. 选一个任务，例如“把 AI 热点转成白板分享提纲”。
  2. 拆成 5 个状态：收集、筛选、翻译、产出、验收。
  3. 为每个状态写清楚输入、允许工具、输出格式和停止条件。
  4. 加 2 条失败处理规则，例如“来源不足时降低结论强度”“练习太大时缩成 30 分钟版本”。
  5. 写一个最终验收标准：今天必须产出一个可发送、可展示或可执行的东西。
- **验收标准**：得到一页 Markdown 模板；Codex 看到模板后能明确下一步做什么、何时停止、产出是否合格。

## 06 应用层信号

1. **Miaoda 应用与企业版上线，自生成代码占比 90%**，X：百度 Baidu：编程助手正在让按需定制软件具备商业可行性。https://x.com/Baidu_Inc/status/2054511974172557463
2. **AI 技能更新地图组件，支持交互与标记**，X：歸藏：AI skill 开始支持空间信息处理和可视化操作。https://x.com/op7418/status/2054433146532479266
3. **智能体时代新指标：日活跃智能体数**，X：百度 Baidu：agent 价值开始用交付成果衡量，而不是只看 token。https://x.com/Baidu_Inc/status/2054400181903524133
4. **Codex 应用内浏览器升级，提升多视口测试与标注效率**，X：Tibo：AI 开发工作流开始内置更强的验证与截图反馈。https://x.com/thsottiaux/status/2054398093886673260
5. **BenchLoop：本地大模型一键基准测试与排行榜发布**，X：Berry Xia：模型选择开始走向可评测、可比较。https://x.com/berryxia/status/2054390836721553487
6. **无需注册付费，Telegram 内一键启动 AI 智能体**，X：Berry Xia：agent 的入口正在变轻，接近“即用即走”。https://x.com/berryxia/status/2054358231791923392
7. **Claude Code 新增 `/goal` 功能确保任务完成**，X：Claude Devs：编码 agent 开始围绕目标完成度设计。https://x.com/ClaudeDevs/status/2054351031279186040
8. **90% 的人在白白浪费 Token**，X：Berry Xia：上下文管理、模型路由和 skill 化会成为 AI 工作流基本功。https://x.com/berryxia/status/2054339265103065156
9. **Codex 实现跨应用无感多任务处理**，X：OpenAI Developers：AI 正在进入后台跨应用执行场景。https://x.com/OpenAIDevs/status/2054298427245441141
10. **使用 ADK 构建可暂停、恢复且永不丢失上下文的长时运行 AI 智能体**，Google Developers Blog：生产级 agent 需要持久状态和事件驱动恢复。https://developers.googleblog.com/build-long-running-ai-agents-that-pause-resume-and-never-lose-context-with-adk
11. **Grok 接入 Gmail，智能邮件助手革新收件箱管理**，X：cb_doge：邮箱正在成为个人 AI agent 的关键入口。https://x.com/cb_doge/status/2054225901232259092
12. **Statewright：通过可视化状态机提升 AI 智能体可靠性**，Hacker News：状态机约束可显著提升 agent 在任务中的稳定性。https://github.com/statewright/statewright

## 07 明天观察

- 看长时运行 agent 是否继续沉淀出通用设计模式：状态、记忆、权限、验收、失败恢复。
- 观察 Gmail、浏览器、文档、代码工具这类真实工作入口是否继续被 agent 化。
- 继续关注上下文管理、模型路由和评测工具，避免“输入很多，输出很少”。
