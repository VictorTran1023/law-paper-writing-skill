# 更新记录

本文件记录本技能的版本与变更。新增能力或规则递增次版本号，措辞与格式修订递增修订号；变更同时更新 `SKILL.md` 的 `metadata.version`。

## 1.2.0（2026-10-07）

新增引注体例（为输出提供默认引注格式；未指定期刊时按《法学引注手册》第二版体例，目标期刊正式要求仍优先）：

- 新增 `references/citation-format.md`：手册一般规范与中文文献体例（引用原则、引注体例、法律文件、司法案例、统计数据，附快速示例表 32 条），条号可回查。
- 新增 `references/citation-format-foreign.md`：引注格式规范·外文文献（英、法、德、意大利、俄、日六语种，第95—150条）。
- 接线：`SKILL.md` 读取清单与「生成正文与引注」补入默认体例；`citation-integrity.md` 增设「格式规范」指引；`citation-audit.md` 新增 3 项格式检查；`journal-adaptation.md` 明确默认体例与期刊优先并存。
- 新增 `evals/citation-format-cases.md`（8 个引注格式场景，F1—F8），`evals/pressure-tests.md` 尾部指引同步指向该场景；README 结构树、使用指南与检验段同步更新。

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
