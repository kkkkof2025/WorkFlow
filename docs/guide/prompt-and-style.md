# Prompt 工程与 Style 工程的关系

本文说明 Prompt 工程和 Style 工程在本项目中各自的定位，以及二者如何协同工作。

---

## 核心区别

**Style 工程** 是全书的生产规范。它回答"这本书应该长什么样"，定义了语言风格、结构规范、术语体系、禁用表达和质量标准。Style 工程是静态的——一旦冻结，全书所有内容都必须遵守。

**Prompt 工程** 是调用 Style 工程的执行工具。它回答"怎么用 AI 生产出符合 Style 工程的内容"，提供可直接复制使用的提示词，让 AI 在生成内容时自动遵守 Style 工程的要求。

二者不是重复关系：Style 工程制定标准，Prompt 工程执行标准。

---

## 协作流程

```
Style 工程（标准）
    ↓ 被引用
Prompt 工程（执行工具）
    ↓ 驱动
AI 生成内容
    ↓ 对照
Style 工程（审查）
    ↓ 不符合则
Prompt 工程（修正工具）
    ↓ 重新生成
符合 Style 工程的最终内容
```

---

## 各 Prompt 文件与 Style 工程的对应关系

| Prompt 文件 | 调用 Style 工程的哪些规范 |
|------------|------------------------|
| `workflow-generation.md` | 工作流卡结构规范、专家节点写法规范 |
| `node-prompt-generation.md` | 提示词写法规范、多提示词层级规范 |
| `chapter-generation.md` | 内容密度要求、行业差异化写法 |
| `style-review.md` | 禁用表达、AI 味识别规则、风格自检清单 |
| `quality-check.md` | 质量评分规则、内容硬性禁止项 |
| `final-polish.md` | 术语统一表、推荐表达、禁用词替换 |

---

## 使用顺序

生产一张工作流卡时，按以下顺序使用 Prompt 文件：

1. `workflow-generation.md` → 生成工作流卡初稿
2. `node-prompt-generation.md` → 补充或优化各节点的 4 类提示词
3. `style-review.md` → 审查风格是否符合 Style 工程
4. `quality-check.md` → 评分，确认是否达到 80 分合格线
5. `final-polish.md` → 最终统一润色

---

## 修改原则

- **修改 Style 工程**：必须在第二阶段标准冻结前完成。冻结后不允许修改核心规范，只允许补充边缘情况说明。
- **修改 Prompt 工程**：可以随时优化，但每次修改后需要对至少一个已有样章重新跑一遍，确认修改有效。
- **不允许的操作**：用 Prompt 工程的局部变通绕过 Style 工程的核心规范。
