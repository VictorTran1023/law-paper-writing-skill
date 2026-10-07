# 更新记录

本文件记录本技能的版本与变更。新增能力或规则递增次版本号，措辞与格式修订递增修订号；变更同时更新 `SKILL.md` 的 `metadata.version`。

## 1.3.0（2026-10-07）

新增“审读反馈固化”：把两轮论文审读反馈提炼为通用规则，融入现有参考文件（方案与批次见 `docs/superpowers/plans/2026-10-07-review-feedback-fusion.md`）。

- 引注：`citation-integrity.md` 新增“标注位置”（引注紧随观点句、多来源分别就近标注、不集中堆列）与“案例的使用”（以生效裁判为主、少作多判决对比、引出格式）。
- 表达：`legal-prose.md` 新增“概念与用词”（不自造术语、慎用宽泛流行词、概念不并排）与“常识性内容”（删通识铺垫、保持一般读者可读）两节。
- 论证：`argumentation-diagnostics.md` 新增“研究现状与文献综述”、部分开头理论化与标题体系要求；扩写多来源反馈处理（分别登记、比对合并、不一致交作者、以本方主稿核对）。
- 数据与摘要：`evidence-and-legal-validity.md` 补充数据来源可复查与统计对象一致；`journal-adaptation.md` 补充摘要误区清单与关键词要求。
- 测试：新增 `evals/review-feedback-cases.md`（H1—H10）；SKILL.md 描述词、读取指引与常见错误同步，README 结构树与检验段同步。

## 1.2.0（2026-10-07）

正式版（内容与候选线 1.2.0-rc.1、rc.2 一致）：论证、表达与引注三项更新；未指定期刊时引注默认按《法学引注手册》第二版体例，目标期刊正式要求仍优先。

- 论证：将统一的归纳顺序改为按命题类型检查理由（案例归纳、现行法解释、制度评价、制度建议、概念理论、统计），允许先提出判断再证明；提纲、起草与实质改稿明确读取适用的论证指引。
- 表达：新增正文表达参考与合成对照示例（`references/legal-prose.md`、`assets/examples/legal-prose-examples.md`），处理“AI味”反馈并保留作者有效表达；论点表补充推论理由与必要前提，原稿修订检查立场强弱、研究边界和有效表达。
- 引注：新增 `references/citation-format.md`（手册一般规范与中文文献体例，附快速示例表 32 条）与 `references/citation-format-foreign.md`（英、法、德、意大利、俄、日六语种，第95—150条）；接线读取清单与「生成正文与引注」、`citation-audit.md`（新增 3 项格式检查）、`journal-adaptation.md`（默认体例与期刊优先并存）。
- 测试：新增独立写作任务、评阅方法与实际运行记录（`evals/writing-inputs.md`、`writing-evaluation.md`、`2026-09-18-writing-review.md`、`runs/`）与 8 个引注格式场景（`evals/citation-format-cases.md`，F1—F8）；同步 G1 观察标准、`evals/pressure-tests.md` 指引与 README 结构树、使用指南、检验段。
- 保留来源真实性、法律有效性、引注、期刊适配与资料权限规则；技能不自动更新任何已安装副本。

## 1.1.0（2026-09-15）

新增通用工作纪律（均为通用表述，不绑定特定项目）：

- 需求拆解：需求模糊或新项目启动时先用五问澄清（新增 `references/requirement-decomposition.md` 与 `evals/generic-fusion-cases.md`，G1—G6）。
- 材料边界与查询纪律：写作用料限于已提供或已核验登记的来源；联网检索属于材料获取与核验环节；新标记 `[来源不明：现有材料未覆盖]` 并登记进工作稿标记清单。
- 推理链呈现：核心结论须呈现完整推理链（证据→归纳→排除竞争解释→反例→结论），不以断言出现。
- 版本管理：新稿件版本递增版本号并保留旧版，改动点记入修改记录。

本轮修复与打磨：

- `SKILL.md` 增加 `metadata.version`，description 补入新能力触发词。
- 术语统一为"来源登记"（SKILL.md、evidence-and-legal-validity.md、citation-integrity.md）。
- 论文项目卡增加"读者与用途"字段，承接五问第二问。
- README：去除"材料边界"重复条目；仓库结构树补 `docs/` 与 `CHANGELOG.md`；检验段区分两轮检验并给出场景总数（27）；使用指南衔接五问与版本管理。
- `evals/pressure-tests.md` 末尾指引补指向通用规则融合场景。
- README 图片由 PNG 转为 JPG（横幅 2172×724→1600×533、2.17MB→126KB；插图 1672×941→1600×900、2.07MB→190KB）。

## 1.0.0（2026-07-29）

首个公开版本：任务路由与七项任务模式、五项硬门禁、论证诊断、证据与法律核验、引注完整性、目标期刊适配、Obsidian 协作边界，以及项目卡、来源登记、论点—证据—引注表、反馈落实表等配套模板。
