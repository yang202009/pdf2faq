---
name: pdf2faq
description: Use when the user wants to deeply understand a PDF or PDF-derived text, turn a book/report into a learning FAQ, or generate a coach-style Markdown FAQ with explicit source-chain and evidence labeling.
---

# PDF Learning FAQ

Generate a **coach-style, coverage-first learning FAQ** from an original document and its actual analysis object. The default workflow is: gather `原始文档路径 + 实际分析对象路径 + 阅读目标 + 输出模式` → inspect source chain and extraction quality → produce an analysis outline → wait for confirmation → generate the final Markdown FAQ.

## Inputs

Require both:
- `原始文档路径`
- `一句阅读目标`

Strongly prefer also capturing:
- `实际分析对象路径`（可为 PDF / TXT / MD；默认等于原始文档）
- `输出模式`（默认：标准学习版）

If the user only gives one path, treat it as both 原始文档 and 实际分析对象 unless the conversation shows a PDF→TXT/OCR workflow.

If either required field is missing, ask only for the missing field.

Examples of reading goals:
- `帮我真正理解这本书的核心框架`
- `提炼可用于写作的观点，并指出哪些地方证据不足`
- `重点判断这份报告的假设、证据和商业含义`

## Supported source setups

This skill supports:
- 直接分析 PDF
- 分析从 PDF 抽取出的 TXT / MD
- mixed 模式（PDF 作为原始文档，TXT / MD 作为主要分析对象）

Always distinguish:
- `原始文档`：用户真正想分析的源文件
- `实际分析对象`：本次实际读取和推理所依据的文件

Never blur the two.

## Workflow

1. Read the original document and the actual analysis object when both are available.
2. Identify the source relationship:
   - 原始文件直读
   - 从 PDF 抽取的文本
   - OCR / 未知抽取链路
   - mixed 校对模式
3. Judge extraction quality and structure integrity:
   - title
   - table of contents
   - chapter / section headings
   - page cues
   - repeated concepts
   - layout damage / OCR noise / broken words
4. Map the reading goal to one or more internal emphases:
   - 理解型
   - 输出型
   - 应用型
   - 批判型
   - 决策型
5. Classify the document as one of:
   - 书籍
   - 行业报告
   - 研究报告
   - 方法论文档
   - 混合型
6. Choose an anchor strategy:
   - 章节 + 页码
   - 页码
   - 章节标题
   - 文本锚点 / nearby titled region
7. Judge:
   - reading difficulty
   - credibility first pass
   - page/section traceability
   - text extraction quality
   - source-chain reliability
8. Produce the **analysis outline** using `references/analysis-outline-template.md`.
9. Stop and wait for confirmation.
10. After confirmation, generate the final Markdown FAQ using:
   - `references/final-faq-template.md` for **标准学习版**
   - `references/final-faq-audit-template.md` for **商业审计增强版**
   - `references/source-integrity-rules.md` as a mandatory guardrail whenever the analysis object is derived text or anchor quality is not high

Do **not** skip the outline stage unless the user explicitly asks for one-shot generation.

## Output modes

### 标准学习版
Use when the user primarily wants understanding, writing support, or reusable learning notes.

Must still include:
- 原始文档 vs 实际分析对象
- 来源关系
- 提取方式
- 锚点可靠性
- lightweight evidence labeling
- `如果继续想下去`
- short `进一步思考`

The `进一步思考` in standard mode should:
- naturally extend the follow-up questions into deeper territory
- surface the underlying tension, tradeoff, or human meaning
- feel like the reader's own thought process continuing
- deepen inquiry without claiming to resolve it

### 商业审计增强版
Use when the output needs stronger traceability, delivery rigor, or explicit auditability.

Must additionally include:
- 文档处理说明
- 输入来源与完整性声明
- stronger evidence blocks
- risk / limitation disclosure
- scope boundaries and audit summary
- `如果继续想下去`
- short `进一步思考（克制版）`

The `进一步思考（克制版）` in audit mode should:
- be shorter and more restrained than standard mode
- never add new factual claims beyond the evidence block
- clarify tension or boundary without weakening audit rigor
- remain subordinate to evidence, not replace it

## Output rules

- Default depth: **深度版**
- Default strategy: **覆盖优先**
- Default tone: **教练式**
- Default output mode: **标准学习版**
- Prefer **pure Markdown** output
- Try to cite **章节 + 页码**, then page, then section heading, then nearby titled region, then text anchor
- Never invent references
- Never pretend TXT-derived analysis has stronger page precision than the extraction actually supports
- Clearly distinguish:
  - 原文明确说明
  - 原文暗示但未展开
  - 综合推断
  - 原文未说明
  - 证据不足
- `进一步思考` must not become motivational filler, decorative profundity, or unsupported analysis
- `进一步思考` should answer the reader's “then what does this really mean?” feeling, not drift into empty uplift

## Mode recommendation

Recommend **文档生产器** when the source chain is structurally clear, readable, and worth long-term retention.

Recommend **分析器** when OCR is weak, anchors are unstable, structure is fragmented, or a full FAQ would create fake precision.

Recommend **商业审计增强版** when the user needs delivery-grade traceability, provenance disclosure, or stronger evidence review.

The user may always override the recommendation.

## Document-specific emphasis

### If book
Prioritize:
- chapter arc
- author's worldview
- key models
- recurring principles
- chapter-to-chapter progression

### If industry report
Prioritize:
- data definitions
- assumptions
- trend logic
- business implications
- risk and bias

### If research report
Prioritize:
- claims
- evidence quality
- method transparency
- limits
- counterarguments

### If method/framework document
Prioritize:
- process steps
- model structure
- use cases
- failure modes

## Degrade honestly

If the document or extraction is messy:
- reduce precision
- prefer sections or text anchors over exact pages
- flag extraction limitations
- narrow claims instead of sounding confident
- say when the actual analysis object is a derived TXT / MD rather than the original PDF

If page references are unstable, say so explicitly instead of faking exactness.

If the actual analysis object omits visuals, tables, footnotes, or layout cues, say so explicitly.

## Mandatory provenance rules

Before final generation, make sure the output states:
- 原始文档
- 实际分析对象
- 来源关系
- 提取方式（如可判断）
- 锚点可靠性
- 文本抽取质量

If the conclusion is inferred rather than directly stated, label it as `综合推断`.

## Final self-check before generating output

- Have you clearly separated 原始文档 and 实际分析对象?
- Have you disclosed the source chain honestly?
- Are you avoiding fake page precision?
- Are you labeling inference vs explicit support?
- Are you reducing certainty when extraction quality is weak?
- Are you avoiding chapter summaries disguised as FAQs?
- Does the chosen output mode match the user's need?

## Interaction wording

Before the outline, say:

`我先给你分析提纲，确认方向后再生成完整 FAQ。也会先说明原始文档、实际分析对象和锚点可靠性。`

After the outline, say:

`如果方向对，我就按这个结构生成完整学习型 FAQ。如果要调，告诉我你想改覆盖重点、批判强度、应用/写作导向，还是切到商业审计增强版。`

## Quality bar

A good result should leave the user feeling:
- I understand what this document is really about.
- I know the most important sections and questions.
- I can tell which claims are strong, which are inferred, and which are weak.
- I can reuse this understanding in writing, learning, or decision-making.
- I understand what source chain and extraction limits shaped the result.

Avoid:
- shallow chapter summaries disguised as FAQs
- decorative “deep” language
- fake certainty
- unsupported criticism
- fake provenance
- fake citation precision

