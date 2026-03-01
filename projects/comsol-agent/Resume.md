**COMSOL Agent 智能仿真建模 Agent**
2025.11-至今

**技术选型：** Python, TypeScript, Rust, Tauri 2, React, COMSOL Java API, LLM (Qwen/DeepSeek/OpenAI)

**项目描述：** 一个基于 ReAct（推理与行动）架构的 AI 仿真建模智能体，将自然语言描述的 COMSOL Multiphysics 建模需求自动转换为完整的 .mph 模型文件。核心由 Python 后端引擎与 Tauri 2 + React 桌面应用组成：后端实现多模块 Agent 系统（规划层、执行层、观察层），支持自然语言解析 → 建模步骤规划 → COMSOL Java API 调用 → 结果观察与迭代的完整闭环；前端提供友好的交互界面、实时推理展示、LLM 与 COMSOL 环境配置、对话历史与摘要式记忆等功能。支持多个 LLM 后端（Qwen、DeepSeek、OpenAI、Ollama 等），一键生成可在 COMSOL 中直接打开的仿真模型。

**责任描述：**

1. **Agent 架构设计**：基于 ReAct 模式实现推理 → 行动 → 观察 → 迭代的闭环，通过 SessionOrchestrator 管理多个独立 Agent（Geometry、Physics、Material、Study），每个 Agent 负责特定建模阶段的规划与执行。
2. **自然语言理解**：实现 ReasoningEngine 进行需求理解与建模步骤规划，生成结构化的 Plan 对象（GeometryPlan、PhysicsPlan、StudyPlan 等），支持多轮对话与上下文记忆。
3. **COMSOL 集成**：设计 COMSOLRunner、JavaAPIController 等模块，直接调用 COMSOL Java API，支持几何创建（矩形、圆形、椭圆、多边形等）、物理场设置、网格划分、研究与求解的完整流程。
4. **桌面应用开发**：基于 Tauri 2 + React + TypeScript 构建跨平台桌面应用，实现模型编辑框、参数输入、实时推理过程展示、记忆管理、LLM 与 COMSOL 配置面板、主题切换等交互功能。
5. **工程化与部署**：使用 PyInstaller 打包 Python 后端，集成 Java 11 运行时，构建 Windows 安装包（exe/msi），通过 GitHub Actions 自动化发布流程，提供开箱即用的桌面应用体验。