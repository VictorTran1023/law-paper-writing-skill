# 中国法学论文写作 Skill

面向中国法学学术论文的 Hermes/Codex Skill。用于选题诊断、研究材料组织、论证结构、正文起草、引注核验、全文修改和目标期刊适配。

它提供写作流程与审核门禁，不是任何 CSSCI 期刊的官方指南，也不能保证录用。

## 主要能力

- 区分选题诊断、研究、提纲、起草、修改、审核和期刊适配任务；
- 建立“主问题—分节主张—证据—引注—结论”链条；
- 使用平台无关的来源登记保存完整著录、原始位置、精确定位和核验状态；
- 区分法律规范、司法解释、会议纪要、案例、政策和学术文献；
- 核验法律版本、案例身份和来源状态；
- 生成带正文引注标识的工作稿；
- 使用目标期刊卡处理篇幅、摘要、关键词、匿名和投稿要求；
- 通过指定项目笔记与 Obsidian 配合，不默认扫描整个资料库。
- 区分 Obsidian 读取与写回授权；默认不写回资料库。

## 硬性边界

- 不编造作者、题名、页码、案号、法条、数据、DOI、网址或期刊要求；
- 资料不完整时保留 `[待核]`，不得把工作稿伪装成最终稿；
- 外部观点、引语、数据、法条和案例必须在对应正文后设置引注标识；
- Obsidian 的 `[[双链]]`只用于内部追踪，不能替代正式脚注；
- CSSCI 是来源期刊评价体系，不存在统一的投稿格式；目标期刊正式要求优先。

详细规则见 [SKILL.md](SKILL.md)。

## 安装

### Hermes Agent

Hermes 官方文档将 `~/.hermes/skills/`作为本地 Skill 的主目录。

以下克隆命令以仓库地址可访问为前提；私有仓库须先为当前 Git 客户端配置相应 GitHub 读取权限。

PowerShell：

```powershell
git clone https://github.com/VictorTran1023/law-paper-writing-skill.git `
  "$HOME\.hermes\skills\chinese-law-paper-writing"
```

Bash：

```bash
git clone https://github.com/VictorTran1023/law-paper-writing-skill.git \
  ~/.hermes/skills/chinese-law-paper-writing
```

新建会话后可自然触发，或使用：

```bash
hermes chat -q "/chinese-law-paper-writing 帮我诊断这个法学论文选题"
```

参考：[Hermes Skills System](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills)、[Working with Skills](https://hermes-agent.nousresearch.com/docs/guides/work-with-skills/)。

### OpenAI Codex

PowerShell：

```powershell
git clone https://github.com/VictorTran1023/law-paper-writing-skill.git `
  "$HOME\.codex\skills\chinese-law-paper-writing"
```

Bash：

```bash
git clone https://github.com/VictorTran1023/law-paper-writing-skill.git \
  ~/.codex/skills/chinese-law-paper-writing
```

新建任务后直接要求使用 `chinese-law-paper-writing`。Codex 的项目级持久指令使用 `AGENTS.md`，不是 `CODEX.md`；参见 [Custom instructions with AGENTS.md](https://developers.openai.com/codex/guides/agents-md)。

## 使用示例

```text
使用 chinese-law-paper-writing：
根据我指定的 Obsidian 项目索引和来源笔记，
为“行政公益诉讼中调查核实权的边界”建立论文项目卡、
论点—证据—引注表和三级提纲。
所有缺少原文页码的材料保留待核标记。
```

还可以用于：

- 检查选题是否过宽、是否具有真实学术增量；
- 审核正文是否只有材料而缺乏论证；
- 检查会议纪要、案例和政策文件的使用是否准确；
- 补齐已有可靠来源的脚注；
- 审核全文是否存在引注断链和法律时效问题；
- 按已核验的目标期刊投稿须知调整稿件。

## 与 Obsidian 配合

建议由 Obsidian 管理原始资料、来源笔记和项目索引，由 Hermes 执行写作：

```text
项目索引
→ 来源笔记与原始资料
→ 论点—证据—引注表
→ 带脚注标识的工作稿
→ 引用和法律时效审核
→ 投稿稿
```

每条正式引注应能追溯到原始文件和准确位置。Hermes 默认不写回 Vault；只有明确授权并指定目标文件后才可回写。不要向公开稿件暴露本地路径、私人笔记或整个 Vault。

## 文件结构

```text
law-paper-writing-skill/
├── SKILL.md
├── references/
│   ├── workflow.md
│   ├── evidence-and-legal-validity.md
│   ├── citation-integrity.md
│   ├── journal-adaptation.md
│   └── obsidian-hermes-workflow.md
├── assets/
│   └── templates/
│       ├── paper-project-brief.md
│       ├── journal-profile.md
│       ├── source-register.md
│       ├── claim-evidence-matrix.md
│       ├── citation-audit.md
│       └── submission-checklist.md
├── evals/
│   └── pressure-tests.md
├── README.md
└── LICENSE
```

## 不适用

- 法律专著、教材、评注或实务指南：使用 [chinese-law-book-writing](https://github.com/VictorTran1023/chinese-law-book-writing-skill)；
- 法律意见书、合同、诉状或具体客户法律建议；
- 硕士、博士等学位论文（需要独立的学位论文 Skill 或专门流程）；
- 英文期刊或其他学科论文；
- 自动生成无法核验的参考文献或“保证录用”的稿件。

## 来源与许可

初始方法源于《关于中国法学类CSSCI期刊发表论文的写作过程与方法》，随后增加了目标期刊适配、证据核验、引用完整性、法律时效和 Obsidian/Hermes 工作流。

MIT License © 2025 VictorTran1023
