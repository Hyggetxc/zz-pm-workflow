---
name: zz-pm-proto-image
description: 截图原型专项技能。用于基于截图、设计稿或 mockup 输出高保真 HTML 原型。
intent: >-
  用于将界面截图、线框图或设计稿复刻为可预览、可继续编辑的 HTML 原型，优先保证结构、视觉和交互还原。
type: workflow
metadata:
  short-description: PM Proto Image
---

# 截图到 HTML 原型

**EN Summary:** Recreates screenshots and mockups as editable HTML prototypes with key interactions and states.

## 定位

本技能用于把截图复刻成 HTML 原型，不负责 `.pen` 设计稿交付。

## 边界

- URL 原型工程 -> `zz-pm-proto-url`
- `.pen` 设计稿 -> `zz-pm-proto-pencil`
- 只做原型路径判断 -> `zz-pm-prototype-workflow`

优先使用本技能的判断标准：

- 主要输入是截图、设计图或标注图
- 目标是快速输出可预览的页面原型
- 默认交付是 HTML 或轻量前端页面，而不是完整工程

不应停留在本技能的场景：

- 用户明确要求“做成本地工程 / Next.js 原型项目” -> `zz-pm-proto-url`
- 用户明确要求 `.pen` 设计稿或设计评审画板 -> `zz-pm-proto-pencil`
- 用户只是要判断原型该走哪条链路 -> `zz-pm-prototype-workflow`

## 适用输入

适用输入：

- 页面截图
- 设计稿或 mockup
- 标注图
- 页面结构要求

不适用输入：

- 只有 URL，且目标是本地工程
- 明确要求 `.pen` / Pencil 设计稿
- 只想判断原型路线，不做具体执行

## 默认产出

默认应包含：

1. 可预览的 HTML 原型
2. 关键交互与状态补充
3. 待确认项标注

## 默认触发场景

- “照这个图做页面”
- “根据截图出 HTML”
- “把这个界面画出来”
- “复刻这个弹窗 / 表单 / 列表”

## 执行流程

1. 解析截图结构、组件和状态
2. 读取 `DESIGN.md` 与项目原型规范
3. 输出 HTML 原型
4. 补必要交互与状态
5. 标注待确认项

## 常见误用

- 把截图复刻直接做成 `.pen`
- 只还原静态外观，不补交互和状态
- 用户明确要求工程化交付，却只给单文件 HTML
