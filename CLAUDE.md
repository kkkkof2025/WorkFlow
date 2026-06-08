# CLAUDE.md — AI 工作流图鉴 项目记忆

## 项目身份

- **项目名**：AI 工作流图鉴：30 个真实岗位的多专家协作方法
- **仓库**：kkkkof2025/WorkFlow
- **本地路径**：E:\c\github\WorkFlow
- **发布地址**：https://kkkkof2025.github.io/WorkFlow/
- **发布形式**：MkDocs + Material for MkDocs + GitHub Pages
- **参赛赛道**：Unity2.ai VibeCoding 挑战赛 B：内容与数据
- **项目定位**：不是提示词大全，而是 30 个真实岗位的多专家 AI 工作流图鉴

---

## 核心内容结构

每个工作流章节必须包含：
1. 工作流名称 / 适用岗位 / 真实场景 / 最终目标
2. 输入材料清单
3. 工作流总览（流程图）
4. 专家节点详解（每节点用 N.1–N.6 结构）
5. 节点交接表
6. 最终输出模板
7. 常见错误
8. 人工验收清单
9. 延伸玩法

每个专家节点必须用六节结构：
- **N.1 节点定位**
- **N.2 输入与输出**
- **N.3 使用顺序**
- **N.4 提示词包**（A 快速生成版 / B 专家增强版 / C 自查审稿版 / D 返修优化版）
- **N.5 交付给下游节点**
- **N.6 人工验收清单**

**重要**：C 自查审稿版和 D 返修优化版是当前节点内部工作模式，不是新专家角色。人工验收清单是用户确认步骤，不是 AI 角色。

---

## 已完成批次（截至 2026-06-08）

| 阶段 | 内容 | 状态 |
|------|------|------|
| 第一阶段 | 项目骨架、MkDocs、Style 工程、工作流卡模板 | ✅ 已完成 |
| 第二阶段 | 标准冻结、黄金样章、节点结构统一 | ✅ 已完成 |
| 批次 A | 内容创作类（04, 05, 06） | ✅ 已完成 |
| 批次 B | 视觉与音乐类（07, 08, 09, 10） | ✅ 已完成 |
| 批次 C | 项目与工程类（11, 12, 13, 14, 15） | ✅ 已完成 |
| 批次 D | 办公效率与信息整理类（16, 17, 18, 19, 20） | ✅ 已完成 |
| 批次 E | 职能支持类（21, 22, 23, 24, 25） | ❌ 未开始 |
| 批次 F | 教育学习与个人知识管理类（26-30） | ❌ 未开始 |

黄金样章：01（短视频创作）、02（项目管理）、03（工会活动）均已完成。

---

## 下一步任务

**继续第三阶段批次 E：职能支持类工作流**

| 编号 | 文件 | 招牌节点 | 特殊约束 |
|------|------|---------|---------|
| 21 | docs/chapters/21-hr-recruitment.md | 简历筛选标准专家 | 禁止基于年龄/性别/婚育/地域/民族筛选 |
| 22 | docs/chapters/22-sales-follow-up.md | 异议处理专家 | 不得夸大承诺、虚假稀缺、诱导欺骗 |
| 23 | docs/chapters/23-customer-service.md | 用户情绪识别专家 | 不得推责、冷漠、机械套话、过度承诺 |
| 24 | docs/chapters/24-finance-reimbursement.md | 异常票据识别专家 | 不得编造票据信息，不确定项标注"需人工核实" |
| 25 | docs/chapters/25-legal-contract-review.md | 风险条款标记专家 | 必须声明"非法律意见，仅作初步辅助" |

批次 E 完成后还需：
- 新增 docs/guide/stage-3-batch-e-review.md
- 更新 mkdocs.yml（新增"职能支持"导航节）
- 更新 docs/chapters/00-workflow-map.md
- 更新 data/workflows.yaml
- 更新 TODO.md
- 运行 `py -3 -m mkdocs build --strict`

---

## 重要规则

- 不要重写已完成章节
- 不要一次性生成所有剩余工作流，每次一个批次
- 每个批次完成后必须运行构建验证
- 技术/安全/法务类内容必须保守、合规、边界清楚
- 不要编造事实、数据、简历、票据、合同内容或会议结论
- 如果上下文接近满，先写入 PROJECT_STATE.md，再建议用户开启新会话

---

## 常用命令

```bash
py -3 -m mkdocs build --strict
py -3 -m mkdocs serve
git status
git add .
git commit -m "..."
git push
```

---

## 新会话启动清单

新会话应先读取：
1. CLAUDE.md（本文件）
2. PROJECT_STATE.md
3. TASKS.md
4. TODO.md
5. mkdocs.yml
6. data/workflows.yaml
7. docs/chapters/00-workflow-map.md
8. docs/guide/workflow-card-template.md
9. docs/guide/style-engineering.md
10. docs/guide/quality-standard.md
11. docs/guide/prompt-and-style.md
12. 最新的 docs/guide/stage-3-batch-*-review.md
