# 审读反馈固化查漏补缺方案（1.4.0）

> **目标**：以两轮审读反馈原件为唯一依据，独立复核 1.3.0“审读反馈固化”的融入是否完整、正确、通用，补齐遗漏，理顺规则之间的张力，并清理公开文档中的项目语料。
>
> **执行位置**：分支 `feature/review-feedback-gap-fix`（基于 `main@443b76f`），`main` 不受影响。
>
> **素材**：反馈原件、逐条提取记录与独立复核报告为本地材料，未随仓库分发。本文件只记录通用化后的结论。

---

## 一、复核结论（摘要）

- 1.3.0 已融入的 11 项规则中，多数与反馈原意一致；部分写得过软（以“宜”代替“应”）或只吸收了部分要素。
- 遗漏集中在：引言的问题提出（设问与起笔方案）、摘要要素与常见误区、文献综述的检索与组织、概念界定来源的强度、具体页码定位、DOCX 页面参数、正文句读与自我指涉、反馈载体与审阅人修订的处理。
- 规则张力三处：逐观点标注与“避免一句多注”；理论“正反两面”与“不制造反方”；案例简称引号与审阅人改法。
- 公开文档：两份旧方案文件在排除清单和检索词中写入了项目词，验收时只查了技能正文，没查方案文件本身。

## 二、采纳清单

| 编号 | 规则 | 落位 |
|---|---|---|
| G1 | 问题提出：主问题写成可回答的设问；三种可训练起笔 | `argumentation-diagnostics.md` §章节衔接与表达 |
| G2 | 文献综述：检索要充分、按矛盾组织、有结构 | `argumentation-diagnostics.md` §研究现状与文献综述 |
| G3 | 各部分开头：应交代理论问题并引代表性理论文献；正反两面限于实质分歧 | `argumentation-diagnostics.md` §章节衔接与表达 |
| G4 | 反馈落实：载体读全（脚注批语、高亮范围、附录材料）、共识单列、审阅人修订校读 | `argumentation-diagnostics.md` §反馈如何落实 |
| G5 | 概念界定来源：重要概念（含自建核心概念）应有可回查来源；与“不强求权威背书”区分 | `legal-prose.md` §概念与用词 |
| G6 | 句子层面：主体称谓与简称、少用自我指涉、一句一判断 | `legal-prose.md` §让推论落到句子中 |
| G7 | 引注：具体页码定位；逐观点标注不等于一句多注；案例简称引号 | `citation-integrity.md` |
| G8 | 摘要：补要素（重要性、既有不足、创新）与写法（编辑重组），补误区；手册体例改为引用 | `journal-adaptation.md` §摘要与关键词 |
| G9 | 未指定期刊的 DOCX 工作稿页边距暂用默认“普通” | `journal-adaptation.md` §无目标期刊 |
| G10 | 统计对象一致：删去超出依据的“不同来源” | `evidence-and-legal-validity.md` |
| G11 | 快速示例表：与流传摘编本不一致时回查印刷本 | `citation-format.md` §十 |
| 配套 | evals H11—H17 及 H2、H5、H6 补强；SKILL.md、README、CHANGELOG、压力测试指引接线；旧方案文件脱敏 | 见第三节 |

**不采纳**（依据既有纪律“审稿人个人偏好不升级为通用门槛”）：虚词的文白替换、段首序列词、改法前后不一致的标题格式调整。**待作者确认后再定**：反馈中一组示例对的用途、一类“补充文献信息”批语的确切所指。

## 三、文件级变更

| 文件 | 动作 |
|---|---|
| `references/argumentation-diagnostics.md` | 修改（G1—G4） |
| `references/legal-prose.md` | 修改（G5、G6） |
| `references/citation-integrity.md` | 修改（G7） |
| `references/journal-adaptation.md` | 修改（G8、G9） |
| `references/evidence-and-legal-validity.md` | 修改（G10） |
| `references/citation-format.md` | 修改（G11） |
| `evals/review-feedback-cases.md` | 修改（H11—H17 新增，H2、H5、H6 补强） |
| `evals/pressure-tests.md`、`SKILL.md`、`README.md`、`CHANGELOG.md` | 接线（版本 1.4.0） |
| `docs/superpowers/plans/2026-09-14-generic-rules-fusion.md`、`2026-10-07-citation-format-fusion.md` | 脱敏（项目词改为通用描述） |
| `docs/superpowers/plans/2026-10-08-review-feedback-gap-fix.md` | 新增（本方案） |

## 四、验收标准

- [x] 变更文件与第三节清单一致，清单外零改动；
- [x] 全库（含 `docs/`）项目词表检索零命中；
- [x] 相对链接全部有效；SKILL.md 元数据完整；
- [x] `git diff --check` 无错误；
- [x] 新增规则均有对应 evals 场景。

脱敏只改写当前版本，旧提交历史中仍保留原文；如需清除历史，须改写历史并强制推送，应先与仓库所有者商定。
