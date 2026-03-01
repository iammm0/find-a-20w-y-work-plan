**PhysicistsCard 面向研究者的协作平台**
2025.05-至今

**技术选型：** TypeScript, Next.js, React, Go, Gin, MySQL, Redis, Tailwind CSS, Radix UI, Docker Compose

**项目描述：** 一个完整的研究者社区协作平台，通过"动态-仓库-里程碑"的三层级结构，帮助研究者从思想交流沉淀到成熟的研究项目。前端基于 Next.js + TypeScript 构建高性能 SSR 应用，实现认证、动态发布、项目管理、协作等交互功能；后端采用 Go + Gin 微服务架构，拆分为 Auth、Collab、Feed、Beta、Media、Cardstore、Admin 七个独立服务，通过 MySQL + Redis 实现数据持久化与缓存，Docker Compose 统一编排部署，Swagger 自动化文档。

**责任描述：**

1. **前端架构**：基于 Next.js + TypeScript 构建完整前端系统，实现用户认证、个人资料、动态发布、项目创建与管理、里程碑追踪、团队协作等功能模块的页面与交互。
2. **项目管理系统**：设计灵活的项目管理功能，支持项目基础配置、学科领域/分类/状态/预算等多维度分类、里程碑记录、Git 仓库/文档/数据集等资源关联、协作者权限管理。
3. **前端工程化**：自定义 React Hooks 层（useAuth、usePosts、useProjects 等）统一 API 调用逻辑；采用 Radix UI + Tailwind CSS 实现响应式、无障碍的现代化 UI；处理多结构数据兼容性与即时渲染。
4. **后端微服务**：设计七模块微服务架构，Auth 服务提供 JWT 认证与用户管理、Feed 服务支持动态发布/评论/点赞/分享、Media 服务支持文件上传、Cardstore 服务实现商品/订单/支付、Collab 服务管理项目与团队协作。
5. **数据与部署**：基于 MySQL 建立关键业务表（Post、Attachment、Like、Comment、Order 等），Redis 缓存优化查询性能，Docker Compose 统一编排，Swagger 自动生成 API 文档。