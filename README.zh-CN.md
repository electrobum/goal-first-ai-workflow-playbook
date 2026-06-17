# Goal-First AI Workflow Playbook | Goal 优先 AI 工作流手册

[English](README.md) | 中文

这是一个面向长期 AI 工作流的开源 playbook，重点不是“让 AI 看起来很忙”，而是让它在跨 session、过夜跑、长链路任务中持续推进真实工作。

## 这个项目解决什么问题

很多 AI 系统不是因为完全停掉才失败，而是因为它们一直显得很活跃：

- 记录越来越多；
- 状态一直刷新；
- 多个线程不断对话；
- token 持续消耗；
- 但真正的目标并没有明显推进。

这个仓库就是为了解决这种问题。

它提供的是一套长期 AI workflow 的控制方法，而不是一个夸张的“万能自治框架”。

## 核心思路

用一套更克制、更可验证的方式去运行长期 AI 工作：

- 保持一个主执行线程；
- 用文件保存连续性状态；
- 用 hard gate 绑定真实输出；
- 用精确 handoff 让下一个线程能直接接上；
- 只有在确实需要恢复时，才唤醒兜底自动化。

最核心的一句话是：

> 可以激进地简化编排，但不能偷偷简化真正的工作义务

## 适合哪些人

如果你在做这些事，这个项目会特别有用：

- agentic coding workflow
- 长期运行的内部 AI 助手
- 文档、知识、审查、分析流水线
- 需要过夜跑、跨天跑的自动化项目
- 任何需要在中断后正确接续的 AI workflow

## 你能在这个仓库里找到什么

- [docs/getting-started.md](docs/getting-started.md)：最快上手方式
- [docs/final-architecture.md](docs/final-architecture.md)：完整架构
- [docs/case-study-overnight-monorepo.md](docs/case-study-overnight-monorepo.md)：适合公开传播的代表性案例
- [docs/use-cases.md](docs/use-cases.md)：典型使用场景
- [docs/anti-patterns.md](docs/anti-patterns.md)：常见失败模式
- [docs/design-rules.md](docs/design-rules.md)：设计规则
- [docs/faq.md](docs/faq.md)：FAQ
- [docs/why-not-agent-swarms.md](docs/why-not-agent-swarms.md)：为什么默认不走 agent swarm
- [docs/discoverability.md](docs/discoverability.md)：关键词、话题、分享角度
- [starter-kit/](starter-kit)：最小可复制起步包
- [templates/](templates)：可复用模板
- [examples/](examples)：小型示例

## 最推荐的阅读顺序

1. 看 [docs/getting-started.md](docs/getting-started.md)
2. 看 [docs/final-architecture.md](docs/final-architecture.md)
3. 看案例 [docs/case-study-overnight-monorepo.md](docs/case-study-overnight-monorepo.md)
4. 直接复制 [starter-kit/](starter-kit) 试用
5. 再根据自己的场景选 `templates` 和 `examples`

## 这个项目的差异化

它不是一个强调“更多 agent、更强编排、更炫自治”的项目。

它更像一套长期 AI 工作流的控制面设计，重点是：

- 怎么让系统真正推进工作
- 怎么让中断后还能快速恢复
- 怎么让 validator 能抓住假进展
- 怎么避免多线程协作沦为 orchestration theater

## 推荐关键词

如果你要给别人介绍这个项目，或者写 GitHub 简介、发帖文案，建议自然包含这些词：

- long-running AI workflows
- ai-workflows
- agentic-workflow
- exact continuation
- hard gates
- workflow control plane
- anti-fake-progress
- bounded autonomy
- file-backed continuity
- overnight AI execution

## 推荐的 GitHub topics

- `ai-autonomy`
- `ai-workflows`
- `agentic-workflow`
- `workflow-design`
- `agentic-systems`
- `automation`
- `operations`
- `human-in-the-loop`
- `knowledge-work`
- `context-engineering`
- `coding-agents`
- `prompt-engineering`
- `playbook`

## 这个项目不是什么

它不是：

- 万能自治系统
- 完全无监督自动化
- 多 agent 魔法框架
- 替代真实领域验证的捷径

它是一套实战型、可恢复、可审计、反假进展的长期 AI workflow playbook。

## License

[MIT](LICENSE)
