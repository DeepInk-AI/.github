<p align="center">
  <img src="./home.png" alt="深墨 DeepInk" width="100%" />
</p>

<p align="center">
  <img src="./logo.png" alt="DeepInk Logo" width="84" />
</p>

<h1 align="center">深墨 DeepInk</h1>

<p align="center">
  面向论文写作场景的 AI 创作平台，从文献准备、提纲生成、段落写作、在线排版到 WPS/Word 导出，帮助用户更高效地完成结构化学术写作。
</p>

<p align="center">
  <img alt="Next.js" src="https://img.shields.io/badge/Next.js-16-111827?style=for-the-badge&logo=nextdotjs" />
  <img alt="React" src="https://img.shields.io/badge/React-19-2563eb?style=for-the-badge&logo=react" />
  <img alt="NestJS" src="https://img.shields.io/badge/NestJS-11-e11d48?style=for-the-badge&logo=nestjs" />
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-5.x-3178c6?style=for-the-badge&logo=typescript&logoColor=white" />
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-TypeORM-4169e1?style=for-the-badge&logo=postgresql&logoColor=white" />
</p>

---

## 产品定位

深墨不是一个简单的聊天式生成工具，而是围绕“论文交付”设计的一套工作流系统。第一版本会优先打通用户真正需要的核心路径：登录注册、论文创作、万方文献插入、段落级生成、在线编辑排版、文档导出、AIGC 降重、充值计费与代理模式。

<p align="center">
  <img src="./showcase.png" alt="深墨工作台视觉" width="100%" />
</p>

## 核心能力

| 模块 | 说明 |
| --- | --- |
| AI 论文写作 | 支持按论文主题、专业方向、字数、章节结构生成内容，并允许用户逐段编辑标题后再生成正文。 |
| 万方文献接入 | 对接万方文献 API，完成文献检索、选择、引用插入与参考文献管理。 |
| 在线编辑排版 | 提供接近 WPS/Word 的文档编辑体验，支持标题层级、正文格式、引用与排版规则调整。 |
| 文档导出 | 支持将论文结果导出为可继续编辑的 WPS/Word 文档。 |
| AIGC 降重 | 面向论文重复率与 AI 痕迹优化，提供段落级改写、语义保留与风格调整。 |
| 代理模式 | 支持代理账号、客户订单、余额/套餐、渠道收益与服务工单等业务能力。 |
| 充值与账户 | 支持用户套餐、点数余额、订单记录、消费明细与权限控制。 |

## 技术架构

```mermaid
flowchart LR
  Docs["官网 Docs<br/>品牌介绍 / 转化入口"]
  Web["Web 工作台<br/>用户端 / 代理端 / 管理端"]
  Core["DeepInk Core<br/>NestJS API 服务"]
  AI["AI 生成层<br/>大模型编排 / Agent 流程"]
  Literature["文献服务<br/>万方 API / 引用管理"]
  DocEngine["文档引擎<br/>在线编辑 / 排版 / 导出"]
  Billing["业务系统<br/>登录 / 充值 / 订单 / 代理"]
  DB[("PostgreSQL<br/>用户 / 论文 / 订单 / 文献")]

  Docs --> Web
  Web --> Core
  Core --> AI
  Core --> Literature
  Core --> DocEngine
  Core --> Billing
  Core --> DB
```

## 技术栈

| 层级 | 技术选型 |
| --- | --- |
| 前端 Monorepo | Turborepo、pnpm、TypeScript |
| Web 工作台 | Next.js 16、React 19、Tailwind CSS、shadcn/radix-ui、React Hook Form、Zod、Motion |
| Docs 官网 | Next.js、品牌视觉资产、滚动动效与响应式页面 |
| 后端服务 | NestJS 11、TypeORM、PostgreSQL、class-validator、Jest |
| AI 能力 | 模型接入层、生成任务编排、论文段落生成、AIGC 改写、Agent 模式 |
| 文档能力 | 在线编辑、排版规则、文献引用、DOCX/WPS 导出 |

## 第一版优先级

- **P0：可上线闭环**：官网、登录注册、论文创建、AI 生成、在线编辑、文档导出。
- **P1：论文增强**：万方文献检索、引用插入、参考文献管理、AIGC 降重。
- **P2：商业化**：充值套餐、订单记录、消费明细、代理账户与代理客户管理。
- **P3：运营与服务**：工单系统、后台管理、用户权限、数据看板与异常追踪。

## 仓库入口

| 仓库 | 说明 |
| --- | --- |
| [DeepInk](https://github.com/DeepInk-AI/DeepInk) | 深墨前端 Monorepo，包含 Web 工作台与 Docs 官网。 |
| [DeepInk-Core](https://github.com/DeepInk-AI/DeepInk-Core) | 深墨后端服务，负责用户、论文、文献、AI 任务、计费与代理业务。 |

<p align="center">
  <img src="./night-workspace.png" alt="深墨夜间工作台视觉" width="100%" />
</p>

---

<p align="center">
  <strong>Deep</strong> 代表深度学习，<strong>Ink</strong> 代表笔墨。深墨希望把 AI 能力真正落到论文创作的每一个步骤里。
</p>
