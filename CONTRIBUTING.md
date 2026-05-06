# Contributing · 贡献指南

Thank you for considering a contribution to **awesome-trading-agents** —
the awesome list for the LLM-driven trading paradigm (Agents · MCPs ·
Skills). This document spells out the quality bar, the submission
format, and the bilingual-PR rule so your PR lands quickly.

感谢你为 **awesome-trading-agents** 做贡献。本仓库专注 LLM 驱动的
交易范式，三大支柱并列收录：Agents · MCPs · Skills。本文档说明
质量门槛、提交格式与双语 PR 规则。

---

## 1. Welcome and scope · 欢迎与范围

This list covers the **post-LLM, agentic stack** for trading,
investment, and financial research. We are deliberately disjoint
from the prior paradigm of time-series deep learning, deep
reinforcement learning trading bots, and classical quantitative
libraries. If a candidate entry's primary value is non-LLM
(LSTM/Transformer/GNN price prediction, DRL trading, classical
quant libraries, robo-advisor without LLM reasoning, payments /
KYC infrastructure, generic LLM tutorials, paid SaaS without an
open artifact), it belongs in another list — see the **Related
awesome lists** section of [README.md](README.md#related-awesome-lists)
for the right home.

本清单专注 LLM 之后的 agentic stack：交易、投资、
金融研究三类场景。我们刻意与"旧范式"（时间序列深度学习、深度
强化学习交易 bot、经典量化库）不重叠。若某仓库的主要价值非
LLM（LSTM/Transformer/GNN 价格预测、DRL 交易、经典量化库、
非 LLM 推理的 robo-advisor、支付/KYC 基础设施、通用 LLM 教程、
无开源 artifact 的付费 SaaS），请去 README 的 **Related awesome
lists / 相关清单** 看更合适的归处。

---

## 2. Quality bar · 质量门槛

To be admitted to the list, an entry should meet these quality and
credibility criteria. PR authors should self-evaluate against this
checklist in the PR description:

- [ ] **Open source** — or has a public technical artifact (paper,
      architecture doc, reproducible demo).
- [ ] **Demonstrably LLM-driven** — uses LLM reasoning as a primary
      decision component, not as a feature extractor or post-hoc
      explainer.
- [ ] **Active or recently active** — last commit within the last
      12 months, unless the entry is a foundational paper or
      canonical reference.
- [ ] **Clear scope + minimal documentation** — has a clear scope
      description and at least minimal documentation.
- [ ] **Distinct contribution** — distinct enough from existing
      entries to merit a separate listing.
- [ ] **Public credibility signal** — normally at least **100
      GitHub stars** for repo entries, with enough external adoption
      signal that the entry improves the main list's trust density.

The public main list is intentionally selective. Repositories below
100 GitHub stars are normally deferred rather than listed. A maintainer
may approve a narrow exception only for a first-party artifact from a
recognized protocol, broker, exchange, or data vendor, or for a
canonical companion repo to a listed paper / benchmark. Such exceptions
must be documented in the PR or issue.

每条目应满足以上质量与可信度准入条件。提交 PR 时请在描述中逐条
自评。公开主清单刻意保持高信噪比：仓库条目通常需要至少
**100 GitHub stars**。低于 100 stars 的仓库默认暂缓收录；只有
已知协议 / 券商 / 交易所 / 数据厂商的一方官方产物，或已收录论文 /
benchmark 的 canonical companion repo，才可由维护者明确豁免，并
在 PR 或 issue 中记录理由。

---

## 3. Submission format — new entry · 新增条目格式

Open an issue first (the smoothest path) using the
[Add entry · 添加条目](.github/ISSUE_TEMPLATE/add-entry.md)
template, OR open a PR directly with the following fields filled:

1. **Repo URL** — the canonical primary URL (the org/repo of record,
   not a fork).
2. **Pillar + sub-category** — pick from existing sub-categories in
   [README.md](README.md#contents). Use the section heading exactly as
   it appears in the README (e.g. `Multi-agent decision frameworks`).
3. **Entry bullet body** — match the existing entry rendering:

   ```
   - [<repo-name>](<repo-url>) - <≤120 en chars / ≤80 zh chars description>. *(Optional pairing / lineage note.)*
   ```

   Do not include inline activity dates, per-entry star counts, or
   bracketed curation badges in the README entry.

4. **Metadata at submission time** — GitHub stars, last commit or
   activity date (`YYYY-MM-DD`). Do not include language, license,
   per-entry star counts, or bracketed curation badges in the README
   row. If license context matters, mention it in curation notes.
5. **Pairing annotation (optional)** — if the entry pairs with an
   already-listed Skill / MCP / Agent, declare it as
   `→ pairs with <name>` (the entry uses the other) or
   `← used by <name>` (the entry is used by the other).
6. **Self-evaluation against the §2 quality-bar checklist** — six
   boxes ticked or explicitly waived with one-sentence reasoning.

新增条目走 [Add entry · 添加条目](.github/ISSUE_TEMPLATE/add-entry.md)
issue 模板最顺；也可直接开 PR，按上述 6 项填写。

---

## 4. Submission format — removal / move · 移除 / 重定位

To request removal of an entry (link rot, project archived,
license changed, no longer LLM-driven, etc.) or to request a move
between sub-categories, open an issue using the
[Remove entry · 移除条目](.github/ISSUE_TEMPLATE/remove-entry.md)
template. PRs that remove entries directly without a tracking
issue may be asked to open the issue first so the rationale is
preserved in the issue tracker.

For sub-category boundary changes (proposing a new axis, merging
two axes, splitting an axis), open a **Restructure proposal**
using the [Restructure · 重构提议](.github/ISSUE_TEMPLATE/restructure.md)
template. Do not silently relabel sub-categories in a regular
new-entry PR.

移除已收录条目走 Remove entry issue 模板。子类边界变更（新增子类、
合并子类、拆分子类）走 Restructure 模板，不要在常规新增 PR 中
顺带改子类标签。

---

## 5. Removal criteria · 移除标准

An entry will be removed (or moved to a Watch annotation) if **any**
of the following becomes true:

- **Repo deleted or archived** for >12 months without a clearly
  identified successor.
- **License changed** to a form that contradicts the CC0-1.0
  reusability assumptions of this list. The entry stays on the list
  but moves to a `[Watch]` annotation if the project itself is
  otherwise canonical.
- **No longer LLM-driven** — refactored away from LLM reasoning as
  a primary decision component (e.g. ablated to a non-LLM rule
  engine or pure classical-ML pipeline).
- **Public credibility dropped below the main-list floor** — on a
  maintainer-led re-evaluation pass, the project no longer clears the
  100-star reputation floor and has no documented first-party or
  canonical companion exception.
- **Two-or-more failures** on the §2 quality-bar checklist on a
  re-evaluation pass.

仓库删除 / 归档 12 个月以上、许可证变更与 CC0-1.0 可重用假设
冲突、不再 LLM 驱动、在维护者复核中低于 100-star 主清单可信度
门槛且无明确豁免理由，或在重新评估中触发 §2 多项失败 — 任一条件
满足即移除（或转入 Watch）。

---

## 6. Bilingual-PR rule · 双语 PR 规则

This repo is bilingual: `README.md` (English, primary on
github.com surface) and `README.zh-CN.md` (Simplified Chinese, the
authored source-of-truth during development). They are kept in 1:1
structural lockstep — same sections, same sub-categories, same
entry order, identical `<a id>` anchors.

**Each PR that edits one README MUST edit the other in the same
PR**, OR open a tracked translation issue with a **7-day SLA** for
the sibling edit. The exception path:

1. Open the PR against the README you can edit, and link to the
   tracked translation issue in the PR description.
2. The PR is held in review (not merged) until either:
   - The sibling edit lands in the same PR, OR
   - The 7-day SLA expires AND the maintainer team explicitly
     signs off on a single-side merge with a follow-up tracking
     issue.

Bilingual lockstep applies to:

- Section headings and sub-category labels (mirror, not literal
  translate).
- Entry order within each sub-category.
- The 64+ `<a id>` anchor IDs (must remain identical across the
  two READMEs so cross-link integrity holds).

每个改动 README 的 PR 必须同 PR 改另一份 README，或开一个 7 天
SLA 翻译跟踪 issue。两份 README 的 sub-category 顺序、条目顺序、
`<a id>` 锚 ID 必须 1:1 对齐。

---

## 7. Sub-category boundary policy · 子类边界政策

When in doubt between two sub-categories, pick the one whose
existing definition (visible at the sub-section heading + intro
paragraph in [README.md](README.md)) is the closer fit. If
**neither** sub-category fits, **file an issue rather than
silently creating a new sub-category** — sub-category churn
requires a maintainer-led re-enumeration pass and lands via the
Restructure template (§4 above).

Do not relabel an existing sub-category in a new-entry PR.
Sub-category labels are part of the locked v0.1 taxonomy; changes
are reviewed separately.

判断不清时优先选与现有子类定义更接近的那一个。若都不合适，请
开 Restructure issue 而非自创新子类 — 子类边界改动需维护团队
统一重新枚举。

---

## 8. Curation notes · 策展说明

The README should read like a conventional awesome list: project
link, concise description, and only durable metadata. Avoid
bracketed badges for curation judgments. Express important context in
plain language:

- If a project is official, say so in the description (for example,
  "Alpaca's official MCP").
- If a project spans multiple pillars, list it once in its primary
  section and use a short cross-link where the secondary angle matters.
- If several entries share an author or fork lineage, mention that in
  prose only when it helps navigation.
- Maintainer first-read picks live in the README's "If you only read
  three" block, not as per-entry badges.

README 应保持传统 awesome list 的阅读方式：项目链接、简洁描述、
只保留稳定元信息。避免把策展判断做成公开的方括号徽标，重要信息用自然语言表达：

- 官方项目就在描述里写明（例如"Alpaca 官方 MCP"）。
- 跨支柱项目只在主归属章节展开；确有必要时，在次要视角保留一行
  回链。
- 同作者或 fork 关系只有在有助导航时才用正文说明。
- 维护者推荐的首读入口放在 README 顶部"如果你只读三个"，不做
  每条目徽标。

---

## 9. Awesome-lint as an advisory check · awesome-lint 辅助检查

We use `awesome-lint` as an **advisory compatibility check** against
the broader GitHub awesome-list ecosystem:

```bash
npx --yes awesome-lint README.md
```

For Chinese-language structure checks, you may also run:

```bash
npx --yes awesome-lint README.zh-CN.md
```

Treat the output as reviewer input, not as an automatic merge gate.
This repository intentionally uses a few patterns that classic
awesome lists do not: stable `<a id>` anchors, compact pairing
metadata in entry rows, cross-pillar back-links, bilingual text, and a
visual image header instead of a Markdown H1. These may trigger false
positives such as duplicate links, non-standard list items, or
heading-name complaints.

High-signal findings should still be fixed when they are introduced by
your PR: broken Markdown, malformed links, accidental duplicate primary
entries, misspellings, or list items that no longer follow the local
entry format. Do **not** reformat the entire README only to satisfy
`awesome-lint`; preserve this repository's local structure unless a
maintainer explicitly asks for a broader cleanup.

我们把 `awesome-lint` 当作**辅助兼容性检查**，用来对照 GitHub
awesome-list 生态的传统格式，而不是自动阻塞合并的硬门槛：

```bash
npx --yes awesome-lint README.md
```

也可以对中文版跑一遍结构检查：

```bash
npx --yes awesome-lint README.zh-CN.md
```

请把输出视为 review 参考。本仓库有意使用若干传统 awesome list
不常见的结构：稳定 `<a id>` 锚点、紧凑的更新日期元信息、跨支柱回链、双语
文本。因此 duplicate links、non-standard list items、
heading-name 等结果可能是可接受的噪音。

如果 PR 新引入了高信号问题，应当修复：Markdown 破损、链接格式
错误、意外重复主条目、拼写问题、或条目不再符合本仓库条目格式。
不要为了通过 `awesome-lint` 而大规模重排 README；除非维护者明确
要求，否则以保持本仓库既有结构为准。

---

## 10. Code of conduct · 行为准则

This project follows the
[Contributor Covenant v2.1](https://www.contributor-covenant.org/version/2/1/code_of_conduct/).
By participating, you agree to uphold its standards: be respectful,
assume good faith, focus on the technical work, and report
violations to the maintainer team via a private channel.

Behaviour that demeans contributors, derails technical discussion,
or pursues personal disputes through PR / issue threads is
out-of-bounds and may result in PR closure or, in repeated cases,
a ban from the repo.

本项目遵循 [Contributor Covenant v2.1](https://www.contributor-covenant.org/version/2/1/code_of_conduct/)
行为准则。参与本项目即同意遵守该准则：保持尊重、善意推断、聚焦
技术、违规请通过私信渠道向维护团队反馈。

---

## 11. License notice · 许可证说明

The list itself — this README, `CONTRIBUTING.md`, the curation
structure, and every contribution to the list's text — is released
under [CC0-1.0](LICENSE). By submitting a PR you agree that your
contribution to the list's text is released under CC0-1.0.

**Each linked entry retains its own license**. Adding an entry to this
list does not change that entry's license. The CC0-1.0 release covers
the description text we author about the entry; it does not cover the
linked code itself.

清单本身（本 README、CONTRIBUTING.md、策展结构、对清单文本的
每一个贡献）以 [CC0-1.0](LICENSE) 发布。提交 PR 即表示同意你对
清单文本的贡献以 CC0-1.0 发布。每个被收录的条目保留其原有许可；
收录不改变原项目许可。

---

Maintained by [LLMQuant](https://llmquant.com) · 维护方：LLMQuant 社区
