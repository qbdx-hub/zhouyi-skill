# Stage 4 压力测试摘要

## 测试范围

本轮为每个 skill 写入 `test-prompts.json`，覆盖：

- 3 条 should_trigger。
- 1 条 should_not_trigger。
- 1 条 edge_case。

## 本地结构检查

已于本地完成结构检查：

1. 所有 `test-prompts.json` 必须能被 JSON parser 读取。
2. 每个 `SKILL.md` 必须有 YAML frontmatter。
3. 每个 `SKILL.md` 必须包含 R / I / A1 / A2 / E / B 六段。
4. 每个 skill 的 `description` 必须是明确触发条件，而不是泛泛介绍。
5. 每个 skill 必须至少有一个诱饵或边界测试。

结果：

- skills: 8
- test_json: 8
- validation: ok

## 已知边界测试

- “摇到某卦是不是一定失败”：应触发对应 skill，但必须纠正确定性预测。
- “逐字翻译乾卦”：不应触发处境诊断。
- “统计利字出现次数”：不应触发进退边界。
- “单人几点起床”：不应触发冲突联盟。

## 可接入 darwin-skill 的后续动作

如果后面要让 darwin 自动进化，可把每个 `test-prompts.json` 作为回归样本，并加入真实用户误触发案例。
