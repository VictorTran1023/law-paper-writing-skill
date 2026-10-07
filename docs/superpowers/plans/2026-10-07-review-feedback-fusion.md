# 审读反馈固化方案：两轮论文审读反馈提炼为通用规则

> **目标**：把同一篇稿件上收到的两轮审读反馈（项目负责人的批注与修改、指导专家的通改与批语、及其随附材料）提炼为**通用规则**，融入本仓库写作方法论。全部去项目化重写，不复制反馈原文，不带项目语料。
>
> **执行位置**：本分支 `feature/review-feedback-fusion`（main 不受影响）。
>
> **素材与核对**：反馈原件与逐条解析记录为本地材料（未随仓库分发）；每条规则的反馈出处逐字摘录于工作区《审读反馈固化-核对对照表》备查。

---

## 一、设计原则

1. **通用化重写**：删除项目语境（研究对象、案名、人名、期刊名、数据），示例改为抽象或合成表述。
2. **只吸收可复用规则**：一次性的个案措辞取舍不入库；审稿人个人偏好不升级为通用门槛（沿用既有纪律）。
3. **融入现有结构**：不新增顶层目录；优先并入对应参考文件；确需新文件时同步接线。
4. **增量不重复**：与既有条款近似处只做补充（如证据核验已有数据条款）。

## 二、采纳清单（11 项 + 配套）

| 编号 | 规则 | 批次 | 落位 |
|---|---|---|---|
| R1 | 标注位置：引注紧随观点句；多来源分别就近标注，不集中堆列段末 | 一 | citation-integrity.md |
| R2 | 文献综述写法：扣问题、讲理论脉络、有述有评 | 二 | argumentation-diagnostics.md |
| R3 | 用词规范：不自造术语；慎用宽泛流行词；概念界定要来源 | 一 | legal-prose.md |
| R4 | 通识与含金量：删教科书式铺垫；保证非本专题读者可读 | 二 | legal-prose.md |
| R5 | 各部分开头理论化：以理论关切起头；引理论正反对打 | 二 | argumentation-diagnostics.md |
| R6 | 案例的使用：以生效裁判为主；少作同案多判决对比；引出格式 | 一 | citation-integrity.md |
| R7 | 实证数据可复查：交代检索来源、方法、范围 | 三 | evidence-and-legal-validity.md |
| R8 | 摘要与关键词细化：摘要误区清单化；关键词标示核心主题 | 三 | journal-adaptation.md |
| R9 | 多来源审读反馈处理流水线（解析、登记、合并、冲突清单、交付物） | 三 | argumentation-diagnostics.md §反馈如何落实（必要时新开 feedback-handling.md） |
| R10 | 概念不扎堆：自建概念随问题渐次引入 | 一 | legal-prose.md |
| R11 | 标题成体系：同级平行、下级承接、与正文一致 | 三 | argumentation-diagnostics.md |
| 配套 | evals 反例场景；接线（CHANGELOG、版本、SKILL.md 必要时） | 三 | evals/、根文件 |

## 三、文件级变更计划

| 文件 | 动作 | 批次 |
|---|---|---|
| `references/citation-integrity.md` | 修改（+标注位置、+案例的使用） | 一 |
| `references/legal-prose.md` | 修改（+概念与用词） | 一 |
| `references/argumentation-diagnostics.md` | 修改（R2 增补、R5、R9 扩写、R11） | 二/三 |
| `references/evidence-and-legal-validity.md` | 修改（R7） | 三 |
| `references/journal-adaptation.md` | 修改（R8） | 三 |
| `evals/review-feedback-cases.md` | 新增（配套） | 三 |
| `CHANGELOG.md` / `SKILL.md`（如需要） | 接线 | 三 |
| `docs/superpowers/plans/2026-10-07-review-feedback-fusion.md` | 新增（本方案） | — |

## 四、实施顺序

1. 本提交：方案文件；
2. 第一批：R1、R3、R6、R10 → 交付用户审"写法风格与详略"（附简/详样例对照）；
3. 第二批：R2、R4、R5；
4. 第三批：R7、R8、R9、R11 + evals + 接线；
5. 全量校验（链接、quick_validate、零项目语料、清单外零改动）→ 独立复核 → 用户指示后推送/合并。

## 五、验收标准

- [ ] 变更文件与清单一致，清单外零改动；
- [ ] 新增内容零项目语料（研究对象、案名、人名、期刊名 grep = 0）；
- [ ] 相对链接全通；`quick_validate` 通过；
- [ ] 与既有条款逐条对照，无重复或冲突；
- [ ] 每批附核对对照表（规则 → 反馈出处摘录 → 落位 → 状态）。

## 六、实施记录（滚动更新）

- 2026-10-07：建分支 `feature/review-feedback-fusion`；本方案提交；第一批（R1/R3/R6/R10）落地。
- 2026-10-07（续）：用户选定“长版”写法，第一批按长版改定；第二批（R2/R4/R5）落地。
