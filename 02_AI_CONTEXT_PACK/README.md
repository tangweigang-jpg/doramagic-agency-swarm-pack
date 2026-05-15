# AI Context Pack

## Pack Identity

- Upstream: https://github.com/VRSEN/agency-swarm
- Pack type: Agency Swarm Pack
- Doramagic canonical: https://doramagic.ai/zh/projects/agency-swarm/
- Relationship: independent pack; not affiliated or endorsed unless explicitly stated.

## Operating Rules

- Evidence first.
- No official endorsement claim.
- Run evals before claiming success.
- Use pitfall and risk files for recovery.

## Host Files

- `../AGENTS.md`
- `../CLAUDE.md`

## Doramagic Source Extract

# agency-swarm-agent-generator - Doramagic AI Context Pack

> 定位：安装前体验与判断资产。它帮助宿主 AI 有一个好的开始，但不代表已经安装、执行或验证目标项目。

## 充分原则

- **充分原则，不是压缩原则**：AI Context Pack 应该充分到让宿主 AI 在开工前理解项目价值、能力边界、使用入口、风险和证据来源；它可以分层组织，但不以最短摘要为目标。
- **压缩策略**：只压缩噪声和重复内容，不压缩会影响判断和开工质量的上下文。

## 给宿主 AI 的使用方式

你正在读取 Doramagic 为 agency-swarm-agent-generator 编译的 AI Context Pack。请把它当作开工前上下文：帮助用户理解适合谁、能做什么、如何开始、哪些必须安装后验证、风险在哪里。不要声称你已经安装、运行或执行了目标项目。

## Claim 消费规则

- **事实来源**：Repo Evidence + Claim/Evidence Graph；Human Wiki 只提供显著性、术语和叙事结构。
- **事实最低状态**：`supported`
- `supported`：可以作为项目事实使用，但回答中必须引用 claim_id 和证据路径。
- `weak`：只能作为低置信度线索，必须要求用户继续核实。
- `inferred`：只能用于风险提示或待确认问题，不能包装成项目事实。
- `unverified`：不得作为事实使用，应明确说证据不足。
- `contradicted`：必须展示冲突来源，不得替用户强行选择一个版本。

## 它最适合谁

- **正在使用 Claude/Codex/Cursor/Gemini 等宿主 AI 的开发者**：README 或插件配置提到多个宿主 AI。 证据：`README.md` Claim：`clm_0003` supported 0.86
- **希望把专业流程带进宿主 AI 的用户**：仓库包含 Skill 文档。 证据：`.codex/skills/claude-cli-review/SKILL.md`, `.codex/skills/codex-cli-review/SKILL.md`, `.codex/skills/delegation-management/SKILL.md`, `.codex/skills/policy-maintenance/SKILL.md` 等 Claim：`clm_0004` supported 0.86

## 它能做什么

- **AI Skill / Agent 指令资产库**（可做安装前预览）：项目包含可被宿主 AI 读取的 Skill 或 Agent 指令文件，可用于把专业流程带入 Claude、Codex、Cursor 等宿主。 证据：`.codex/skills/claude-cli-review/SKILL.md`, `.codex/skills/codex-cli-review/SKILL.md`, `.codex/skills/delegation-management/SKILL.md`, `.codex/skills/policy-maintenance/SKILL.md` 等 Claim：`clm_0001` supported 0.86
- **命令行启动或安装流程**（需要安装后验证）：项目文档中存在可执行命令，真实使用需要在本地或宿主环境中运行这些命令。 证据：`README.md` Claim：`clm_0002` supported 0.86

## 怎么开始

- `pip install -U agency-swarm` 证据：`README.md` Claim：`clm_0005` supported 0.86

## 继续前判断卡

- **当前建议**：需要管理员/安全审批
- **为什么**：继续前可能涉及密钥、账号、外部服务或敏感上下文，建议先经过管理员或安全审批。

### 30 秒判断

- **现在怎么做**：需要管理员/安全审批
- **最小安全下一步**：先跑 Prompt Preview；若涉及凭证或企业环境，先审批再试装
- **先别相信**：真实输出质量不能在安装前相信。
- **继续会触碰**：命令执行、宿主 AI 配置、本地环境或项目文件

### 现在可以相信

- **适合人群线索：正在使用 Claude/Codex/Cursor/Gemini 等宿主 AI 的开发者**（supported）：有 supported claim 或项目证据支撑，但仍不等于真实安装效果。 证据：`README.md` Claim：`clm_0003` supported 0.86
- **适合人群线索：希望把专业流程带进宿主 AI 的用户**（supported）：有 supported claim 或项目证据支撑，但仍不等于真实安装效果。 证据：`.codex/skills/claude-cli-review/SKILL.md`, `.codex/skills/codex-cli-review/SKILL.md`, `.codex/skills/delegation-management/SKILL.md`, `.codex/skills/policy-maintenance/SKILL.md` 等 Claim：`clm_0004` supported 0.86
- **能力存在：AI Skill / Agent 指令资产库**（supported）：可以相信项目包含这类能力线索；是否适合你的具体任务仍要试用或安装后验证。 证据：`.codex/skills/claude-cli-review/SKILL.md`, `.codex/skills/codex-cli-review/SKILL.md`, `.codex/skills/delegation-management/SKILL.md`, `.codex/skills/policy-maintenance/SKILL.md` 等 Claim：`clm_0001` supported 0.86
- **能力存在：命令行启动或安装流程**（supported）：可以相信项目包含这类能力线索；是否适合你的具体任务仍要试用或安装后验证。 证据：`README.md` Claim：`clm_0002` supported 0.86
- **存在 Quick Start / 安装命令线索**（supported）：可以相信项目文档出现过启动或安装入口；不要因此直接在主力环境运行。 证据：`README.md` Claim：`clm_0005` supported 0.86

### 现在还不能相信

- **真实输出质量不能在安装前相信。**（unverified）：Prompt Preview 只能展示引导方式，不能证明真实项目中的结果质量。
- **宿主 AI 版本兼容性不能在安装前相信。**（unverified）：Claude、Cursor、Codex、Gemini 等宿主加载规则和版本差异必须在真实环境验证。
- **不会污染现有宿主 AI 行为，不能直接相信。**（inferred）：Skill、plugin、AGENTS/CLAUDE/GEMINI 指令可能改变宿主 AI 的默认行为。 证据：`.codex/skills/claude-cli-review/SKILL.md`, `.codex/skills/codex-cli-review/SKILL.md`, `.codex/skills/delegation-management/SKILL.md`, `.codex/skills/policy-maintenance/SKILL.md` 等
- **可安全回滚不能默认相信。**（unverified）：除非项目明确提供卸载和恢复说明，否则必须先在隔离环境验证。
- **真实安装后是否与用户当前宿主 AI 版本兼容？**（unverified）：兼容性只能通过实际宿主环境验证。
- **项目输出质量是否满足用户具体任务？**（unverified）：安装前预览只能展示流程和边界，不能替代真实评测。
- **安装命令是否需要网络、权限或全局写入？**（unverified）：这影响企业环境和个人环境的安装风险。 证据：`README.md`

### 继续会触碰什么

- **命令执行**：包管理器、网络下载、本地插件目录、项目配置或用户主目录。 原因：运行第一条命令就可能产生环境改动；必须先判断是否值得跑。 证据：`README.md`
- **宿主 AI 配置**：Claude/Codex/Cursor/Gemini/OpenCode 等宿主的 plugin、Skill 或规则加载配置。 原因：宿主配置会改变 AI 后续工作方式，可能和用户已有规则冲突。 证据：`.codex/skills/claude-cli-review/SKILL.md`, `.codex/skills/codex-cli-review/SKILL.md`, `.codex/skills/delegation-management/SKILL.md`, `.codex/skills/policy-maintenance/SKILL.md` 等
- **本地环境或项目文件**：安装结果、插件缓存、项目配置或本地依赖目录。 原因：安装前无法证明写入范围和回滚方式，需要隔离验证。 证据：`README.md`
- **环境变量 / API Key**：项目入口文档明确出现 API key、token、secret 或账号凭证配置。 原因：如果真实安装需要凭证，应先使用测试凭证并经过权限/合规判断。 证据：`.claude/agents/agent-creator.md`, `.claude/agents/api-researcher.md`, `.claude/agents/prd-creator.md`, `README.md` 等
- **宿主 AI 上下文**：AI Context Pack、Prompt Preview、Skill 路由、风险规则和项目事实。 原因：导入上下文会影响宿主 AI 后续判断，必须避免把未验证项包装成事实。

### 最小安全下一步

- **先跑 Prompt Preview**：用安装前交互式试用判断工作方式是否匹配，不需要授权或改环境。（适用：任何项目都适用，尤其是输出质量未知时。）
- **只在隔离目录或测试账号试装**：避免安装命令污染主力宿主 AI、真实项目或用户主目录。（适用：存在命令执行、插件配置或本地写入线索时。）
- **先备份宿主 AI 配置**：Skill、plugin、规则文件可能改变 Claude/Cursor/Codex 的默认行为。（适用：存在插件 manifest、Skill 或宿主规则入口时。）
- **不要使用真实生产凭证**：环境变量/API key 一旦进入宿主或工具链，可能产生账号和合规风险。（适用：出现 API、TOKEN、KEY、SECRET 等环境线索时。）
- **安装后只验证一个最小任务**：先验证加载、兼容、输出质量和回滚，再决定是否深用。（适用：准备从试用进入真实工作流时。）

### 退出方式

- **保留安装前状态**：记录原始宿主配置和项目状态，后续才能判断是否可恢复。
- **准备移除宿主 plugin / Skill / 规则入口**：如果试装后行为异常，可以把宿主 AI 恢复到试装前状态。
- **记录安装命令和写入路径**：没有明确卸载说明时，至少要知道哪些目录或配置需要手动清理。
- **准备撤销测试 API key 或 token**：测试凭证泄露或误用时，可以快速止损。
- **如果没有回滚路径，不进入主力环境**：不可回滚是继续前阻断项，不应靠信任或运气继续。

## 哪些只能预览

- 解释项目适合谁和能做什么
- 基于项目文档演示典型对话流程
- 帮助用户判断是否值得安装或继续研究

## 哪些必须安装后验证

- 真实安装 Skill、插件或 CLI
- 执行脚本、修改本地文件或访问外部服务
- 验证真实输出质量、性能和兼容性

## 边界与风险判断卡

- **把安装前预览误认为真实运行**：用户可能高估项目已经完成的配置、权限和兼容性验证。 处理方式：明确区分 prompt_preview_can_do 与 runtime_required。 Claim：`clm_0006` inferred 0.45
- **命令执行会修改本地环境**：安装命令可能写入用户主目录、宿主插件目录或项目配置。 处理方式：先在隔离环境或测试账号中运行。 证据：`README.md` Claim：`clm_0007` supported 0.86
- **待确认**：真实安装后是否与用户当前宿主 AI 版本兼容？。原因：兼容性只能通过实际宿主环境验证。
- **待确认**：项目输出质量是否满足用户具体任务？。原因：安装前预览只能展示流程和边界，不能替代真实评测。
- **待确认**：安装命令是否需要网络、权限或全局写入？。原因：这影响企业环境和个人环境的安装风险。

## 开工前工作上下文

### 加载顺序

- 先读取 how_to_use.host_ai_instruction，建立安装前判断资产的边界。
- 读取 claim_graph_summary，确认事实来自 Claim/Evidence Graph，而不是 Human Wiki 叙事。
- 再读取 intended_users、capabilities 和 quick_start_candidates，判断用户是否匹配。
- 需要执行具体任务时，优先查 role_skill_index，再查 evidence_index。
- 遇到真实安装、文件修改、网络访问、性能或兼容性问题时，转入 risk_card 和 boundaries.runtime_required。

### 任务路由

- **AI Skill / Agent 指令资产库**：先基于 role_skill_index / evidence_index 帮用户挑选可用角色、Skill 或工作流。 边界：可做安装前 Prompt 体验。 证据：`.codex/skills/claude-cli-review/SKILL.md`, `.codex/skills/codex-cli-review/SKILL.md`, `.codex/skills/delegation-management/SKILL.md`, `.codex/skills/policy-maintenance/SKILL.md` 等 Claim：`clm_0001` supported 0.86
- **命令行启动或安装流程**：先说明这是安装后验证能力，再给出安装前检查清单。 边界：必须真实安装或运行后验证。 证据：`README.md` Claim：`clm_0002` supported 0.86

### 上下文规模

- 文件总数：447
- 重要文件覆盖：40/447
- 证据索引条目：73
- 角色 / Skill 条目：5

### 证据不足时的处理

- **missing_evidence**：说明证据不足，要求用户提供目标文件、README 段落或安装后验证记录；不要补全事实。
- **out_of_scope_request**：说明该任务超出当前 AI Context Pack 证据范围，并建议用户先查看 Human Manual 或真实安装后验证。
- **runtime_request**：给出安装前检查清单和命令来源，但不要替用户执行命令或声称已执行。
- **source_conflict**：同时展示冲突来源，标记为待核实，不要强行选择一个版本。

## Prompt Recipes

### 适配判断

- 目标：判断这个项目是否适合用户当前任务。
- 预期输出：适配结论、关键理由、证据引用、安装前可预览内容、必须安装后验证内容、下一步建议。

```text
请基于 agency-swarm-agent-generator 的 AI Context Pack，先问我 3 个必要问题，然后判断它是否适合我的任务。回答必须包含：适合谁、能做什么、不能做什么、是否值得安装、证据来自哪里。所有项目事实必须引用 evidence_refs、source_paths 或 claim_id。
```

### 安装前体验

- 目标：让用户在安装前感受核心工作流，同时避免把预览包装成真实能力或营销承诺。
- 预期输出：一段带边界标签的体验剧本、安装后验证清单和谨慎建议；不含真实运行承诺或强营销表述。

```text
请把 agency-swarm-agent-generator 当作安装前体验资产，而不是已安装工具或真实运行环境。

请严格输出四段：
1. 先问我 3 个必要问题。
2. 给出一段“体验剧本”：用 [安装前可预览]、[必须安装后验证]、[证据不足] 三种标签展示它可能如何引导工作流。
3. 给出安装后验证清单：列出哪些能力只有真实安装、真实宿主加载、真实项目运行后才能确认。
4. 给出谨慎建议：只能说“值得继续研究/试装”“先补充信息后再判断”或“不建议继续”，不得替项目背书。

硬性边界：
- 不要声称已经安装、运行、执行测试、修改文件或产生真实结果。
- 不要写“自动适配”“确保通过”“完美适配”“强烈建议安装”等承诺性表达。
- 如果描述安装后的工作方式，必须使用“如果安装成功且宿主正确加载 Skill，它可能会……”这种条件句。
- 体验剧本只能写成“示例台词/假设流程”：使用“可能会询问/可能会建议/可能会展示”，不要写“已写入、已生成、已通过、正在运行、正在生成”。
- Prompt Preview 不负责给安装命令；如用户准备试装，只能提示先阅读 Quick Start 和 Risk Card，并在隔离环境验证。
- 所有项目事实必须来自 supported claim、evidence_refs 或 source_paths；inferred/unverified 只能作风险或待确认项。

```

### 角色 / Skill 选择

- 目标：从项目里的角色或 Skill 中挑选最匹配的资产。
- 预期输出：候选角色或 Skill 列表，每项包含适用场景、证据路径、风险边界和是否需要安装后验证。

```text
请读取 role_skill_index，根据我的目标任务推荐 3-5 个最相关的角色或 Skill。每个推荐都要说明适用场景、可能输出、风险边界和 evidence_refs。
```

### 风险预检

- 目标：安装或引入前识别环境、权限、规则冲突和质量风险。
- 预期输出：环境、权限、依赖、许可、宿主冲突、质量风险和未知项的检查清单。

```text
请基于 risk_card、boundaries 和 quick_start_candidates，给我一份安装前风险预检清单。不要替我执行命令，只说明我应该检查什么、为什么检查、失败会有什么影响。
```

### 宿主 AI 开工指令

- 目标：把项目上下文转成一次对话开始前的宿主 AI 指令。
- 预期输出：一段边界明确、证据引用明确、适合复制给宿主 AI 的开工前指令。

```text
请基于 agency-swarm-agent-generator 的 AI Context Pack，生成一段我可以粘贴给宿主 AI 的开工前指令。这段指令必须遵守 not_runtime=true，不能声称项目已经安装、运行或产生真实结果。
```


## 角色 / Skill 索引

- 共索引 5 个角色 / Skill / 项目文档条目。

- **claude-cli-review**（skill）：Use when Claude CLI is the chosen local review worker for a bounded diff review or extraction pass and a saved /tmp artifact is required. 激活提示：当用户任务与“claude-cli-review”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.codex/skills/claude-cli-review/SKILL.md`
- **codex-cli-review**（skill）：Use when a local Codex CLI review, pull-request opening or update compliance check, pull-request comment review loop, or saved Codex review artifact is required for this repo. 激活提示：当用户任务与“codex-cli-review”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.codex/skills/codex-cli-review/SKILL.md`
- **delegation-management**（skill）：Use when a manager delegates to subagents, scopes staged worker tasks, decides whether to reuse or rotate workers, or reviews delegated output before relying on it. 激活提示：当用户任务与“delegation-management”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.codex/skills/delegation-management/SKILL.md`
- **policy-maintenance**（skill）：Use when editing AGENTS.md, CLAUDE.md, or .codex/skills/ policy, workflow, and manager-skill files. Keeps durable operating rules concise, separates general policy from manager-only policy, and requires review for distorted meaning or regressions. 激活提示：当用户任务与“policy-maintenance”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.codex/skills/policy-maintenance/SKILL.md`
- **requirement-ledger**（skill）：Use when a task needs a durable active requirement queue and archive workflow. Captures only real user requests or requirements with proofread, sanitized requirement text, source pointers, category, intent, status, next action, and linked artifacts; avoids noisy transcript dumps without erasing user intent. 激活提示：当用户任务与“requirement-ledger”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.codex/skills/requirement-ledger/SKILL.md`

## 证据索引

- 共索引 73 条证据。

- **Agency Swarm Claude Code Sub-Agents**（documentation）：Agency Swarm Claude Code Sub-Agents 证据：`.claude/README.md`
- **Instruction File Contract**（documentation）：1. Definitions 1.1 Instruction File : the policy text in AGENTS.md and its Mirror Link. 1.2 Mirror Link : the symlink at CLAUDE.md that points to AGENTS.md . 1.3 User Request : any explicit user direction, issue, failure, contradiction, odd behavior, or useful clue that changes the work. 1.4 Manager : an agent with a real Native Subagent capability. 1.5 Subagent : an agent without that capability, or one acting under delegation. 1.6 Native Subagent : the built-in delegation capability. 1.7 Default Native Subagent Policy : model gpt-5.4 with high reasoning. 1.8 Mandate : the authorized action, repository, branch, artifact, and visibility boundary for the task. 1.9 Requirement Ledger : the du… 证据：`AGENTS.md`
- **🐝 Agency Swarm**（documentation）：! Framework https://firebasestorage.googleapis.com/v0/b/vrsen-ai/o/public%2Fgithub%2FLOGO BG large bold shadow%20 1 .jpg?alt=media&token=8c681331-2a7a-4a69-b21b-3ab1f9bf1a23 证据：`README.md`
- **Examples**（documentation）：This directory contains runnable examples demonstrating key features of Agency Swarm v1.x. 证据：`examples/README.md`
- **Tests**（documentation）：Before running any tests, make sure you have uv installed and ideally run make sync after . 证据：`tests/README.md`
- **FastAPI Integration Example**（documentation）：Full Guide: The canonical FastAPI documentation lives in docs/additional-features/fastapi-integration.mdx . This README only summarizes the runnable sample. 证据：`examples/fastapi_integration/README.md`
- **Integrations Technical Reference**（documentation）：This file documents technical details for framework integrations that are too low-level for end-user deployment docs. 证据：`src/agency_swarm/integrations/README.md`
- **Getting Started**（documentation）：This is a Next.js https://nextjs.org project bootstrapped with create-next-app https://nextjs.org/docs/app/api-reference/cli/create-next-app . 证据：`src/agency_swarm/ui/demos/copilot/README.md`
- **Package**（package_manifest）：{ "name": "agency-swarm-agent-generator", "version": "1.8.0", "description": "Generate Agency Swarm v1.x agents from settings.json files", "private": true, "devDependencies": { "@types/node": "^20.0.0", "typescript": "^5.0.0", "ts-node": "^10.9.0" }, "engines": { "node": " =16.0.0" } } 证据：`package.json`
- **Contributing to Agency Swarm**（documentation）：Contributing to Agency Swarm Each agent or tool you add to Agency Swarm will automatically be available for import by the Genesis Swarm, which will help us create an exponentially larger and smarter system. 证据：`CONTRIBUTING.md`
- **Package**（package_manifest）：{ "name": "ag-ui-app", "version": "0.1.0", "private": true, "scripts": { "dev": "next dev --turbopack", "build": "next build", "start": "next start", "lint": "next lint" }, "dependencies": { "@ag-ui/client": "^0.0.41", "@ag-ui/langgraph": "^0.0.19", "@copilotkit/react-core": "^1.9.1", "@copilotkit/react-ui": "^1.9.1", "@copilotkit/runtime": "^1.9.1", "class-variance-authority": "^0.7.1", "clsx": "^2.1.1", "lucide-react": "^0.522.0", "next": "^15.4.7", "react": "^19.0.0", "react-dom": "^19.0.0", "tailwind-merge": "^3.3.1" }, "devDependencies": { "@tailwindcss/postcss": "^4", "@types/node": "^20", "@types/react": "^19", "@types/react-dom": "^19", "tailwindcss": "^4", "tw-animate-css": "^1.3.4… 证据：`src/agency_swarm/ui/demos/copilot/package.json`
- **Claude CLI Review**（skill_instruction）：Use Claude CLI only when AGENTS.md and Tool And Model Policy allow it. Treat it as weaker evidence than GPT-5.5; managers must verify its output before final decisions. 证据：`.codex/skills/claude-cli-review/SKILL.md`
- **Codex CLI Review**（skill_instruction）：Use this skill for local Codex review artifacts and pull-request review loops. 证据：`.codex/skills/codex-cli-review/SKILL.md`
- **Delegation Management**（skill_instruction）：Use this skill when delegation affects correctness, queue control, review quality, or context management. 证据：`.codex/skills/delegation-management/SKILL.md`
- **Policy Maintenance**（skill_instruction）：Use this skill for policy, workflow-rule, and repo-skill changes. Repo skills are checked-in manager instructions under .codex/skills/ ; read the relevant SKILL.md when AGENTS.md routes work to one unless the environment exposes the skill directly. 证据：`.codex/skills/policy-maintenance/SKILL.md`
- **Requirement Ledger**（skill_instruction）：Use this skill when task state must survive beyond the current chat or when a request has several requirements that can drift. The ledger records work state; durable operating rules live in AGENTS.md or the relevant repo skill. 证据：`.codex/skills/requirement-ledger/SKILL.md`
- **License**（source_file）：Copyright c 2023–2025 Nick Bobrowski, Arsenii Shatokhin, Artemii Shatokhin 证据：`LICENSE`
- **Background**（documentation）：Create complete agent modules including folders, agent classes, and initial configurations for Agency Swarm v1.0.0 agencies. 证据：`.claude/agents/agent-creator.md`
- **Background**（documentation）：Research MCP servers and APIs for Agency Swarm v1.0.0 tool implementation, strongly prioritizing MCP servers. 证据：`.claude/agents/api-researcher.md`
- **Background**（documentation）：Write and refine Agency Swarm v1.0.0 agent instructions using prompt engineering best practices for maximum clarity and performance. 证据：`.claude/agents/instructions-writer.md`
- **Background**（documentation）：Create Product Requirements Documents for Agency Swarm v1.0.0 agencies, optimized for parallel agent creation. 证据：`.claude/agents/prd-creator.md`
- **Background**（documentation）：Wire agency components and test with 5 realistic queries, then provide specific improvement suggestions. 证据：`.claude/agents/qa-tester.md`
- **Background**（documentation）：Implement production-ready Agency Swarm v1.0.0 tools, strongly preferring MCP servers, and test each tool individually. 证据：`.claude/agents/tools-creator.md`
- **Please read this first**（documentation）：- Have you read the docs? Agency Swarm docs https://agency-swarm.ai/ - Have you searched for related issues? Others may have faced similar issues. 证据：`.github/ISSUE_TEMPLATE/bug_report.md`
- **Please read this first**（documentation）：- Have you read the docs? Agency Swarm docs https://agency-swarm.ai/ - Have you searched for related issues? Others may have had similar requests 证据：`.github/ISSUE_TEMPLATE/feature_request.md`
- **Please read this first**（documentation）：- Have you read the docs? Agency Swarm docs https://agency-swarm.ai/ - Have you searched for related issues? Others may have had similar requests 证据：`.github/ISSUE_TEMPLATE/question.md`
- **Summary**（documentation）：- I've added new tests if relevant - I've added/updated the relevant documentation - I've run make lint and make format - I've made sure tests pass 证据：`.github/PULL_REQUEST_TEMPLATE/pull_request_template.md`
- **Instructions**（documentation）：Test instructions 证据：`tests/data/files/instructions.md`
- **Role**（documentation）：Do not do any task if you did not say to the user "Hello, I'm John Doe, your Portfolio Manager." 证据：`tests/integration/fin_agency/financial_research_agency/PortfolioManager/instructions.md`
- **Role**（documentation）：You are a professional Report Generator specialist in creating executive-ready investment reports and financial documentation. 证据：`tests/integration/fin_agency/financial_research_agency/ReportGenerator/instructions.md`
- **Role**（documentation）：You are a specialized Risk Analyst expert in investment risk assessment and portfolio risk management. 证据：`tests/integration/fin_agency/financial_research_agency/RiskAnalyst/instructions.md`
- **Docs**（structured_config）：{ "$schema": "https://mintlify.com/docs.json", "theme": "maple", "name": "Agency Swarm", "colors": { "primary": " fcd53b", "light": " fcd53b", "dark": " B76E00" }, "favicon": "/images/favicon.svg", "navigation": { "tabs": { "tab": "Framework", "global": { "anchors": { "anchor": "Discord Community", "href": "https://discord.gg/cw2xBaWfFM", "icon": "discourse" }, { "anchor": "Changelog", "href": "https://github.com/VRSEN/agency-swarm/releases", "icon": "timeline" } }, "groups": { "group": "Welcome", "pages": "welcome/overview", "welcome/ai-agency-vs-other-frameworks", { "group": "Get Started", "icon": "rocket", "pages": "welcome/installation", "welcome/getting-started/starter-template", "welc… 证据：`docs/docs.json`
- **Openapi**（structured_config）：{ "openapi": "3.0.3", "info": { "title": "Agencii Platform API", "version": "1.0.0", "description": "Reference documentation for the Agencii Platform API. Provides endpoints allowing you to run your agents on custom backends or on other unsupported channels. ⚡ Live Postman Example: https://www.postman.com/vrsen-ai/agencii-api/overview" }, "servers": { "url": "https://agency-swarm-app-japboyzddq-uc.a.run.app", "description": "Production server" } , "components": { "securitySchemes": { "BearerAuth": { "type": "http", "scheme": "bearer", "bearerFormat": "JWT", "description": "Platform token required for authentication. Find or create one inside Profile Icon API Keys. Example: Bearer sk-agencii… 证据：`docs/openapi.json`
- **Tsconfig**（structured_config）：{ "compilerOptions": { "target": "ES2020", "module": "commonjs", "lib": "ES2020" , "types": "node" , "outDir": "./dist", "rootDir": "./", "strict": true, "esModuleInterop": true, "skipLibCheck": true, "forceConsistentCasingInFileNames": true, "resolveJsonModule": true, "declaration": true, "declarationMap": true, "sourceMap": true }, "include": "src/agency swarm/cli/utils/generate-agent-from-settings.ts" , "exclude": "node modules", "dist" } 证据：`tsconfig.json`
- **Model Prices And Context Window**（structured_config）：{ "sample spec": { "code interpreter cost per session": 0.0, "computer use input cost per 1k tokens": 0.0, "computer use output cost per 1k tokens": 0.0, "deprecation date": "date when the model becomes deprecated in the format YYYY-MM-DD", "file search cost per 1k calls": 0.0, "file search cost per gb per day": 0.0, "input cost per audio token": 0.0, "input cost per token": 0.0, "litellm provider": "one of https://docs.litellm.ai/docs/providers", "max input tokens": "max input tokens, if the provider specifies it. if not default to max tokens", "max output tokens": "max output tokens, if the provider specifies it. if not default to max tokens", "max tokens": "LEGACY parameter. set to max o… 证据：`src/agency_swarm/data/model_prices_and_context_window.json`
- **Components**（structured_config）：{ "$schema": "https://ui.shadcn.com/schema.json", "style": "new-york", "rsc": true, "tsx": true, "tailwind": { "config": "", "css": "app/globals.css", "baseColor": "neutral", "cssVariables": true, "prefix": "" }, "aliases": { "components": "@/components", "utils": "@/lib/utils", "ui": "@/components/ui", "lib": "@/lib", "hooks": "@/hooks" }, "iconLibrary": "lucide" } 证据：`src/agency_swarm/ui/demos/copilot/components.json`
- **Tsconfig**（structured_config）：{ "compilerOptions": { "target": "ES2017", "lib": "dom", "dom.iterable", "esnext" , "allowJs": true, "skipLibCheck": true, "strict": true, "noEmit": true, "esModuleInterop": true, "module": "esnext", "moduleResolution": "bundler", "resolveJsonModule": true, "isolatedModules": true, "jsx": "preserve", "incremental": true, "plugins": { "name": "next" } , "paths": { "@/ ": "./ " } }, "include": "next-env.d.ts", " / .ts", " / .tsx", ".next/types/ / .ts" , "exclude": "node modules" } 证据：`src/agency_swarm/ui/demos/copilot/tsconfig.json`
- **Generated Data**（structured_config）：{"C72aUUla9W": "GFp2jqKZlBCJpwANZlHZBK4KxtAUQSL22PlnKil17U4DY1OzAP", "fIZ5sGdtDr": "G9rfk7kn7Np7ZzObJr2SWidOE1seJH0KanyGsZSt7x934gnfb0", "CCp7UfWbxS": "dtkYHMLwwyxyVvayZanPM0wOE9GopivwF76XTwA1OHpDbgxNQX", "rFNe0bCaGk": "lUMKCptIzFVdxyPTLYYPEZnnGSE6ZAXxOykKYRV5N6QJejjzpQ", "BYx7YYou1O": "B20YUQemcd6KDxJ8Ro40hvcHT2KXHEjrtE33kv1W66ZtVrco3C", "C3bgGJNfjR": "jkTQ5gBwjVWExA1jJ6LE8BDLcK6TzMJLjYhhT21lS1S6wxrQ5T", "lQD4SCdbah": "e2in1CsSWSU5OMZTVQdzSQdO23t7R8Ryr8FRYOkwsF5EdOijeq", "6OgrE4BG3U": "tFtK2jgIyAkHWoEcL7rIJwN0VYCczXxffOZo3GZ4oCuO8xkOE0", "nXUBzCFTiI": "3RNTzGe1pMghXowbMA4JAstYmWFv1x9brH6INXETkEQytbGZTs", "bJWlwCyjpX": "tAlXIOztQtP98jK10t4oPhHws66rbSHTAng7itXOYcuImeoCRp", "osOVD3sm8D": "44p… 证据：`tests/data/files/generated_data.json`
- **Pastebin**（structured_config）：{ "openapi": "3.1.0", "info": { "title": "Pastebin API", "description": "Create pastes programmatically.", "version": "v1.0.0" }, "servers": { "url": "https://pastebin.example.com" } , "paths": { "/pastes": { "post": { "operationId": "createPaste", "summary": "Create a new paste entry", "requestBody": { "required": true, "content": { "application/json": { "schema": { "type": "object", "properties": { "title": { "type": "string" }, "content": { "type": "string" }, "visibility": { "type": "string", "enum": "public", "unlisted", "private" } }, "required": "title", "content", "visibility" } } } }, "description": "Create a new paste entry" } } } } 证据：`tests/data/schemas/pastebin.json`
- **macOS Files**（source_file）：Byte-compiled / optimized / DLL files pycache / / pycache / .py cod $py.class 证据：`.gitignore`
- **.Pre Commit Config**（source_file）：repos: - repo: https://github.com/pre-commit/pre-commit-hooks rev: v6.0.0 hooks: - id: trailing-whitespace exclude: ^docs/ - id: end-of-file-fixer exclude: ^docs/ - id: check-yaml - id: check-toml - id: debug-statements language version: python3 证据：`.pre-commit-config.yaml`
- **.prettierignore**（source_file）：.mdx .md 证据：`.prettierignore`
- **.prettierrc**（source_file）：{ "tabWidth": 4, "overrides": { "files": " .yml", "options": { "tabWidth": 2 } } } 证据：`.prettierrc`
- **Makefile**（source_file）：.PHONY: sync sync: uv sync --all-extras --dev 证据：`Makefile`
- **docs/.prettierrc**（source_file）：{ "semi": true, "singleQuote": false, "tabWidth": 2, "printWidth": 120, "bracketSpacing": true, "arrowParens": "always", "trailingComma": "none" } 证据：`docs/.prettierrc`
- **Replace dot access with whitespace if detected**（source_file）：import pandas as pd import textstat 证据：`docs/analise_docs.py`
- **Then, pass these callbacks during your agency initialization to resume conversations:**（source_file）：Set your API key in your code: Or use a .env file: Then load it with: 证据：`docs/faq.mdx`
- **Make the examples directory into a package to avoid top-level module name collisions.**（source_file）：Make the examples directory into a package to avoid top-level module name collisions. This is needed so that mypy treats files like examples/customer service/main.py and examples/researcher app/main.py as distinct modules rather than both named "main". 证据：`examples/__init__.py`
- **Path setup for standalone examples**（source_file）：Simple demonstration of sharing data between agents using agency context. Shows how one agent can store data and another can retrieve it. """ 证据：`examples/agency_context.py`
- **!/usr/bin/env python3**（source_file）：!/usr/bin/env python3 """ Agency Swarm Visualization Demo 证据：`examples/agency_visualization.py`
- **Path setup for standalone examples**（source_file）：This example demonstrates how to enable file search capabilities for an agent by attaching a file storage with automatic vector store processing. 证据：`examples/agent_file_storage.py`
- **How to get Google OAuth token:**（source_file）：""" This example demonstrates how to use openai's connector feature with the agency swarm framework. 证据：`examples/connectors.py`
- **In this demo, we use a simple file for simplicity, but in production**（source_file）：This example demonstrates how to persist thread data between different sessions using callback functions. """ 证据：`examples/custom_persistence.py`
- **Path setup so the example can be run standalone**（source_file）：""" Custom SendMessage Tool with Context Example 证据：`examples/custom_send_message.py`
- **in case Agency.get response gets a list of input items, join them into a single string**（source_file）："""Input guardrails demo that delegates relevance decisions to a judge agent.""" 证据：`examples/guardrails_input.py`
- **Guardrails Output**（source_file）："""Minimal output guardrail example.""" 证据：`examples/guardrails_output.py`
- **Path setup so the example can be run standalone**（source_file）：This example demonstrates a realistic handoff workflow using Handoff. 证据：`examples/handoffs.py`
- **Launch the SSE MCP server**（source_file）：""" An example of running an agency with a local and a public MCP server. 证据：`examples/mcp_servers.py`
- **examples/message attachments.py**（source_file）：examples/message attachments.py """ Message Attachments Example 证据：`examples/message_attachments.py`
- **examples/multi agent workflow.py**（source_file）：examples/multi agent workflow.py """ Multi-Agent Collaboration Example with Validation 证据：`examples/multi_agent_workflow.py`
- 其余 13 条证据见 `AI_CONTEXT_PACK.json` 或 `EVIDENCE_INDEX.json`。

## 宿主 AI 必须遵守的规则

- **把本资产当作开工前上下文，而不是运行环境。**：AI Context Pack 只包含证据化项目理解，不包含目标项目的可执行状态。 证据：`.claude/README.md`, `AGENTS.md`, `README.md`
- **回答用户时区分可预览内容与必须安装后才能验证的内容。**：安装前体验的消费者价值来自降低误装和误判，而不是伪装成真实运行。 证据：`.claude/README.md`, `AGENTS.md`, `README.md`

## 用户开工前应该回答的问题

- 你准备在哪个宿主 AI 或本地环境中使用它？
- 你只是想先体验工作流，还是准备真实安装？
- 你最在意的是安装成本、输出质量、还是和现有规则的冲突？

## 验收标准

- 所有能力声明都能回指到 evidence_refs 中的文件路径。
- AI_CONTEXT_PACK.md 没有把预览包装成真实运行。
- 用户能在 3 分钟内看懂适合谁、能做什么、如何开始和风险边界。

---

## Doramagic Context Augmentation

下面内容用于强化 Repomix/AI Context Pack 主体。Human Manual 只提供阅读骨架；踩坑日志会被转成宿主 AI 必须遵守的工作约束。

## Human Manual 骨架

使用规则：这里只是项目阅读路线和显著性信号，不是事实权威。具体事实仍必须回到 repo evidence / Claim Graph。

宿主 AI 硬性规则：
- 不得把页标题、章节顺序、摘要或 importance 当作项目事实证据。
- 解释 Human Manual 骨架时，必须明确说它只是阅读路线/显著性信号。
- 能力、安装、兼容性、运行状态和风险判断必须引用 repo evidence、source path 或 Claim Graph。

- **Agency Swarm 简介**：importance `high`
  - source_paths: README.md, src/agency_swarm/__init__.py, pyproject.toml
- **安装与配置**：importance `high`
  - source_paths: pyproject.toml, Makefile, CONTRIBUTING.md
- **系统架构**：importance `high`
  - source_paths: src/agency_swarm/agency/core.py, src/agency_swarm/agent/core.py, src/agency_swarm/tools/base_tool.py, src/agency_swarm/messages/message_formatter.py
- **项目目录结构**：importance `medium`
  - source_paths: src/agency_swarm, examples, docs
- **智能体 (Agent)**：importance `high`
  - source_paths: src/agency_swarm/agent/core.py, src/agency_swarm/agent/tools.py, src/agency_swarm/agent/execution.py, src/agency_swarm/agent/file_manager.py
- **代理组织 (Agency)**：importance `high`
  - source_paths: src/agency_swarm/agency/core.py, src/agency_swarm/agency/setup.py, src/agency_swarm/agency/helpers.py
- **通信流程**：importance `high`
  - source_paths: src/agency_swarm/agent/agent_flow.py, src/agency_swarm/tools/send_message.py, examples/custom_send_message.py, examples/handoffs.py
- **自定义工具开发**：importance `high`
  - source_paths: src/agency_swarm/tools/base_tool.py, src/agency_swarm/tools/tool_factory.py, src/agency_swarm/tools/function_tool_compat.py, examples/tools.py

## Repo Inspection Evidence / 源码检查证据

- repo_clone_verified: true
- repo_inspection_verified: true
- repo_commit: `32bca5e4d69c8781d6d3dbd697d4231863c9564b`
- inspected_files: `pyproject.toml`, `package.json`, `README.md`, `uv.lock`, `docs/openapi.json`, `docs/docs.json`, `docs/analise_docs.py`, `docs/faq.mdx`, `docs/migration/guide.mdx`, `docs/platform/additional-instructions.mdx`, `docs/platform/pricing.mdx`, `docs/platform/how-credits-work.mdx`, `docs/platform/overview.mdx`, `docs/contributing/contributing.mdx`, `docs/additional-features/azure-openai.mdx`, `docs/additional-features/agency-context.mdx`, `docs/additional-features/few-shot-examples.mdx`, `docs/additional-features/mcp-tools-server.mdx`, `docs/additional-features/deployment-to-production.mdx`, `docs/additional-features/third-party-models.mdx`

宿主 AI 硬性规则：
- 没有 repo_clone_verified=true 时，不得声称已经读过源码。
- 没有 repo_inspection_verified=true 时，不得把 README/docs/package 文件判断写成事实。
- 没有 quick_start_verified=true 时，不得声称 Quick Start 已跑通。

## Doramagic Pitfall Constraints / 踩坑约束

这些规则来自 Doramagic 发现、验证或编译过程中的项目专属坑点。宿主 AI 必须把它们当作工作约束，而不是普通说明文字。

### Constraint 1: 来源证据：Chart Library tool for financial pattern analysis in agent swarms

- Trigger: GitHub 社区证据显示该项目存在一个安装相关的待验证问题：Chart Library tool for financial pattern analysis in agent swarms
- Host AI rule: 来源问题仍为 open，Pack Agent 需要复核是否仍影响当前版本。
- Why it matters: 可能增加新用户试用和生产接入成本。
- Evidence: community_evidence:github | cevd_736c9d770ee34419ad2476f2a973e433 | https://github.com/VRSEN/agency-swarm/issues/596 | 来源讨论提到 python 相关条件，需在安装/试用前复核。
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 2: 来源证据：Feature request: native advisor/executor consult flow for stronger-model escalation

- Trigger: GitHub 社区证据显示该项目存在一个安装相关的待验证问题：Feature request: native advisor/executor consult flow for stronger-model escalation
- Host AI rule: 来源问题仍为 open，Pack Agent 需要复核是否仍影响当前版本。
- Why it matters: 可能增加新用户试用和生产接入成本。
- Evidence: community_evidence:github | cevd_1b01977e66ac46caa8a8b860da5bdafe | https://github.com/VRSEN/agency-swarm/issues/598 | 来源讨论提到 python 相关条件，需在安装/试用前复核。
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 3: 来源证据：Proposal: ClawMem adapter for thread persistence across sessions

- Trigger: GitHub 社区证据显示该项目存在一个安装相关的待验证问题：Proposal: ClawMem adapter for thread persistence across sessions
- Host AI rule: 来源问题仍为 open，Pack Agent 需要复核是否仍影响当前版本。
- Why it matters: 可能增加新用户试用和生产接入成本。
- Evidence: community_evidence:github | cevd_3bb24559ba48467ab0c8d43d3069d7f1 | https://github.com/VRSEN/agency-swarm/issues/594 | 来源类型 github_issue 暴露的待验证使用条件。
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 4: 来源证据：CI-level governance checks for swarm agent code

- Trigger: GitHub 社区证据显示该项目存在一个安装相关的待验证问题：CI-level governance checks for swarm agent code
- Host AI rule: 来源显示可能已有修复、规避或版本变化，说明书中必须标注适用版本。
- Why it matters: 可能增加新用户试用和生产接入成本。
- Evidence: community_evidence:github | cevd_b995c0dfb8a5460caa7cfde16ac1c7a4 | https://github.com/VRSEN/agency-swarm/issues/593 | 来源类型 github_issue 暴露的待验证使用条件。
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 5: 来源证据：Feature: Runtime governance and compliance audit trails

- Trigger: GitHub 社区证据显示该项目存在一个安装相关的待验证问题：Feature: Runtime governance and compliance audit trails
- Host AI rule: 来源显示可能已有修复、规避或版本变化，说明书中必须标注适用版本。
- Why it matters: 可能增加新用户试用和生产接入成本。
- Evidence: community_evidence:github | cevd_4bd751455da0479bb37a014ef50934dd | https://github.com/VRSEN/agency-swarm/issues/592 | 来源类型 github_issue 暴露的待验证使用条件。
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 6: 来源证据：v1.9.0 - Agent Swarm TUI and OpenClaw

- Trigger: GitHub 社区证据显示该项目存在一个安装相关的待验证问题：v1.9.0 - Agent Swarm TUI and OpenClaw
- Host AI rule: 来源显示可能已有修复、规避或版本变化，说明书中必须标注适用版本。
- Why it matters: 可能增加新用户试用和生产接入成本。
- Evidence: community_evidence:github | cevd_445071ada1ba4d558d4ebea6ec395364 | https://github.com/VRSEN/agency-swarm/releases/tag/v1.9.0 | 来源讨论提到 python 相关条件，需在安装/试用前复核。
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 7: 来源证据：v1.8.0 — Present and Accounted For

- Trigger: GitHub 社区证据显示该项目存在一个配置相关的待验证问题：v1.8.0 — Present and Accounted For
- Host AI rule: 来源显示可能已有修复、规避或版本变化，说明书中必须标注适用版本。
- Why it matters: 可能影响升级、迁移或版本选择。
- Evidence: community_evidence:github | cevd_d270ab8e87c945878e308b78a2c8e7e6 | https://github.com/VRSEN/agency-swarm/releases/tag/v1.8.0 | 来源类型 github_release 暴露的待验证使用条件。
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 8: 来源证据：v1.9.2

- Trigger: GitHub 社区证据显示该项目存在一个配置相关的待验证问题：v1.9.2
- Host AI rule: 来源显示可能已有修复、规避或版本变化，说明书中必须标注适用版本。
- Why it matters: 可能增加新用户试用和生产接入成本。
- Evidence: community_evidence:github | cevd_2e69c962dcc44fd5a160047df0f18192 | https://github.com/VRSEN/agency-swarm/releases/tag/v1.9.2 | 来源类型 github_release 暴露的待验证使用条件。
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 9: 来源证据：v1.9.5

- Trigger: GitHub 社区证据显示该项目存在一个配置相关的待验证问题：v1.9.5
- Host AI rule: 来源显示可能已有修复、规避或版本变化，说明书中必须标注适用版本。
- Why it matters: 可能增加新用户试用和生产接入成本。
- Evidence: community_evidence:github | cevd_ec6832c5bd7b4083b4dd1a68c50f666f | https://github.com/VRSEN/agency-swarm/releases/tag/v1.9.5 | 来源类型 github_release 暴露的待验证使用条件。
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 10: 能力判断依赖假设

- Trigger: README/documentation is current enough for a first validation pass.
- Host AI rule: 将假设转成下游验证清单。
- Why it matters: 假设不成立时，用户拿不到承诺的能力。
- Evidence: capability.assumptions | github_repo:719367294 | https://github.com/VRSEN/agency-swarm | README/documentation is current enough for a first validation pass.
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

