# Codex Runtime Research

这是一个面向 **coding agent runtime** 的个人研究项目。我通过源码阅读、local run 和可复现实验，理解 Codex 如何把用户任务转化为 context、model inference、tool call、文件修改与验证结果。

> 当前仓库只保留项目入口。研究记录和可复现 evidence 会在完成后逐步公开，不把 OpenAI Codex 的完整源码重复上传到本仓库。

## 我在研究什么

1. **Runtime loop**：一次 task 如何经过 turn、sampling、tool execution 和 result handling。
2. **Context engineering**：指令、历史消息、工具结果与压缩后的 context 如何进入下一次 inference。
3. **Tool safety**：文件修改、命令执行、approval 和 sandbox 如何共同限制 agent 行为。
4. **Provider compatibility**：Codex CLI 如何通过 Responses API 接入不同 model provider。
5. **Evaluation evidence**：如何区分“模型给出了回答”和“runtime 确实完成并验证了任务”。

## 当前进展

| 内容 | 状态 | Evidence 类型 |
| --- | --- | --- |
| Codex CLI runtime 与 provider contract 阅读 | 已完成第一轮 | Source reading |
| 可复用 EVN provider profile | 本地已验证 | Local configuration |
| 使用 Codex CLI 完成受约束代码修复 | 本地已验证 | Test result + file-scope check |
| Runtime trace 与研究笔记 | 整理中 | 待公开 |
| 真实业务系统集成 | 未声称完成 | — |

这里的“本地已验证”只代表在指定环境中完成过实际运行，不等同于 production deployment 或通用兼容性证明。

## Upstream

本项目的源码研究对象是 [OpenAI Codex](https://github.com/openai/codex)。

本仓库不是 Codex 的镜像、二次分发或官方文档。需要查看、构建或跟踪源码时，请直接使用官方仓库；本仓库只记录我自己的研究问题、实验过程、结论与边界。

## 后续公开内容

后续材料会在具备独立验证价值后再加入，包括：

- runtime 调用链笔记；
- 脱敏后的 trace 与关键事件；
- 可复制的运行命令、输入和预期输出；
- 成功标准、失败记录与适用边界；
- coding agent 在真实业务 workflow 中的最小实验。
