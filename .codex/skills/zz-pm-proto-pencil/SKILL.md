---
name: zz-pm-proto-pencil
description: Pencil 原型专项技能。用于基于截图或设计稿输出 `.pen` 设计稿及配套设计说明。
intent: >-
  用于将截图、设计图或页面参考复刻为 Pencil `.pen` 设计稿，必要时同步输出结构化设计文档，适合设计评审和可视化交付。
type: workflow
metadata:
  short-description: PM Proto Pen
---

# 截图到 Pencil 设计稿

## 定位

本技能用于 `.pen` 设计稿交付，必须走 Pencil 工作流，不用 HTML 替代。

## 边界

- HTML 原型 -> `zz-pm-proto-image`
- URL 工程原型 -> `zz-pm-proto-url`
- 只做原型路径判断 -> `zz-pm-prototype-workflow`

优先使用本技能的判断标准：

- 用户明确要 `.pen` / Pencil / 设计稿交付
- 目标是设计评审、可视化规范资产或画布交付
- 不以 HTML 或工程原型为主交付物

不应停留在本技能的场景：

- 用户只要前端可预览页面 -> `zz-pm-proto-image`
- 用户要本地工程原型 -> `zz-pm-proto-url`
- 用户还没决定是否做 `.pen` -> `zz-pm-prototype-workflow`

## 适用输入

适用输入：

- 页面截图
- 设计图
- 参考页面
- `.pen` 交付要求

不适用输入：

- 只要前端可预览页面
- 明确要求本地原型工程
- 只想判断原型路线，不做具体执行

## 默认产出

默认应包含：

1. `.pen` 设计稿
2. 配套设计说明
3. 待确认项与校验结果

## 默认触发场景

- “根据这张图做 .pen”
- “按图复刻设计稿”
- “做一个 Pencil 页面”
- “输出设计图和说明”

## 执行流程

1. 明确目标尺寸与精度
2. 读取设计规范与原型规范
3. 通过 Pencil 流程生成设计稿
4. 补设计说明
5. 做截图校验

## 常见误用

- 用户要 `.pen`，却只交 HTML
- 只画页面，不补说明与待确认项
- 把 `.pen` 设计稿当作前端原型工程替代品
