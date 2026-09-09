# 前端专业技能全集 (Frontend Skills Pack)

这套专业前端 Skills 是一套针对现代化前端工程、高质感视觉设计、动态交互与真实 UI 验收打造的专业 Agent 技能库。

---

## 快速安装与配置

将本文件夹下的所有子文件夹直接放入你的 Agent 全局 Skills 目录即可生效：

- **全局安装推荐路径**：
  - Windows: `~/.agents/skills/` (即 `C:\Users\你的用户名\.agents\skills\`)
  - macOS / Linux: `~/.agents/skills/`
- **单项目隔离安装**：
  - 复制到项目根目录下的 `.agents/skills/`

---

## 统一调度入口：`qianduan`

平时与 AI 交互时，**不需要记忆任何零碎技能名称**，只需在对话中说：

> **“前端skill：做个类似 Clash Verge 的高颜值暗黑科幻仪表盘”**  
> 或  
> **“前端：实现一个支持拖拽排序的虚拟列表，带平滑动画”**

`qianduan` 会作为顶层总指挥，自动分析你的任务需求，并精准分流调度底层的专业技能。

---

## 包含的 18 个独立大类 Skill 清单

### 1. 统一调度入口
- **`qianduan`**: 前端统一入口与任务动态分流。

### 2. 视觉美学与设计系统
- **`frontend-design`**: 打破 AI 模板化，提供色彩、排版、玻璃拟态等高质感视觉体系。
- **`frontend-components`**: 弹窗、抽屉、表单等业务交互与通用组件封装。
- **`shadcn`**: 针对现代 shadcn/ui 的组件添加、组合、样式微调与无障碍处理。
- **`tailwind-design-system`**: Tailwind CSS (v3/v4) 原子类、响应式与设计 Token 规范。
- **`tubiao-auto-icon-selector`**: 图标库选型、离线图标与矢量图标资产。

### 3. 数据可视化与复杂交互
- **`echarts`**: Apache ECharts 大屏看板、流式数据、自适应 Resize 与暗色主题。
- **`sortablejs-drag-sort`**: 列表/看板拖拽排序，兼顾触屏与键盘无障碍。

### 4. 动画与交互动效大类
- **`gsap`**: GreenSock 工业级动效大类全集。统一涵盖核心补间 (Core Tweens)、时间轴编排 (Timeline)、滚动触发与视差吸顶 (ScrollTrigger)、React/Next.js (@gsap/react useGSAP)、Vue/Svelte 框架挂载、高级插件 (Flip/Draggable/SplitText 等)、高帧率调优 (60FPS/GPU) 及实用工具函数 (gsap.utils)，并在 `modules/` 目录下提供完整子模块文档。

### 5. 质量底线与真实验收体系
- **`webapp-testing`**: 本地真实 UI 验收底线，检查控制台报错、网络请求与真实可用性。
- **`playwright`**: 无头浏览器自动化截屏比对与端到端回归。
- **`web-perf`**: 性能瓶颈诊断与首屏加载调优。
- **`vercel-react-best-practices`**: Vercel 工业级 React 架构规范与打包体积优化。
- **`web-design-guidelines`**: Web 界面可访问性 (WCAG) 与规范审计。

### 6. 受控独立专项
- **`huashu-design`**: 独立高保真 HTML 原型与概念设计演示方案。
- **`frontend-slides`**: 生成动画丰富的专业 Web 幻灯片。
- **`theme-factory`**: 多套主题包深度定制与切换。
- **`web-coding-workflow`**: 规范的 VC 前端工程交付工作流。

---

## 核心设计纪律
- **不滥用依赖**：小动效优先原生 CSS，大动效用 Canvas / GSAP，不盲目乱装第三方大包。
- **验证质量底线**：必须启动并确认 HTTP 200 或真实浏览器渲染，区分“命令跑了”和“用户真能用”。
