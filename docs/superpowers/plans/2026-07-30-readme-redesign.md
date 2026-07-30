# Paper README Professional Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a professional GitHub README for the Chinese legal journal-writing Skill, with a complete usage guide, a repository-backed MIT badge, and two original visual assets.

**Architecture:** Keep all factual behavior in Markdown and use generated raster images only for atmosphere and conceptual reinforcement. Store project images under `assets/readme/`; the rewritten root `README.md` remains the single user-facing entry point and links to existing Skill, templates, sibling repository, and root `LICENSE`.

**Tech Stack:** GitHub Flavored Markdown, GitHub-supported inline HTML, Shields.io static badges, built-in `image_gen`, PNG assets, PowerShell validation.

## Global Constraints

- Preserve `SKILL.md`, `references/`, templates, `LICENSE`, repository name, remote default branch, and existing legal-writing rules.
- Use deep navy, ivory, and restrained cool-gold accents; remain legible in GitHub light and dark modes.
- Do not imply official certification by Hermes, OpenAI, Obsidian, CSSCI, any journal, court, or regulator.
- Do not place generated text, legal citations, case numbers, logos, watermarks, flags, court insignia, gavels, or scales in images.
- Keep the root MIT `LICENSE` unchanged; add only a README badge linking to `LICENSE`, not a README License section.
- The usage guide must cover preparation, mode selection, invocation, project/source templates, work-draft citations, final audit, and common prompt recipes.
- Every image must be stored inside the repository and include meaningful Chinese alt text in README.

## File Map

- Create: `assets/readme/paper-banner.png` — wide README hero artwork.
- Create: `assets/readme/paper-evidence-chain.png` — evidence-chain conceptual illustration.
- Create: `docs/superpowers/plans/2026-07-30-readme-redesign.md` — this implementation plan.
- Modify: `README.md` — complete professional project homepage and usage guide.

---

### Task 1: Generate and Validate Paper Visual Assets

**Files:**
- Create: `assets/readme/paper-banner.png`
- Create: `assets/readme/paper-evidence-chain.png`

**Interfaces:**
- Consumes: the visual constraints in `docs/superpowers/specs/2026-07-30-readme-redesign.md`.
- Produces: two local PNG paths referenced by `README.md`.

- [ ] **Step 1: Verify both target assets are absent before generation**

Run:

```powershell
@(
  'assets/readme/paper-banner.png',
  'assets/readme/paper-evidence-chain.png'
) | ForEach-Object { "$_ = $(Test-Path -LiteralPath $_)" }
```

Expected: both paths print `False`.

- [ ] **Step 2: Generate the paper Banner with the built-in image tool**

Use this exact prompt:

```text
Use case: stylized-concept
Asset type: ultra-wide GitHub README banner for a Chinese legal journal-writing open-source skill
Primary request: create a restrained editorial illustration expressing rigorous legal scholarship, evidence traceability, citation integrity, and manuscript refinement
Scene/backdrop: abstract layered manuscript pages, subtle footnote markers rendered only as non-readable geometric superscript shapes, fine evidence-connection lines, quiet archival paper textures
Style/medium: premium academic editorial design, refined contemporary printmaking mixed with subtle digital depth, no photorealistic people
Composition/framing: ultra-wide 3:1 panoramic composition, balanced central focus, safe margins, visually calm
Lighting/mood: precise, trustworthy, contemplative, understated
Color palette: deep navy, ivory, slate blue, restrained cool gold
Constraints: no readable text, no letters, no numbers, no logos, no watermark, no national symbols, no court insignia, no flag, no gavel, no scales of justice
Avoid: fake citations, fake documents, busy stock-art collage, glossy corporate advertising, neon colors
```

Save the selected result as `assets/readme/paper-banner.png`.

- [ ] **Step 3: Generate the paper evidence-chain illustration**

Use this exact prompt:

```text
Use case: stylized-concept
Asset type: wide conceptual illustration inside a GitHub README
Primary request: visualize an evidence chain moving from source materials through structured research notes and argument nodes into a polished legal journal manuscript
Scene/backdrop: left-to-right sequence of abstract source pages, catalog cards, connected evidence nodes, footnote anchors, and a clean final manuscript; all page content represented by non-readable lines and shapes
Style/medium: sophisticated academic information illustration without labels, editorial vector-like precision with subtle paper texture
Composition/framing: wide 16:9 horizontal flow, clear progression, generous negative space
Lighting/mood: analytical, transparent, dependable
Color palette: deep navy, ivory, slate blue, restrained cool gold
Constraints: no readable text, no letters, no numbers, no logos, no watermark, no people, no national symbols, no court insignia, no gavel, no scales of justice
Avoid: fake citations, UI screenshots, dense infographic labels, decorative clutter
```

Save the selected result as `assets/readme/paper-evidence-chain.png`.

- [ ] **Step 4: Inspect both images**

Open each asset with the local image viewer at original detail. Confirm:

- the Banner reads as an ultra-wide academic hero;
- the evidence illustration clearly progresses left to right;
- no readable pseudo-text, numbers, logos, watermarks, official insignia, gavel, or scales appear;
- both share the same navy/ivory/cool-gold family.

If one condition fails, regenerate only the failing asset with a targeted correction.

- [ ] **Step 5: Verify the generated files**

Run:

```powershell
Get-Item -LiteralPath `
  'assets/readme/paper-banner.png', `
  'assets/readme/paper-evidence-chain.png' |
  Select-Object FullName, Length
```

Expected: both files exist and have non-zero `Length`.

- [ ] **Step 6: Commit the approved image assets**

```bash
git add assets/readme/paper-banner.png assets/readme/paper-evidence-chain.png
git commit -m "Add paper README visuals"
```

### Task 2: Rewrite the Paper README and Add the Usage Guide

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: `assets/readme/paper-banner.png`, `assets/readme/paper-evidence-chain.png`, root `LICENSE`, existing templates and references.
- Produces: the public project landing page.

- [ ] **Step 1: Run the pre-change assertions**

Run:

```powershell
$readme = Get-Content -LiteralPath README.md -Raw -Encoding UTF8
@{
  Banner = $readme.Contains('assets/readme/paper-banner.png')
  UsageGuide = $readme.Contains('## 使用指南')
  LicenseBadge = $readme.Contains('[![License: MIT]')
} | Format-List
```

Expected before implementation: all three values are `False`.

- [ ] **Step 2: Replace README with the approved information architecture**

The rewritten file must contain, in this order:

```text
Banner
Centered title, English subtitle, one-sentence value proposition
Five badges and compact navigation
为什么使用
核心能力
工作流程
真实性与引用边界
快速安装
使用指南
与 Obsidian 配合
Evidence-chain illustration
仓库结构
适用范围
来源说明
```

Use `<p align="center">` only for the hero, badges, and navigation. Use normal Markdown for all substantive content.

- [ ] **Step 3: Add the exact usage-guide components**

Include:

- an input checklist for research question, approved materials, cutoff date, target journal, and output;
- a mode table for `PLAN / RESEARCH / OUTLINE / DRAFT / REVISE / AUDIT / ADAPT`;
- one Hermes call and one Codex call;
- links to `assets/templates/paper-project-brief.md`, `assets/templates/source-register.md`, and `assets/templates/claim-evidence-matrix.md`;
- a Markdown footnote example with `[^S001]`;
- a pending footnote example with `[^待核引注-01]`;
- final-audit links to `assets/templates/citation-audit.md` and `assets/templates/submission-checklist.md`;
- a `<details>` section containing prompts for topic diagnosis, outline, section drafting, citation audit, and journal adaptation.

- [ ] **Step 4: Add the project MIT badge without a License section**

Use:

```markdown
[![License: MIT](https://img.shields.io/badge/License-MIT-B08D57?style=flat-square)](LICENSE)
```

Do not add a `## License` heading. Do not edit `LICENSE`.

- [ ] **Step 5: Add both local images with accessible alt text**

Use repository-relative paths:

```html
<img src="assets/readme/paper-banner.png" alt="深蓝与象牙白构成的法学论文写作与证据链主题横幅" width="100%">
```

```markdown
![从资料、来源登记和论点到正式引注与论文稿件的证据链示意](assets/readme/paper-evidence-chain.png)
```

- [ ] **Step 6: Validate required content and links**

Run:

```powershell
$readme = Get-Content -LiteralPath README.md -Raw -Encoding UTF8
$required = @(
  'assets/readme/paper-banner.png',
  'assets/readme/paper-evidence-chain.png',
  '## 使用指南',
  'PLAN',
  'ADAPT',
  '[^S001]',
  '[^待核引注-01]',
  '[![License: MIT]',
  '](LICENSE)'
)
$missing = $required | Where-Object { -not $readme.Contains($_) }
if ($missing) { $missing; exit 1 }
if ($readme.Contains('## License')) { 'Unexpected README License section'; exit 1 }
```

Expected: exit code `0` and no output.

- [ ] **Step 7: Run repository validation**

Run:

```powershell
git diff --check
python -X utf8 "C:\Users\Victor\.codex\skills\.system\skill-creator\scripts\quick_validate.py" .
```

Expected: no diff errors and `Skill is valid!`.

- [ ] **Step 8: Commit the README**

```bash
git add README.md
git commit -m "Redesign paper skill README"
```

### Task 3: Final Paper Repository Verification

**Files:**
- Verify: `README.md`
- Verify: `LICENSE`
- Verify: `assets/readme/paper-banner.png`
- Verify: `assets/readme/paper-evidence-chain.png`

**Interfaces:**
- Consumes: Tasks 1 and 2.
- Produces: a clean, push-ready branch.

- [ ] **Step 1: Verify all README local links resolve**

Scan Markdown links and HTML `src` attributes. Resolve each local target relative to repository root or the containing Markdown file. Expected: zero missing targets.

- [ ] **Step 2: Verify the license file remains unchanged**

Run:

```powershell
git diff origin/main -- LICENSE
```

Expected: no output.

- [ ] **Step 3: Verify branch cleanliness and recent commits**

Run:

```powershell
git status -sb
git log -4 --oneline
```

Expected: clean worktree on `codex/improve-paper-skill`.

- [ ] **Step 4: Push after the paired book repository passes its own plan**

```bash
git push origin codex/improve-paper-skill
```

Expected: remote branch advances successfully without modifying `main`.
