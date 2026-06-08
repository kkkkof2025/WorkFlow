# TASKS.md — 当前任务队列

## 当前状态

- **当前阶段**：第三阶段正式内容生产
- **当前批次**：批次 E（职能支持类）
- **当前任务**：生成工作流 21-25
- **是否可继续**：是
- **是否需要新会话**：建议新会话开始，避免上下文积累过多

---

## 立即任务（批次 E）

- [ ] 生成 docs/chapters/21-hr-recruitment.md
- [ ] 生成 docs/chapters/22-sales-follow-up.md
- [ ] 生成 docs/chapters/23-customer-service.md
- [ ] 生成 docs/chapters/24-finance-reimbursement.md
- [ ] 生成 docs/chapters/25-legal-contract-review.md
- [ ] 新增 docs/guide/stage-3-batch-e-review.md
- [ ] 更新 mkdocs.yml（新增"职能支持"导航节）
- [ ] 更新 docs/chapters/00-workflow-map.md
- [ ] 更新 data/workflows.yaml
- [ ] 更新 TODO.md
- [ ] 运行 `py -3 -m mkdocs build --strict`
- [ ] 提交并 push

---

## 批次 E 内容边界（必须遵守）

| 工作流 | 禁止事项 |
|--------|---------|
| 21 HR 招聘 | 禁止基于年龄、性别、婚育、地域、民族等不当因素筛选；所有筛选必须围绕岗位能力、经验、项目证据和匹配度 |
| 22 销售跟进 | 不得夸大承诺、制造虚假稀缺、诱导欺骗 |
| 23 客服沟通 | 不得推责、冷漠、机械套话、过度承诺、在未核实前下结论 |
| 24 财务报销 | 不得编造票据信息；无法确认的内容标注"需人工核实" |
| 25 法务合同初审 | 必须声明"仅作初步辅助，不构成法律意见"；高风险条款必须建议咨询律师 |

---

## 批次 E 之后（批次 F）

批次 F 待批次 E 完成后再启动：

- [ ] 生成 docs/chapters/26-xx.md（待定）
- [ ] 生成 docs/chapters/27-xx.md
- [ ] 生成 docs/chapters/28-xx.md
- [ ] 生成 docs/chapters/29-xx.md
- [ ] 生成 docs/chapters/30-xx.md
- [ ] 新增 docs/guide/stage-3-batch-f-review.md

---

## 后续阶段

### 第四阶段：MkDocs 展示优化
- [ ] 优化首页 docs/index.md
- [ ] 优化导航结构
- [ ] 修复所有内部链接
- [ ] 优化移动端阅读体验

### 第五阶段：参赛交付
- [ ] 完善 README（补充截图和 Demo 链接）
- [ ] 确认 GitHub Pages Demo 可访问
- [ ] 录制演示视频（3 分钟以内）
- [ ] 准备提交材料
- [ ] 检查原创性说明
