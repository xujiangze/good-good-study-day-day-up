# 🚀 核心概念简介
## 🌀 什么是 Vibe Coding（凭感觉编码）

Vibe Coding 是一种快速与 AI 交互、凭直觉与自然语言 prompt 让 AI 生成可运行代码的开发风格。

开发者像导演一样：描述想要什么 → AI 生成实现 → 运行并修正

不专门写详细规范，只在 prompt 里带上需求与上下文

- 优点：启动快、适合原型
- 缺点：缺乏可维护性、协作难、易丢失长期上下文，与 AI 生成的代码质量不稳定

比喻：
Vibe Coding 就像“去陌生城市旅游只凭兴致而不做攻略”，可能玩的很爽，但很容易迷路。

## 📋 什么是 SDD（规格驱动开发）

规格驱动开发（SDD） 是一种先写规范、再让 AI 自动用规范驱动代码实现的开发方法。
核心思想：
- 规范是唯一事实源
- 代码只是规范的实现产物
- AI 作为执行引擎，实现、任务拆分、测试生成

效果: SDD 让开发变得可重复、可验证、可协作

比喻：
先制定详细作战地图与任务手册，再让队伍（AI）按计划执行，而不是战场上凭感觉乱打。

# 🆚 Vibe Coding 与 SDD 横向对比
| 维度     | Vibe Coding  | SDD     |                  |
| ------ | ------------ | ------- | ---------------- |
| 启动速度   | 🚀 很快        | ⏱️ 较慢   |                  |
| 输入形式   | 自然语言 prompt  | 结构化规范   |                  |
| 可维护性   | ❌ 低          | ✅ 高     |                  |
| 协作友好   | ❌ 差          | ✅ 好     |                  |
| 可重复性   | ❌ 差          | ✅ 好     |                  |
| 团队可扩展性 | ❌ 弱          | ✅ 强     |                  |
| 可靠性    | 🟡 依赖 prompt | 🟢 依赖规范 | ([Vibe Vibe][1]) |

[1]: https://www.vibevibe.cn/Basic/01-awakening/1.2-vibe-vs-spec/1.2.2-what-is-spec-Coding.html?utm_source=chatgpt.com "1.2.2 什么是 Spec Coding（规范驱动开发） | Vibe Coding 全栈实战教程"

# 🧠 SDD 方法论：是什么？为什么？怎么做？
## 🧩 是什么（What）

SDD 是一种以规格为中心的工程化开发方法，规范不是“参考文档”，而是驱动实现的源泉。
核心理念：规范定义WHAT（做什么） + WHY（为什么） → 代码做 HOW（怎么做） 的最后一公里

## 🤔 为什么（Why）
- 提升 可预测性：不是凭 prompt 交互，而是规范驱动 AI 生成代码
- 降低 上下文丢失风险：规范版本可感知全项目意图
- 支持 团队协作与审查：人人可读、review、版本追踪
- 提高 可扩展性和可维护性：规范可持续演化而不是遗忘

## ⚙️ 怎么做（How）
SDD 的核心流程是：
- Specify — 写出规范文件（需求 + 目标 + 前置条件）
- Plan — 设定技术栈与高层架构计划
- Tasks — 将 plan 转成可执行任务列表
- Implement — 用 AI 或自动化执行任务并生成代码
工具链或流程可以用 CLI 或平台集成来驱动这些步骤，让 AI 扮演不同角色来执行

# 🧭 SDD 的四种哲学路径与核心对比
## 1️⃣ BMAD‑METHOD

哲学路径：Agent‑centric Agile AI 开发

GitHub 仓库：
🔗 https://github.com/bmad-code-org/BMAD-METHOD
 
Redreamality's Blog

### 🧠 核心理念
采用多 AI 角色协作方式，例如 Analyst、PM、Architect 等
强调从 宏观规划 → 架构 → 细化任务 再到细节实现的规范流程

- ✨ 适用场景
适合大项目、复杂需求、团队协作
强调团队协作与上下文保持

- 🧠 比喻
就像构建一个工程项目，先由策划、架构师、项目经理分别制定方案、蓝图与任务书，再逐层分发。

## 2️⃣ GitHub Spec‑Kit
哲学路径：可执行规范 + 规范驱动 CLI 工具

GitHub 仓库：
🔗 https://github.com/github/spec-kit

- 🧠 核心理念
GitHub 官方推出的 SDD 工具箱
强调规范可执行、可生成实现计划和任务
specify, plan, tasks 等 CLI 命令驱动全流程

- ✨ 使用情况
社区活跃，有 20k+ stars
支持多家 AI agent（Claude Code，Copilot，Cursor 等）

- 🧠 比喻
就像一个具备命令行执行脚本的蓝图工厂，从规格模板开始一步步自动推进项目执行。

## 3️⃣ OpenSpec
哲学路径：轻量化 Brownfield 优先规范工具

GitHub 仓库：
🔗 https://github.com/Fission-AI/OpenSpec


- 🧠 核心理念
轻量规范优先协议
对现有代码库维护与更新友好（Brownfield first）
将规范与“变更提案（changes）”分开管理，以便于演进

- ✨ 适用场景
适合在已有项目上逐步引入 SDD 流程
更关注规范的版本管理、变更可审计性

- 🧠 比喻
就像版本控制下的规范快照，团队在每个改动前“提出规范”，类似 PR 概念。

## 4️⃣ PromptX

哲学路径：AI 角色 + 记忆 + 交互式上下文平台
GitHub 仓库：
🔗 https://github.com/Deepractice/PromptX

- 🧠 核心理念
提供一个AI context 平台
不局限于“规范就是开发核心”，而是提供“AI 角色、记忆网络、工具集成”

PromptX 更像 AI 团队协作、专家角色抽象化的平台，强调持续上下文与专业角色定位
GitHub

- ✨ 使用情况
社区较新、适合广泛 AI 协作与角色系统构建
可为 SDD 提供记忆与角色支持，但规范本身不是唯一核心

- 🧠 比喻
就像有一个 AI 助手平台，能让你切换专业角色（产品经理、策略专家、架构专家）协助完成 SDD 流程。

## 📊 四种路径横向比较
| 特性     | BMAD      | Spec‑Kit | OpenSpec      | PromptX   |
| ------ | --------- | -------- | ------------- | --------- |
| 核心哲学   | 多 AI 角色协作 | 规范驱动流程   | 规范可演化         | 角色 + 记忆体系 |
| 优势     | 高组织级协作    | 结构化规范模板  | Brownfield 友好 | 上下文与角色存储  |
| 规范中心   | 是         | 是        | 是             | 否（更泛）     |
| 项目规模适应 | 大         | 中大       | 中到大           | 灵活（不限项目）  |
| 学习成本   | 高         | 中        | 中             | 低（平台）     |

# 🧠 结论：SDD 的可靠性与哲学意义
SDD 的核心可靠性源于：
- 强调明确的 WHAT / WHY 规范，而不是凭感觉生成的 HOW
- 为 AI 提供“清晰上下文与不可变事实源”
- 支持团队版本化协作、质量控制与长期维护
- 能在复杂项目中降低重复解释成本，提高一致性

比喻总结：
- Vibe Coding 是“凭直觉航行”，
- SDD 是“拿着指南针和地理图航海”。

# 📌 参考链接
- GitHub Spec‑Kit: https://github.com/github/spec-kit
- GitHub OpenSpec: https://github.com/Fission-AI/OpenSpec
- GitHub BMAD‑METHOD: https://github.com/bmad-code-org/BMAD-METHOD
- GitHub PromptX: https://github.com/Deepractice/PromptX
 
