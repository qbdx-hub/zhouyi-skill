# 周易 Skill

一套使用 [Cangjie Skill](https://github.com/kangarooking/cangjie-skill) 流程蒸馏出来的 AI skill 工具包。

它不是原书摘要，也不是读后感，而是把书中可复用的方法论拆成可触发、可执行、可测试的 skill 模块。

## 这套 skill 解决什么问题

把《周易》中关于处境、时位、进退、谦抑、风险语言和修复周期的判断，拆成可用于复杂局面诊断的 AI skills。

你可以把它理解成一组“读完书之后真正能调用的能力”：

- 遇到真实问题时，先判断是否触发某个 skill
- 进入 skill 后，按步骤拆解处境、约束、风险和下一步动作
- 用 `test-prompts.json` 检查触发边界，避免把书里的概念泛化滥用

## 蒸馏来源

- 来源：《周易》
- Skill 数量：8
- 生成方式：Cangjie Skill / book2skill 流程

## 仓库内容

- `BOOK_OVERVIEW.md`：整书理解和方法论总览
- `INDEX.md`：skill 地图和调用关系
- `verified.md`：验证记录
- `candidates/`：候选框架、原则、案例、反例和术语
- `*/SKILL.md`：可独立调用的 skill
- `*/test-prompts.json`：触发测试和边界测试提示

说明：本仓库只发布蒸馏后的 skill、索引、候选材料和测试提示，不包含原书 PDF、EPUB、OCR 文件、截图或全文源文本。

## Skills

- `advance-retreat-boundary`
- `auspicious-risk-language`
- `conflict-coalition-diagnosis`
- `hexagram-situation-diagnosis`
- `humility-overreach-check`
- `line-position-timing`
- `repair-renewal-cycle`
- `scale-and-restraint-control`

## 怎么使用

1. 选择你需要的 skill 目录，例如 `advance-retreat-boundary`。
2. 把该目录复制到 Codex/Agent 的 skills 目录，或在支持 skill 的环境中按路径引用。
3. 提问时触发对应场景，Agent 会按 `SKILL.md` 中的流程执行，而不是只给你一句抽象总结。
4. 如果不确定该用哪个 skill，先读 `INDEX.md`。

## 与 Cangjie Skill 的关系

这个仓库是 [Cangjie Skill](https://github.com/kangarooking/cangjie-skill) 的输出示例之一。

Cangjie Skill 的目标不是把书变短，而是把书中可迁移的方法论变成 Agent 能调用的能力。

## License

MIT。