---
name: zz-pm-prototype-workflow
description: 原型总控技能。用于判断当前原型任务应走截图复刻、URL 复刻、.pen 设计稿还是通用页面结构规划流程。
intent: >-
  用于承接原型相关任务的总控判断，先识别输入来源与交付类型，再路由到 HTML 原型、Next.js 原型或 Pencil 设计稿等专项技能。
type: workflow
metadata:
  short-description: PM Proto Flow
---

# 原型工作流

**EN Summary:** Main orchestrator for routing prototype requests to image, URL, or Pencil delivery paths.

本技能用于原型任务总控，不直接替代具体原型执行技能。

## 工作目标

先判断：

1. 输入来源是什么
2. 目标交付物是什么
3. 当前应走哪个原型子技能

## 默认触发场景

- “帮我做个原型”
- “照这个页面复刻一下”
- “根据截图出 HTML”
- “根据 URL 出本地原型”
- “根据这张图做 .pen 设计稿”

## 路由规则

- 截图 / 设计稿 / mockup -> `zz-pm-proto-image`
- URL / 在线页面 / 网站参考 -> `zz-pm-proto-url`
- 明确要求 `.pen` / Pencil / 设计稿交付 -> `zz-pm-proto-pencil`

优先使用本技能的判断标准：

- 用户提的是“原型怎么做”，而不是直接指定产出链路
- 输入形式和交付形式还没完全定下来
- 需要先判断应走 HTML、工程原型还是 `.pen`

若用户只说“先出页面结构 / 原型粒度 / 页面状态”，且没有明确截图、URL 或 `.pen` 目标，则停留在本技能，输出原型路径判断和下一步建议。

不应停留在本技能的场景：

- 已明确给出截图，并要求快速复刻页面 -> `zz-pm-proto-image`
- 已明确给出 URL，并要求本地工程化复刻 -> `zz-pm-proto-url`
- 已明确要求 `.pen` 设计稿 -> `zz-pm-proto-pencil`

## 读取优先级

若项目内存在，优先读取：

1. `docs/*SOP*.md`
2. `DESIGN.md`
3. `docs/*设计规范*.md`
4. `docs/*原型规范*.md`
5. 截图 / URL / 现有原型文件

## 标准输出格式

```markdown
## 当前判断
- 输入来源：
- 目标交付物：
- 是否需要切子技能：

## 应先读取
- 文档 / 规范：

## 下一步动作
- ...
```
