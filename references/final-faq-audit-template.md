# Final FAQ Audit Template

Use this template only after the user confirms the analysis outline.
Use this file for **商业审计增强版** output.

```md
# 《{{document_title}}》学习型 FAQ（商业审计增强版）

> 原始文档：`{{original_document_path}}`
> 实际分析对象：`{{analysis_object_path}}`
> 来源关系：{{source_relationship}}
> 提取方式：{{extraction_method}}
> 阅读目标：{{user_goal}}
> 文档类型：{{doc_type}}
> 生成模式：{{分析器 / 文档生产器}}
> 输出模式：商业审计增强版
> 输出深度：深度版
> 锚点可靠性：{{高 / 中 / 低}}
> 文本抽取质量：{{高 / 中 / 低}}
> source-chain可靠性：{{高 / 中 / 低}}

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

## 文档处理说明
- 原始任务对象：{{what_the_user_asked_to_understand}}
- 本次实际读取对象：{{analysis_object_summary}}
- 为什么采用该输入链路：{{why_this_pipeline_was_used}}
- 本次输出不应被误读为：{{what_this_output_does_not_claim}}

## 输入来源与完整性声明
- 原始文档是否直接参与分析：{{是 / 否 / 部分}}
- 实际推理主要依据：{{PDF / TXT / MD / Mixed}}
- 结构保留情况：{{high_level_structure_status}}
- 可能遗漏的内容类型：{{tables / footnotes / visuals / layout cues / none detected}}
- 必须知道的限制：
  - {{limit_1}}
  - {{limit_2}}

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

## 核心 FAQ

### 模块一：{{theme_1}}

#### Q1. {{question}}
**简短回答**
{{short_answer}}

**展开解释**
{{expanded_explanation}}

**为什么这个问题重要**
{{why_it_matters}}

**证据块**
- 原始来源：{{PDF / TXT / Mixed}}
- 锚点类型：{{章节+页码 / 页码 / 章节标题 / 文本锚点}}
- 锚点内容：{{anchor_content}}
- 证据层级：{{原文明确说明 / 原文暗示但未展开 / 综合推断 / 原文未说明 / 证据不足}}
- 可靠性：{{高 / 中 / 低}}
- 说明：{{how_the_conclusion_is_supported_or_why_it_is_limited}}

**如果继续想下去**
- {{follow_up_1}}
- {{follow_up_2}}

**进一步思考（克制版）**
{{ai_reflection}}

---

## 证据不足与风险清单
- {{risk_1}}
- {{risk_2}}
- {{risk_3}}

## 适用边界
- {{scope_1}}
- {{scope_2}}

## 不适用边界
- {{non_scope_1}}
- {{non_scope_2}}

## 审计摘要
- 最强锚点类型：{{best_anchor_type}}
- 最主要的不确定性来源：{{main_uncertainty}}
- 哪些结论最稳：{{stable_conclusions}}
- 哪些结论应保留更强怀疑：{{fragile_conclusions}}
```

## Entry rules

Each audit-enhanced entry should include:
- 问题
- 简短回答
- 展开解释
- 为什么这个问题重要
- 完整证据块
- 如果继续想下去
- 进一步思考（克制版）

**Section order rationale（章节顺序说明）：**
3分钟速读版放在最前，因为审计文档的读者（客户、上级、决策者）通常先看结论再看来源说明。文档处理说明和完整性声明紧随其后，供关心溯源的读者继续查阅。不要调换这个顺序。

Use this mode when delivery rigor matters more than compactness.
The audit reflection must stay short, restrained, and subordinate to the evidence block.
Do not hide source-chain limitations behind polished prose.
Do not invent stronger provenance than the inputs support.
Do not use 进一步思考（克制版） to add unsupported factual extensions.
