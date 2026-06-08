# AI 工作流图鉴

> 不是提示词大全，而是把真实工作拆解成可执行、可交接、可验收的 AI 多专家工作流。

[![GitHub Pages](https://img.shields.io/badge/Demo-GitHub%20Pages-blue)](https://kkkkof2025.github.io/WorkFlow/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Unity2.ai VibeCoding](https://img.shields.io/badge/Unity2.ai-VibeCoding%20B-orange)](https://unity2.ai)

## 一句话介绍

本项目是面向真实职场人的 **AI 工作流图鉴**，收录 30 个岗位级多专家 AI 协作流程，每个流程可执行、可交接、可验收。

---

## 项目背景

AI 工具已经足够好用，但大多数职场人仍然停留在"一个问题一条提示词"的阶段。他们缺少的不是更多提示词，而是一套系统方法：**如何把一项真实工作，拆解成多个 AI 专家节点，协同完成一整套任务。**

本项目从 30 个真实岗位出发，为每个岗位设计一张**工作流卡**，帮助用户把复杂工作变成可执行、可交接、可验收的 AI 协作流程。

---

## 本项目不是什么

- ❌ AI 基础教程
- ❌ 提示词大全
- ❌ 单条 Prompt 合集
- ❌ 旧项目换壳
- ❌ 静态 Markdown 堆砌
- ❌ "一个提示词一个案例"的碎片合集

---

## 本项目是什么

- ✅ 岗位级 AI 工作流图鉴
- ✅ 多专家协作流程手册
- ✅ 可发布的 MkDocs 电子书
- ✅ 可扩展的内容生产工程
- ✅ 带 Style 工程和质量检查机制的内容系统

---

## 什么是工作流卡

**工作流卡**是本项目的核心内容单元。每张卡代表一个真实岗位或真实任务，通过多个 AI 专家节点完成一整套工作。

每张工作流卡包含：

1. 工作流名称与适用岗位
2. 真实场景与最终目标
3. 需要准备的输入材料
4. 工作流总览（流程图文字版）
5. 专家节点设计（5～10 个节点）
6. 每个节点的职责、输入、输出、提示词、验收标准
7. 节点之间的交接方式
8. 最终输出模板
9. 常见错误
10. 人工验收清单
11. 延伸玩法

---

## 什么是多专家节点

一个工作流由多个"专家节点"组成，每个节点代表一个特定角色的 AI。节点之间有明确的输入输出交接，不是孤立的 Prompt，而是协同工作的流水线。

**示例：短视频内容创作工作流的专家节点**

```
选题判断专家 → 故事选取专家 → 故事扩写专家 → 脚本生成专家
→ 分镜设计专家 → 图像生成提示词专家 → 视频生成提示词专家
→ 配音文案专家 → 字幕包装专家 → 发布复盘专家
```

---

## 为什么每个专家节点要有多条提示词

每个专家节点提供 4 类提示词：

| 类型 | 用途 |
|------|------|
| 基础提示词 | 给普通用户直接复制使用 |
| 进阶提示词 | 用于更复杂、更专业的场景 |
| 审查提示词 | 检查 AI 输出是否有问题 |
| 修正提示词 | 根据审查结果进行二次修改 |

这四条提示词构成一个完整的"生产—审查—修正"闭环，而不是单次调用。

---

## 核心功能

- 30 个岗位级 AI 工作流卡
- 每个工作流含 5～10 个专家节点
- 每个节点含 4 类提示词（基础/进阶/审查/修正）
- 清晰的节点交接协议
- 人工验收清单
- Style 工程规范（统一写作标准）
- Prompt 工程文件（可直接复用的生产工具）
- MkDocs + GitHub Pages 发布

---

## 内容结构

```
第一章  内容创作（短视频、短剧、图文）
第二章  视频与图像生产（分镜、图像、Logo、音乐）
第三章  项目与工程（项目管理、程序开发、安全审查）
第四章  办公效率（汇报、会议、周报、数据分析）
第五章  教育与学习（教师备课、学生学习）
第六章  职能支持（人事、财务、法务、客服、销售）
第七章  知识管理（群聊沉淀、评论分析、个人复盘）
第八章  开源与发布（GitHub、MkDocs 发布工作流）
```

---

## 技术栈

- **内容格式**：Markdown
- **发布系统**：MkDocs + Material for MkDocs
- **部署平台**：GitHub Pages
- **自动化**：GitHub Actions
- **内容标准**：Style 工程规范 + Prompt 工程文件

---

## 本地运行

```bash
# 安装依赖
pip install -r requirements.txt

# 本地预览
mkdocs serve

# 构建静态文件
mkdocs build --strict
```

---

## GitHub Pages 发布

推送到 `main` 分支后，GitHub Actions 自动构建并发布到：

```
https://kkkkof2025.github.io/WorkFlow/
```

也可在 Actions 页面手动触发 `workflow_dispatch`。

---

## 项目目录结构

```
WorkFlow/
├── mkdocs.yml                    # MkDocs 配置
├── requirements.txt              # Python 依赖
├── README.md                     # 项目介绍
├── TODO.md                       # 阶段计划
├── .github/
│   └── workflows/
│       └── deploy.yml            # GitHub Pages 自动部署
├── docs/
│   ├── index.md                  # 首页
│   ├── guide/
│   │   ├── what-is-workflow-card.md
│   │   ├── style-engineering.md  # Style 工程规范
│   │   └── workflow-card-template.md
│   └── chapters/
│       ├── 00-workflow-map.md    # 30 个工作流总览
│       ├── 01-content-creator.md # 黄金样章 1
│       ├── 02-project-management.md # 黄金样章 2
│       └── 03-union-activity.md  # 黄金样章 3
├── prompts/
│   ├── book-planning.md
│   ├── workflow-generation.md
│   ├── chapter-generation.md
│   ├── node-prompt-generation.md
│   ├── style-review.md
│   ├── quality-check.md
│   └── final-polish.md
└── data/
    ├── workflows.yaml            # 30 个工作流规划
    └── expert-nodes.yaml         # 专家节点库
```

---

## 原创性说明

本项目所有工作流卡、专家节点设计、提示词体系、Style 工程规范均为本次参赛原创内容，从零构建，不复用任何旧项目内容，不做旧项目换壳。

---

## Unity2.ai VibeCoding 参赛说明

- **赛道**：B：内容与数据
- **项目类型**：MkDocs 电子书 + AI 工作流知识系统
- **核心创新**：岗位级多专家 AI 工作流卡架构，将复杂工作拆解为可执行、可交接、可验收的节点流程
- **技术亮点**：Style 工程 + Prompt 工程双轨内容生产体系，GitHub Actions 全自动部署

---

## 当前进度

| 内容 | 状态 |
|------|------|
| 项目骨架 | ✅ 已完成 |
| Style 工程 | ✅ 已完成 |
| 工作流卡模板 | ✅ 已完成 |
| 黄金样章（01, 02, 03） | ✅ 已完成 |
| 批次 A：内容创作类（04-06） | ✅ 已完成 |
| 批次 B：视觉与音乐类（07-10） | ✅ 已完成 |
| 批次 C：项目与工程类（11-15） | ✅ 已完成 |
| 批次 D：办公效率类（16-20） | ✅ 已完成 |
| 批次 E：职能支持类（21-25） | ❌ 未开始 |
| 批次 F：知识管理类（26-30） | ❌ 未开始 |

**已完成章节：20 个工作流（01-20）**

## 本地继续开发

1. 新会话先读取 `CLAUDE.md`、`PROJECT_STATE.md`、`TASKS.md`
2. 每个批次结束后运行 `py -3 -m mkdocs build --strict`
3. 每个批次都更新对应 `stage-3-batch-*-review.md`
4. 建议一个批次一个新 Claude Code 会话，避免上下文溢出

## 后续计划

- [ ] 批次 E：职能支持类（21-25）
- [ ] 批次 F：知识管理类（26-30）
- [ ] 第四阶段：MkDocs 展示优化
- [ ] 第五阶段：参赛交付（Demo、视频、提交材料）
