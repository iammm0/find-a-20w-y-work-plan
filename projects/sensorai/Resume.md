**Sensor-AI 智能体**                                                                                                                      

技术选型：**Python、FastAPI、LangChain、MongoDB、Qdrant、Ollama、React Native、Expo、Docker**

**项目描述**：多课程 AI 智能体系统，包括后端 API 服务与移动/Web 前端应用。采用 LangChain 与 FastAPI 实现多课程 AI 助手与 RAG 检索增强生成，支持按课程隔离的知识库与系统提示词，提供文档解析、向量搜索、多模式对话等功能。前端基于 React Native（Expo）与 Next.js 实现，统一接入同一后端，提供 Web 与移动端原生体验。

**责任描述**：

1. **后端服务开发**：基于 FastAPI 与 LangChain 实现 AI 助手框架，设计路由层（用户、认证、邮件、资源等）、数据库层（MongoDB 数据存储）、服务层（Agent 工作流、RAG 检索）。
2. **知识库与检索**：构建向量数据库（Qdrant）与文档解析系统（多格式支持），实现 RAG 知识检索与语义搜索，支持多课程独立知识库隔离。
3. **数据持久化**：使用 MongoDB 存储用户数据、对话记录、资源管理，使用 Redis 做会话缓存与检索辅助。
4. **认证与安全**：实现 JWT 认证、用户管理、权限控制、邮件通知等安全机制。
5. **Web 前端开发**：使用 Next.js 与 React 开发 Web 管理端，实现对话界面、知识库管理、用户管理等功能。
6. **移动端开发**：使用 React Native（Expo）开发跨平台移动应用，与 Web 端共享业务逻辑与 API 调用。
7. **工程化**：Docker 容器化部署、自动化测试、开发工具集成（ESLint、TypeScript）。