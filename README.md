# Coding Agent · Codex 源码研究与实验

**围绕代码修复任务，研究 Agent 如何利用上下文、工具结果和验证反馈推进任务。**

我关注任务输入到最终结果之间的执行机制：模型依据什么决定下一步，操作受到哪些约束，以及怎样确认任务已经完成。这个仓库记录源码研究方向与实验整理进度，与 [Forge Agent 的自主实现](https://github.com/mclin082-alt/forge-agent) 相互关联。

当前公开成果是研究问题与进展入口。历史说明记录过源码阅读和本地运行实验，对应笔记、脚本与执行轨迹尚未公开。

## 研究重点

| 研究问题 | 关注内容 |
| --- | --- |
| Agent 怎样根据反馈调整行动 | 上下文组织、模型与工具调用衔接、失败结果如何影响后续决策 |
| 怎样控制操作范围 | 工具权限、具体动作审批与 sandbox 的执行边界 |
| 怎样判断任务完成 | 代码变化、前后测试、执行轨迹与结果验收的对应关系 |

## 目前可核对的材料

1. [原始项目进展记录](https://github.com/mclin082-alt/coding-agent-runtime/blob/5d301b1e8e860a79536ff3c1279245fdc025e97b/README.md)：保留当时的源码阅读与本地实验自述，未附独立验收产物。
2. [公开证据清单](docs/EVIDENCE.md)：列出已有内容、材料缺口与后续整理要求。

研究对象是 [官方 OpenAI Codex](https://github.com/openai/codex)。2026-10-14 的仓库核查仅确认公开文件与说明，没有执行新的 runtime 实验。

## 研究、实现与集成

| 项目 | 我的工作定位 |
| --- | --- |
| 本仓库 | 源码阅读、机制分析与实验整理 |
| [Forge Agent](https://github.com/mclin082-alt/forge-agent) | 自主实现小型 Coding Agent，并验证修复、审批与回放流程 |
| [Enterprise AI Workspace](https://github.com/mclin082-alt/enterprise-ai-workspace) | 基于官方 SDK/runtime 实现任务服务与只读资料接入 |

各项目的贡献和验收结果分别记录，官方 Codex 的实现属于研究对象。

## 待补材料

- 带源码版本、关键路径和个人分析的阅读笔记。
- 包含任务输入、运行命令、前后测试、改动与结论的完整实验记录。
- 经脱敏的执行轨迹，以及截图或短 Demo。

当前仓库尚无可独立复核的研究实验产物，研究过程与结论仍需这些材料支持。可运行的自主实现及其验收记录见 [Forge Agent](https://github.com/mclin082-alt/forge-agent)。
