# Analysis Outline Template

Use this template before generating the final FAQ. The goal is to help the user validate direction, source-chain honesty, and output mode before you draft the full document.

```md
# 《{{document_title}}》学习型 FAQ 分析提纲

## 1. 任务理解
- 原始文档路径：`{{original_document_path}}`
- 实际分析对象：`{{analysis_object_path}}`
- 来源关系：{{original / PDF抽取文本 / OCR文本 / mixed}}
- 提取方式：{{直接读取 / pdftotext / OCR / 未知}}
- 用户阅读目标：{{user_goal}}
- 系统解析目标：{{internal_goal_mapping}}

## 2. 文档初判
- 文档类型：{{doc_type}}
- 主题一句话概括：{{one_sentence_summary}}
- 阅读难度：{{低 / 中 / 高}}
- 可信度初判：{{高 / 中 / 低}}
- 判断依据：
  - {{reason_1}}
  - {{reason_2}}
  - {{reason_3}}

## 3. 结构与提取质量
- 目录保留情况：{{高 / 中 / 低}}
- 章节边界清晰度：{{高 / 中 / 低}}
- 文本抽取质量：{{高 / 中 / 低}}
- 版式损失风险：{{高 / 中 / 低}}
- 可能影响：
  - {{impact_1}}
  - {{impact_2}}

## 4. 锚点策略
- 优先引用方式：{{章节+页码 / 页码 / 章节标题 / 文本锚点}}
- 页码/章节可定位性：{{高 / 中 / 低}}
- 锚点可靠性：{{高 / 中 / 低}}
- 为什么采用该策略：
  - {{anchor_reason_1}}
  - {{anchor_reason_2}}

## 5. 推荐处理模式
- 系统推荐：{{分析器 / 文档生产器}}
- 输出模式推荐：{{标准学习版 / 商业审计增强版}}
- 推荐原因：
  - {{reason_1}}
  - {{reason_2}}
- 用户可覆盖：是

## 6. 阅读策略建议
- 先读：{{sections/pages}}
- 再读：{{sections/pages}}
- 选读：{{sections/pages}}
- 可跳读：{{sections/pages}}
- 回查重点：{{sections/pages}}

## 7. FAQ 生成规划
- 预计FAQ数量：30–50
- 重点覆盖范围：
  - {{theme_1}}
  - {{theme_2}}
  - {{theme_3}}
- 重点问题类型：
  - 理解性
  - 结构性
  - 证据性
  - 批判性
  - 迁移性

## 8. 风险与限制
- source-chain可靠性：{{高 / 中 / 低}}
- 可能限制：
  - {{limit_1}}
  - {{limit_2}}
  - {{limit_3}}
- 需要显式披露的事项：
  - {{disclosure_1}}
  - {{disclosure_2}}

## 9. 待确认
- 是否按当前结构生成完整 FAQ？
- 是否保持当前输出模式，还是切换为标准学习版 / 商业审计增强版？
- 是否需要调整重点覆盖范围？
- 是否需要提高/降低批判性、应用性或审计强度？
```

## Fill rules

- Keep the user's original goal wording where possible.
- Make the document judgment specific to the actual source chain; avoid generic filler.
- Be honest about low OCR quality, unstable page anchors, broken extraction, or fragmented structure.
- If the analysis object is TXT / MD derived from a PDF, say so explicitly.
- Treat this as a decision aid, not a teaser summary.
