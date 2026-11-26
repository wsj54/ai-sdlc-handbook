# AI 时代的软件工程

> 仓库名：`ai-sdlc-handbook`　|　一个关于「AI 时代如何完成软件开发全流程」的方法论与分阶段手册。

[![version](https://img.shields.io/github/v/tag/wsj54/ai-sdlc-handbook?label=version)](https://github.com/wsj54/ai-sdlc-handbook/tags)

---

## 这个项目是什么

当 AI 能够参与需求、设计、编码、测试、部署的绝大多数环节时，软件开发的全流程应该是什么样子？

这个仓库不交付某个具体软件，而是持续研究和整理上面这个问题，最终形成一套可执行的方法论，以及配套的分阶段教程、操作模板与真实案例。每个阶段都回答四个问题：

- 目标是什么？
- 输入是什么？
- 具体怎么做？
- 产出什么、如何验证？

## 这个项目不是什么

- 不是某个 AI 编程工具、Skill 或框架的使用说明；
- 不是提示词技巧合集；
- 不是传统软件工程流程的简单复述；
- 不追求把每个阶段都写成厚文档，而是让每个阶段都有**可检查的中间产物**。

## 核心主张

AI 改变了每个阶段的执行方式，但没有取消流程本身。真正需要重新设计的是人机分工，以及阶段之间的协作方式。

| 角色 | 负责 |
| --- | --- |
| 人 | 定义目标、做出取舍、验收结果 |
| AI | 协助分析、规划、实现和验证 |
| 协作载体 | 规范、计划、任务、测试等明确的中间产物，而不是不断累积的聊天记录 |

由此展开四条原则：

1. **流程仍然存在**：变的是执行方式，不是阶段本身。
2. **规范是主线**：用一份持续有效的规范指导规划、实现与验证，即规范驱动开发（Spec-Driven Development）。
3. **每个阶段都要有产物**：产物必须能被下一阶段读取、被验证，而不是只存在于对话里。
4. **允许回流**：测试发现问题可以回到设计，真实使用发现偏差可以回到需求；需要保持稳定的不是顺序，而是每次修改都有目标、有结果、有影响范围。

## 阶段路线图

当前仓库已提供阶段 1–7 的技能与使用说明；阶段 8 已整理技能要求，技能待实现；阶段 9–12 持续补充。阶段划分以 [`整体流程预览.txt`](./整体流程预览.txt) 为准。

| 阶段 | 状态 | 入口 | 主要产物 |
| --- | --- | --- | --- |
| 1. 原始需求整理 | 已提供 | [`requirement-enrichment`](./step1原始需求整理/requirement-enrichment/SKILL.md) → [`initial-requirements`](./step1原始需求整理/initial-requirements/SKILL.md) → [`initial-requirements-revision`](./step1原始需求整理/initial-requirements-revision/SKILL.md) | `RAW_REQUIREMENTS_BRIEF.md`、`INITIAL_REQUIREMENTS.md` |
| 2. 软件开发模型选择与开发流程规划 | 已提供 | [`development-approach`](./step2开发模型选择与开发流程规划/development-approach/SKILL.md) | `DEVELOPMENT_APPROACH.md` |
| 3. 需求分析与范围管理 | 已提供 | [`requirements-analysis`](./step3需求分析与范围管理/requirements-analysis/SKILL.md) | `REQUIREMENTS.md`、待办与追溯文件 |
| 4. 初步可行性分析与风险识别 | 已提供 | [`feasibility-review`](./step4初步可行性分析与风险识别/feasibility-review/SKILL.md) | `FEASIBILITY_REVIEW.md` |
| 5. 产品设计与交互原型 | 已提供 | [`product-design`](./step5产品设计与交互原型/product-design/SKILL.md) | `PRODUCT_DESIGN.md` |
| 6. 深入技术可行性分析与技术验证 | 已提供 | [`technical-validation`](./step6深入技术可行性分析与技术验证/technical-validation/SKILL.md) | `TECHNICAL_VALIDATION.md`、验证证据 |
| 7. 系统架构设计 | 已提供 | [`architecture-design`](./step7系统架构设计/architecture-design/SKILL.md) | `ARCHITECTURE.md`、ADR |
| 8. 开发计划与任务拆解 | 需求已整理 | [技能要求](./step8开发计划与任务拆解/skill要求.md) | `ROADMAP.md`、开发任务清单 |
| 9. 编码实现 | 规划中 | — | 可运行、可验证的功能增量 |
| 10. 测试与质量保障 | 规划中 | — | 测试记录、审查报告 |
| 11. 部署与发布 | 规划中 | — | 可交付版本 |
| 12. 运行维护与持续迭代 | 规划中 | — | 使用反馈、下一轮需求 |

仓库中还保留 `step2.5`（通用开发阶段适配与流程编排）目录，当前为占位，计划并入阶段 2，不单独计入 12 个阶段。

阶段之间允许回流，不是固定的瀑布模型。

## 快速开始

推荐按下面的顺序使用，每一步确认产物后再进入下一步。

1. **先把想法写下来**：问题、用户、场景、已有功能、限制、还没想清楚的地方。
2. **想法太模糊时先丰富需求**：

   ```text
   请使用 requirement-enrichment 技能，帮我把原始需求丰富完整。
   AI 提的新方向请标成建议，我会说明采纳还是不采纳。
   ```

3. **素材足够后整理成初始需求**：

   ```text
   请使用 initial-requirements 技能整理我的原始需求。
   ```

4. **确定开发模型与流程**：

   ```text
   请使用 development-approach 技能，根据我的原始需求，帮我选择开发模型并制定开发流程。
   ```

5. **收敛为正式需求基线**：

   ```text
   请使用 requirements-analysis 技能，把我的原始需求整理成正式需求基线。
   ```

6. **判断项目整体是否可行**：

   ```text
   使用 feasibility-review 技能，基于当前项目的需求文档做第四阶段可行性分析。
   ```

7. **设计产品页面与交互**：

   ```text
   请使用 product-design 技能，基于我的需求基线产出产品设计文档。
   ```

8. **验证关键技术**：

   ```text
   请使用 technical-validation 技能，基于当前项目文档做技术可行性分析与 PoC 验证。
   ```

9. **设计系统架构**：

   ```text
   请使用 architecture-design 技能，基于当前项目文档做系统架构设计。
   ```

每个阶段都建议从对应的 `使用说明.md` 读起，里面写清了目标、操作步骤、产物、审核方式与常见误区。

## 仓库结构

```text
ai-sdlc-handbook/
├── README.md                          # 项目说明（本文件）
├── 整体流程预览.txt                    # 全流程 12 个阶段总览
├── VERSION                            # 当前版本号（SemVer）
├── .githooks/
│   └── pre-push                       # 推送前自动更新版本号
├── step1原始需求整理/
│   ├── 使用说明.md
│   ├── requirement-enrichment/        # 需求丰富
│   ├── initial-requirements/          # 原始需求整理
│   └── initial-requirements-revision/ # 需求文档修订
├── step2开发模型选择与开发流程规划/
│   ├── 使用说明.md
│   └── development-approach/          # 开发模型选择与流程规划
├── step2.5开发模型与通用开发阶段适配及流程编排/
│   └── 说明.txt                       # 占位，后续并入阶段 2
├── step3需求分析与范围管理/
│   ├── 使用说明.md
│   └── requirements-analysis/         # 需求分析与范围管理
├── step4初步可行性分析与风险识别/
│   ├── 使用说明.md
│   └── feasibility-review/            # 初步可行性分析与风险识别
├── step5产品设计与交互原型/
│   ├── 使用说明.md
│   └── product-design/                # 产品设计与交互蓝图
├── step6深入技术可行性分析与技术验证/
│   ├── 使用说明.md
│   └── technical-validation/          # 技术调研、PoC 与验证
├── step7系统架构设计/
│   ├── 使用说明.md
│   ├── 系统架构设计skill要求.txt
│   └── architecture-design/           # 架构、技术栈、模块与接口
└── step8开发计划与任务拆解/
    └── skill要求.md                    # 技能要求，待实现
```

当前仓库只追踪 `step*` 目录、`README.md`、`整体流程预览.txt` 与版本/钩子基础设施，其余本地研究素材暂未纳入版本控制。

## 每个阶段怎么用

| 阶段 | 先读 | 目标 | 完成标志 |
| --- | --- | --- | --- |
| 1. 原始需求整理 | [使用说明](./step1原始需求整理/使用说明.md) | 把零散想法变成结构化、无冲突的初始需求 | 你确认 `INITIAL_REQUIREMENTS.md` |
| 2. 开发模型与流程 | [使用说明](./step2开发模型选择与开发流程规划/使用说明.md) | 选主开发模型、辅助实践和阶段门禁 | 你确认 `DEVELOPMENT_APPROACH.md` |
| 3. 需求分析与范围 | [使用说明](./step3需求分析与范围管理/使用说明.md) | 划定 MVP、优先级、验收标准，形成需求基线 | 你确认 `REQUIREMENTS.md` |
| 4. 初步可行性分析 | [使用说明](./step4初步可行性分析与风险识别/使用说明.md) | 判断项目整体是否值得推进、是否具备实施条件、有哪些重大风险 | 你确认 `FEASIBILITY_REVIEW.md` |
| 5. 产品设计 | [使用说明](./step5产品设计与交互原型/使用说明.md) | 把需求转成页面结构、用户流程和交互蓝图 | 你确认 `PRODUCT_DESIGN.md` |
| 6. 技术验证 | [使用说明](./step6深入技术可行性分析与技术验证/使用说明.md) | 验证关键技术、识别技术风险，给出架构约束 | 你确认 `TECHNICAL_VALIDATION.md` |
| 7. 系统架构 | [使用说明](./step7系统架构设计/使用说明.md) | 确定架构风格、技术栈、模块、数据与接口 | 你确认 `ARCHITECTURE.md` |
| 8. 开发计划 | [技能要求](./step8开发计划与任务拆解/skill要求.md) | 拆分开发板块与任务，规划多 Agent 协作与执行路线 | 技能待实现 |

每个阶段的技能都会分轮提问，每轮只问当前最阻塞的问题。只有你明确确认的内容才会被视为“已确认”，AI 的推荐只能作为“待定假设”。

## 版本管理

- 版本号采用语义化版本（SemVer），保存在 [`VERSION`](./VERSION)，当前每次推送前自动递增 patch 位。
- 钩子脚本位于 [`.githooks/pre-push`](./.githooks/pre-push)，推送前会：
  1. 读取 `VERSION` 并递增；
  2. 自动提交 `chore(release): vX.Y.Z`；
  3. 打 annotated tag；
  4. 中止本次推送。
- 按提示再次执行 `git push --follow-tags` 即可推送发布提交与 tag。

重新克隆仓库后，需要安装一次钩子入口：

```powershell
# Windows PowerShell
Copy-Item .githooks\pre-push .git\hooks\pre-push
```

```bash
# macOS / Linux
cp .githooks/pre-push .git/hooks/pre-push && chmod +x .git/hooks/pre-push
```

## 文档约定

- 使用中文写作，Markdown 格式；
- 以「阶段」为基本组织单位，每篇讲清：目标、输入、做法、产物、验证方式、常见误区；
- 结论要可操作，避免只停留在概念介绍；
- 引用外部资料时注明来源，区分「已验证的实践」与「个人推断」；
- 新增内容优先并入现有文档，避免产生大量碎片文件；
- 一个阶段一个目录，技能入口统一为 `SKILL.md`，配套 `TEMPLATE.md` 与 `CHECKLIST.md`。

## 参与贡献

欢迎围绕任意阶段补充教程、模板或真实案例。

1. Fork 仓库并从 `main` 创建分支；
2. 保持现有阶段目录结构，不把不同阶段的内容混在同一目录；
3. 提交信息建议遵循 Conventional Commits，例如 `docs: 补充阶段 3 的验收标准说明`；
4. 发起 Pull Request，说明改动的阶段、解决的问题和验证方式。

如果发现阶段划分、产物定义或技能规则有冲突，欢迎先开 Issue 讨论，再改文档。

## 参考来源

- GitHub Spec Kit：规范驱动开发的实践
- OpenAI Codex 工作流：项目指令、分阶段计划与验证
- Matt Pocock Skills：将工程技能映射到开发全流程的案例

---

如果这个项目对你有帮助，欢迎 Star；更欢迎带着一个真实项目来走一遍流程，并把踩坑记录贡献回来。
