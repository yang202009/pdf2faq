# Final FAQ Template

Use this template only after the user confirms the analysis outline.
Use this file for **标准学习版** output.

```md
# 《{{document_title}}》学习型 FAQ

> 原始文档：`{{original_document_path}}`
> 实际分析对象：`{{analysis_object_path}}`
> 来源关系：{{source_relationship}}
> 提取方式：{{extraction_method}}
> 阅读目标：{{user_goal}}
> 文档类型：{{doc_type}}
> 生成模式：{{分析器 / 文档生产器}}
> 输出模式：标准学习版
> 输出深度：深度版
> 锚点可靠性：{{高 / 中 / 低}}
> 文本抽取质量：{{高 / 中 / 低}}

---

## 3 分钟速读版

### 这份文档在讲什么
{{3-5 sentence overview}}

### 最重要的 3-5 个结论
- {{takeaway_1}}
- {{takeaway_2}}
- {{takeaway_3}}
- {{takeaway_4}}
- {{takeaway_5}}

### 最值得记住的一个框架
{{key_framework}}

### 这份文档最大的局限
{{main_limitation}}

### 带着什么问题继续读
- {{guiding_question_1}}
- {{guiding_question_2}}
- {{guiding_question_3}}

---

## 阅读诊断
- **文档类型**：{{doc_type}}
- **阅读难度**：{{低 / 中 / 高}}
- **可信度初判**：{{高 / 中 / 低}}
- **最值得优先读的部分**：{{priority_sections}}
- **推荐阅读策略**：{{reading_strategy}}

### 判断依据
- {{evidence_1}}
- {{evidence_2}}
- {{evidence_3}}

---

## 阅读路线图
### 先读
- {{must_read_1}}
- {{must_read_2}}

### 再读
- {{then_read_1}}
- {{then_read_2}}

### 选读
- {{optional_read_1}}
- {{optional_read_2}}

### 可跳读
- {{skippable_1}}
- {{skippable_2}}

### 回查重点
- {{revisit_point_1}}
- {{revisit_point_2}}

---

## 核心 FAQ

### 模块一：{{theme_1}}

#### Q1. {{question}}
**简短回答**
{{short_answer}}

**展开解释**
{{expanded_explanation}}

**为什么这个问题重要**
{{why_it_matters}}

**依据**
- 来源类型：{{PDF / TXT / Mixed}}
- 定位：{{章节+页码 / 页码 / 章节标题 / 文本锚点}}
- 证据层级：{{原文明确说明 / 原文暗示但未展开 / 综合推断 / 原文未说明 / 证据不足}}

**如果继续想下去**
- {{follow_up_1}}
- {{follow_up_2}}

**进一步思考**
{{ai_reflection}}

---

## 概念拆解

列出文档中 3–8 个核心概念，每个概念包含：
- **概念名称**
- **原文定义或最接近的描述**（附锚点和证据层级）
- **与常见误解的区别**（如有；标注"综合推断"若非原文明确说明）
- **一句话记忆版**（用自己的语言，不是摘抄）

不要把所有术语都列进来，只列真正影响理解整本书/报告的核心概念。

---

## 论证审查

针对文档中 2–4 个核心主张，逐一分析：
- **主张内容**（尽量用原文措辞，附锚点）
- **支撑证据**（附锚点和证据层级标注）
- **证据强度**：强 / 中 / 弱，并说明理由
- **潜在反驳或局限**（标注"综合推断"若非原文承认）

如果文档本身没有对核心主张做充分论证，在此处明确指出，不要替作者补充论证。

---

## 应用迁移

列出 2–3 个场景，说明文档中的框架或结论可以如何实际应用：
- **场景描述**：谁在什么情况下可以用
- **适用的核心概念或方法**（附锚点）
- **需要注意的前提条件**：这个应用在什么情况下会失效

不要给出泛泛的"可以用来提升效率"之类的表述；要具体到行动层面。

---

## 反向提问

列出 3–5 个文档没有回答、但读完后自然产生的问题。

这些问题应当：
- 指向文档的边界、假设或未验证的推论
- 对读者有实际的思考价值
- 不是简单重复文档内容的变体

不要把"作者为什么这么说"当作反向提问，那是论证审查的内容。

---

## 未说明 / 证据不足清单

分三类列出：

**1. 文档声称但证据不足的结论**
- {{claim}} — 锚点：{{anchor}} — 标注：证据不足
- 说明为什么认为证据不足

**2. 文档完全没有说明、但读者可能期待的内容**
- {{expected_content_1}}
- {{expected_content_2}}

**3. 受限于提取质量无法判断的内容**
- {{uncertain_item}} — 标注：提取限制
- 说明是什么原因导致无法判断（OCR损坏 / 图表丢失 / 页面缺失等）

如果三类都不存在，可以写"未发现明显证据不足项"，但不要省略这个章节。

---

## 一句话总结

一句话，说清楚：**这份文档对[目标读者]最大的价值是什么。**

不是摘要，是价值判断。格式参考：
> 对于[目标读者]，这份文档最大的价值是[具体价值]，前提是[使用前提或局限]。
```

## Entry rules

Each FAQ entry should include:
- 问题
- 简短回答
- 展开解释
- 为什么这个问题重要
- 依据
- 如果继续想下去
- 进一步思考

Standard mode should stay readable, but it must still disclose provenance, anchor limits, and evidence level.
The 进一步思考 should naturally extend inquiry, surface real tensions or tradeoffs, and avoid vague uplift.

Do not turn chapter summaries into shallow questions.
Do not pretend the analysis object has stronger citation precision than it actually supports.
Do not use 进一步思考 to introduce unsupported new claims.
Do not leave 概念拆解、论证审查、应用迁移、反向提问、未说明/证据不足清单、一句话总结 empty — each section has fill rules above and must be completed.
