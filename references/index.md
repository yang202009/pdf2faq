# References Index

This directory contains all template and guardrail files used by the pdf2faq skill.

## Files

| 文件                           | 何时加载                                                     |
| ------------------------------ | ------------------------------------------------------------ |
| `analysis-outline-template.md` | 工作流第 8 步：生成分析提纲时                                |
| `final-faq-template.md`        | 用户确认提纲后，输出模式为**标准学习版**时                   |
| `final-faq-audit-template.md`  | 用户确认提纲后，输出模式为**商业审计增强版**时               |
| `source-integrity-rules.md`    | 当锚点可靠性为**中**或**低**，或分析对象为衍生 TXT/MD 时，强制加载并保持激活 |

## Notes

Keep SKILL.md lean. All template-heavy content lives here.
Load only the files needed for the current task — do not preload all references at once.
