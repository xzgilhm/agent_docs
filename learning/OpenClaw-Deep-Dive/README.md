# OpenClaw Deep Dive

这一组笔记进入更技术、偏底层、偏命令行/运维的 OpenClaw 学习视角。

前一组内容更偏“把系统看懂”；这一组开始回答：

- 一个请求进入系统后，具体落在哪个 runtime 骨架里？
- session 为什么是 OpenClaw 的真正中枢，而不只是聊天历史？
- tool call 在底层是怎么被调度、执行、回填的？
- gateway / node / provider / channel 到底分别位于哪一层？
- 运维视角下，应该如何观察、诊断、验证一个 OpenClaw 实例？

---

## 学习目标

学完这一组后，你应该能做到：

- 从“执行引擎”视角解释 OpenClaw，而不是只会描述表层功能
- 看懂 session、runtime、tool loop、memory、subagent、ACP 的层次关系
- 知道常见命令行入口和排障思路
- 形成偏运维/工程化的理解，而不是停留在概念记忆

---

## 建议阅读顺序

1. [01 - Runtime、Session 与 Tool Call Stack](./01-runtime-session-tool-call-stack.md)
2. [02 - Gateway、Node、Provider 与 Channel 分层](./02-gateway-node-provider-channel.md)
3. 03 - Subagent 与 ACP 的执行模型
4. 04 - Memory 检索与上下文装配
5. 05 - OpenClaw 命令行与运维观察面
6. 06 - 权限、安全、审批与隔离边界
7. 07 - 后台任务、detached work 与持久化执行

---

## 这一组和上一组的区别

上一组更像“产品/架构总览”：

- OpenClaw 是什么
- 有哪些核心组件
- 一次请求如何从输入走到输出

这一组更像“系统骨架 + 运维观察视角”：

- runtime 内部有哪些稳定抽象
- 为什么 session 才是主轴
- 为什么 tool 调用不是“模型直接执行 shell”
- 为什么 ACP 和 subagent 看起来相近，但本质是不同执行模型
- 运维排障时，应该先看哪层，再看哪层
