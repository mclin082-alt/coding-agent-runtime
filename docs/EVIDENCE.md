# Codex 源码研究：公开证据清单

[返回项目首页](../README.md) · [自主实现 Forge Agent](https://github.com/mclin082-alt/forge-agent)

核查日期：2026-10-14。基准代码：`5d301b1e8e860a79536ff3c1279245fdc025e97b`。该版本 Git 跟踪文件只有 `README.md`，没有源码阅读笔记、实验脚本、trace、截图、测试或安装入口。本次新增的展示文档只是证据清单，不是补造实验结果。

## 原记录与证据状态

| 原 README 中的进展 | 目前能核对的内容 | 展示方式 |
| --- | --- | --- |
| 已完成第一轮 Codex CLI runtime/provider contract 阅读 | [原 README 固定版本](https://github.com/mclin082-alt/coding-agent-runtime/blob/5d301b1e8e860a79536ff3c1279245fdc025e97b/README.md) 的作者自述 | 保留为历史自述；需源码 commit、文件路径和阅读判断支持 |
| 可复用 EVN provider profile 本地已验证 | 没有公开 profile、运行命令或脱敏输出 | 待补材料；不将配置宣称为可直接复现的交付 |
| 使用 Codex CLI 完成受约束代码修复，本地已验证 | 没有该实验的输入、前后测试、diff 或 Rollout | 待补原始记录；不借用 Forge/Enterprise 的结果代替 |
| Runtime trace 与研究笔记整理中 | 尚未公开 | 仍列待补 |
| 真实业务系统集成 | 原记录未声称完成 | 不增加完成声明 |

[OpenAI Codex](https://github.com/openai/codex) 是研究对象；上游代码、功能和测试数字都不能算作个人实现成果。[Forge Agent](https://github.com/mclin082-alt/forge-agent) 展示项目自有 runtime；[Enterprise AI Workspace](https://github.com/mclin082-alt/enterprise-ai-workspace) 展示官方 SDK 集成。两者有各自证据，不能证明本仓库未公开的研究过程。

## 发布一份可复核研究材料所需内容

1. **问题与判断：** 选择一条调用链，例如 prompt → context → sampling → tool result；标明上游 commit 与源码路径，说明自己的分析。
2. **实验与结果：** 写清任务、环境、模型/provider、命令和预期；附实际观察、测试输出、diff 与失败情况。敏感配置仅保留字段名。
3. **可阅读证据：** 提供经脱敏审阅的 trace 摘要、截图或短演示，并注明适用范围与未验证项。

这些是待补清单，当前不声称已有。建议先完整公开一个可复核实验，再扩展研究范围。

## 本次验证范围

完成了文件清单、历史 README 与导航链接的核对。没有可运行测试，本次也未 clone、构建或运行官方 Codex 来制造新的研究结果。研究成效与可复现性仍待上述材料支持。
