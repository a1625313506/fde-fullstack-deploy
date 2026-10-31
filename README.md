# 🤖 FDE 全栈 AI 智能对话助手 (Fullstack AI Assistant)

基于 React + FastAPI + 智谱 GLM-4 构建的现代化 AI 聊天应用。支持流式打字机输出、Markdown 代码高亮、多会话上下文隔离与持久化存储，并已实现 Docker 一键容器化部署。

## 🚀 在线体验 / 本地部署
本项目采用前后端分离架构，并使用 Docker Compose 进行一键编排。确保本地已安装 Docker Desktop。

```bash
# 1. 克隆仓库
git clone https://github.com/a1625313506/fde-fullstack-deploy.git
cd fde-fullstack-deploy

# 2. 配置你的 API Key
# 打开 docker-compose.yml，将 ZHIPU_API_KEY 替换为你真实的智谱大模型 Key

# 3. 一键启动全栈服务
docker compose up -d --build
启动后访问 http://localhost 即可体验。
 
🛠️ 技术栈
• 前端: React 18, TypeScript, Vite, Tailwind CSS, Nginx
• 后端: Python 3.10, FastAPI, Uvicorn, HTTPX (异步流式)
• 数据库: SQLite + SQLAlchemy ORM (持久化与多表关联)
• 大模型: 智谱 GLM-4-Flash (Server-Sent Events 流式输出)
• 部署: Docker 多阶段构建, Docker Compose 
✨ 核心亮点
1. 丝滑打字机效果: 前后端基于 SSE (Server-Sent Events) 协议实现流式解析，拒绝长时间等待，用户体验对标 ChatGPT。
2. 多会话隔离与记忆: 引入 SQLite 数据库与 Conversation 外键关联，实现数据持久化，刷新网页永久保存，且各会话上下文完全隔离。
3. Markdown 渲染与安全: 使用 react-markdown 实现代码高亮与表格渲染；严格区分 AI 与用户输入，彻底防御 XSS 攻击。
4. 企业级容器化: 前端采用 Nginx 多阶段构建（减小体积），通过反向代理解决跨域；后端通过环境变量隔离敏感配置，实现一键交付。 
🔗 关联仓库
• 前端仓库: https://github.com/a1625313506/my-fde-app.git
• 后端仓库: https://github.com/a1625313506/my-fde-backend.git
👉 [点击查看 1 分钟项目演示视频](https://www.bilibili.com/video/BV1Kpxr6fES7/?vd_source=be42a59399e8d93658e3fcfe8113e3c5)
