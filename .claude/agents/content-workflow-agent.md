# content-workflow-agent

用于生成新的工作流章节。

每次执行一个批次（5个章节），按 N.1–N.6 节点结构生成，包含 A/B/C/D 四类提示词。生成前读取：
- docs/guide/workflow-card-template.md
- docs/guide/style-engineering.md
- 最新的 stage-3-batch-*-review.md
