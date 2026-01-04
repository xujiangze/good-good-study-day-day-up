# OpenSpec
https://github.com/Fission-AI/OpenSpec

# 为什么选他
- 日常工作中, 负责的项目并不总是新项目, 对旧项目的改造是常态.
- 需要多方合作
- 官方介绍的
  - 规范化: 在工作开始前，人类和人工智能相关人员需就技术规范达成一致。 
  - 可审计: 结构化的变更文件夹（提案、任务和规范更新）使范围明确且可审计。 
  - 可见性: 共享对已提议、正在进行或已存档内容的可见性。 
  - 工具友好: 可与您已使用的 AI 工具配合使用：在支持自定义斜杠命令的地方使用自定义斜杠命令，在其他所有地方使用上下文规则。

# 怎么用.
参考: https://github.com/Fission-AI/OpenSpec?tab=readme-ov-file#getting-started
- 真理语录 
  - 有调研才有发言权, 实践检验真理. 
  - 先用起来, 感受它, 再来优化他

视频学习教程(我在哔哩哔哩上大学~): 
https://www.bilibili.com/video/BV1fFWJztEAu/?spm_id_from=333.337.search-card.all.click&vd_source=5e99f964f1e3155ce2aefef8e7780b39

# 实践
下述为我自己个人的实践, 仅供参考

## Claude Code 使用
- npm 安装openspec
```bash
npm install -g @fission-ai/openspec@latest
```
- 在根目录下使用如下指令, 并选择Claude Code
```bash
openspec init
```

根据提示在claude code上输入如下内容, 让Claude Code能够读懂我们现有项目
```
1. Populate your project context:
   "Please read openspec/project.md and help me fill it out
    with details about my project, tech stack, and conventions"

2. Create your first change proposal:
   "I want to add [YOUR FEATURE HERE]. Please create an
    OpenSpec change proposal for this feature"

3. Learn the OpenSpec workflow:
   "Please explain the OpenSpec workflow from openspec/AGENTS.md
    and how I should work with you on this project"
```
