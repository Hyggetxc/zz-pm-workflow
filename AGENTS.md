# zz-pm-workflow Sandbox Rules

适用范围：`<workspace>/zz-pm-workflow`

## 技能路由

- 所有产品任务默认先走 `.codex/skills/zz-pm-workflow/SKILL.md`
- 涉及 PRD、正式文档、按目录出文档时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-prd/SKILL.md`
- 涉及 `proposal.md`、`spec.md`、`design.md`、`tasks.md`、研发交付包、需求变更后的交付文档更新时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-delivery-pack/SKILL.md`
- 涉及原型、截图复刻、URL 复刻、`.pen` 设计稿时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-prototype-workflow/SKILL.md`
- 涉及评审、review、查漏补缺、过会前检查时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-review-board/SKILL.md`
- 涉及埋点、tracking、事件字段设计、指标口径、QA 验收时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-tracking-spec/SKILL.md`
- 涉及 A/B 测试、实验设计、灰度方案、样本量估算、判定标准时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-experiment/SKILL.md`
- 涉及复盘、postmortem、RCA、上线回顾、行动项沉淀时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-postmortem/SKILL.md`
- 涉及优先级、RICE、ICE、Kano、取舍建议时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-prioritization/SKILL.md`
- 涉及 roadmap、版本规划、里程碑、依赖梳理时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-roadmap/SKILL.md`
- 涉及数据分析、漏斗、留存、分群、指标异常时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-analytics/SKILL.md`
- 涉及竞品分析、对标、差异化时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-competitor/SKILL.md`
- 涉及问卷设计、survey、NPS、满意度调研时，由 `zz-pm-workflow` 路由到 `.codex/skills/zz-pm-survey/SKILL.md`
- 若任务需要本地 Word 文档交付，默认 `docx` 作为输出工具链，`zz-pm-prd` 作为内容规则来源

## 验证目标

- 当前目录用于验证新的产品技能分层结构
- 先验证 `主技能 -> 子技能` 的职责边界
- 暂不回写其他现有项目工作流
