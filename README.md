# Engineering Thinking · 工程认知与设计

A Chinese-language Codex skill for understanding mechanisms, diagnosing failures, and designing reliable solutions within real-world constraints. It starts with a provisional problem definition and uses feedback to revise both the solution and the problem.

**先共同界定问题，再决定需要什么工程动作。**

`engineering-thinking` 帮助你理解事物如何运作、诊断问题、设计方案，并判断什么时候应该减少或放下工程化。它以互动探究（Interaction）连接科学、设计、系统与工程思维。

## 它会做什么

| 用法 | 关注的问题 | 典型交付 |
|---|---|---|
| 认知 | 它靠什么机制运作，在哪些条件下成立？ | 结构、机制、约束与解释边界 |
| 诊断 | 差距来自哪里，有什么竞争解释？ | 证据、待检验假设与区分性检查 |
| 设计 | 怎样在现实约束下实现值得要的结果？ | 方案取舍、关键接口、责任与验证方式 |
| 演进 | 应该调整行动、模型，还是重新考虑目标？ | 最小改变、反馈与继续或停止条件 |

面对开放任务，先提出暂定理解，澄清会改变方向的分歧。明确的小任务与已有共识的续作直接推进。用户还说不清问题时，从具体情境帮助问题浮现；用户要求直接给初稿时，标明假设后交付。

它区分事实、推断、假设和未知，也区分“符合设计要求”与“真正满足需要”。只需要理解时，回答可以止于理解。

## 安装到 Codex

可以直接在 Codex 中请求：

> 使用 skill-installer 安装 https://github.com/ynhy513/engineering-thinking ，skill 位于仓库根目录，名称为 engineering-thinking。

也可以手动安装：

```sh
git clone https://github.com/ynhy513/engineering-thinking.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/engineering-thinking"
```

目标目录已存在时，先检查已有版本；不要直接覆盖本地修改。安装后在下一轮对话调用。此仓库没有必需的外部服务、API 密钥或运行时依赖；实际分析任务所需的数据与工具取决于具体任务。

## 调用示例

```text
$engineering-thinking 帮我理解冰箱如何把热量从箱内转移出去，先不做改造设计。
```

```text
$engineering-thinking 帮我设计目前的学习项目，先一起明确这次最值得解决的问题。
```

```text
$engineering-thinking 我们的周报生成更快了，但团队仍觉得没用。请诊断，暂时不要认定需要更换工具。
```

```text
$engineering-thinking 在不增加填报负担、不购买新工具的约束下，设计一个减少项目进展遗漏的办法。
```

```text
$engineering-thinking 别先问问题，直接给一版可修订初稿，并标明影响设计方向的假设。
```

## 适用边界

- 技术、产品、流程、组织和日常系统都可以借用工程视角，具体深度取决于问题和失败代价。
- 情感、审美、关系和价值选择只处理适合工程化的部分；人的体验与自主性不能被代理指标完整替代。
- 不默认把自由探索变成效率项目，不承诺控制复杂系统或保证结果。
- 调用 skill 不扩大实施权限。分析、设计与真实操作分别遵循用户授权。

## 文件

- [SKILL.md](SKILL.md)：主要指令，包含问题对齐、模式选择、建模、设计和验证。
- [references/foundations.md](references/foundations.md)：按需阅读的方法基础与建设性补充。
- [agents/openai.yaml](agents/openai.yaml)：Codex 界面名称、说明和默认调用提示。

## 版本与验证

当前版本为 **0.2.0**，增加了共同界定问题、按分歧澄清和根据反馈重新对齐的开场机制。

核心版本做过结构检查和开发场景回放，覆盖开放任务、明确任务、已有约定的续作、模糊困扰和直接给初稿等情况。公开包仅对方法参考的来源指称做了自包含整理，主要指令未改动。这些检查不等于大规模基准评估、跨领域普遍有效或长期实际效果证明。

## License

[MIT](LICENSE) · Copyright (c) 2026 ynhy513.
