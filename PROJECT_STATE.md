# PROJECT_STATE.md — 当前项目真实进度

> 最后更新：2026-06-08
> 此文件记录项目真实状态，优先于 TODO.md 和 README 中的进度描述。

---

## 项目概览

- **项目名**：AI 工作流图鉴：30 个真实岗位的多专家协作方法
- **仓库路径**：E:\c\github\WorkFlow
- **GitHub**：https://github.com/kkkkof2025/WorkFlow
- **发布地址**：https://kkkkof2025.github.io/WorkFlow/
- **发布方式**：GitHub Actions 自动部署（push 到 main 分支后触发），`.github/workflows/deploy.yml`
- **构建工具**：MkDocs + Material for MkDocs，命令：`py -3 -m mkdocs build --strict`

---

## 已完成章节清单

### 第一阶段（项目骨架）
- mkdocs.yml
- requirements.txt
- .github/workflows/deploy.yml
- data/workflows.yaml
- data/expert-nodes.yaml
- docs/index.md
- docs/chapters/00-workflow-map.md

### Style 工程与指南
- docs/guide/style-engineering.md
- docs/guide/quality-standard.md
- docs/guide/prompt-and-style.md
- docs/guide/workflow-card-template.md
- docs/prompts/（7 个文件）

### 黄金样章
- docs/chapters/01-content-creator.md ✅
- docs/chapters/02-project-management.md ✅
- docs/chapters/03-union-activity.md ✅

### 批次 A（内容创作类）
- docs/chapters/04-short-drama-planning.md ✅
- docs/chapters/05-character-design.md ✅
- docs/chapters/06-video-storyboard.md ✅
- docs/guide/stage-3-batch-a-review.md ✅

### 批次 B（视觉与音乐类）
- docs/chapters/07-image-generation.md ✅
- docs/chapters/08-ai-video-generation.md ✅
- docs/chapters/09-logo-design.md ✅
- docs/chapters/10-music-creation.md ✅
- docs/guide/stage-3-batch-b-review.md ✅

### 批次 C（项目与工程类）
- docs/chapters/11-program-development.md ✅
- docs/chapters/12-agent-collaboration.md ✅
- docs/chapters/13-security-review.md ✅（纯防御性，无进攻性内容）
- docs/chapters/14-github-publishing.md ✅
- docs/chapters/15-mkdocs-publishing.md ✅
- docs/guide/stage-3-batch-c-review.md ✅

### 批次 D（办公效率与信息整理类）
- docs/chapters/16-meeting-minutes.md ✅
- docs/chapters/17-leadership-reporting.md ✅
- docs/chapters/18-data-analysis-report.md ✅
- docs/chapters/19-group-chat-knowledge.md ✅
- docs/chapters/20-comment-opinion-analysis.md ✅
- docs/guide/stage-3-batch-d-review.md ✅

### 批次 E（职能支持类）
- docs/chapters/21-hr-recruitment.md ✅
- docs/chapters/22-sales-follow-up.md ✅
- docs/chapters/23-customer-service.md ✅
- docs/chapters/24-finance-reimbursement.md ✅
- docs/chapters/25-legal-contract-review.md ✅
- docs/guide/stage-3-batch-e-review.md ✅

### 批次 F（教育学习与知识管理类）
- docs/chapters/26-teacher-lesson-prep.md ✅
- docs/chapters/27-student-learning.md ✅
- docs/chapters/28-personal-knowledge.md ✅
- docs/chapters/29-personal-review.md ✅
- docs/chapters/30-personal-task-management.md ✅
- docs/guide/stage-3-batch-f-review.md ✅

---

## 当前状态

- **当前阶段**：第三阶段正式内容生产（30个工作流全部完成）
- **当前批次**：批次 F 已完成，30 个工作流全部生成
- **批次 F 状态**：✅ 已完成，构建通过
- **已完成章节数**：30 个工作流章节（01-30）+ 3 个黄金样章

---

## 当前不应该做的事

- ❌ 不要继续生产批次 F（26-30）
- ❌ 不要重写批次 A-D 任何已完成章节
- ❌ 不要一次性生成所有剩余工作流
- ❌ 不要在上下文不稳定时批量生产内容

---

## 下一会话启动指令

新会话应先读取以下文件（按顺序）：
1. CLAUDE.md
2. PROJECT_STATE.md（本文件）
3. TASKS.md
4. TODO.md
5. mkdocs.yml
6. data/workflows.yaml
7. docs/chapters/00-workflow-map.md
8. docs/guide/workflow-card-template.md
9. docs/guide/style-engineering.md
10. docs/guide/quality-standard.md
11. docs/guide/stage-3-batch-e-review.md（最新完成的 review）

**第一条任务**：规划并开始生成批次 F（26-30），先确认 5 个工作流的主题后再开始生产。

---

## 构建命令

```bash
py -3 -m mkdocs build --strict   # 必须 0 warnings 0 errors
py -3 -m mkdocs serve             # 本地预览
```

## Git 提交建议

```bash
git add .
git commit -m "batch-e: add workflows 21-25 (职能支持类)"
git push
```
