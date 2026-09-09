# 前端专业技能全集 (Frontend Skills Pack)

这套专业前端 Skills 是一套针对现代化前端工程、高质感视觉设计、动态交互与真实 UI 验收打造的专业 Agent 技能集合。

> 本仓库定位是 **Frontend Skills Index / Collection**：先完整保留这套 18 个 Skill 的入口与来源关系，不做“适合某个人”的删减和重组。后续可从这里再提纯出个人版 Frontend Skill Kit。

---

## 快速安装与配置

### 推荐：完整克隆（包含两个大型 Skill 子模块）

```bash
git clone --recurse-submodules https://github.com/lavine888/frontend-index.git
```

如果已经普通 clone：

```bash
git submodule update --init --recursive
```

随后将所需 Skill 文件夹放入 Agent Skills 目录：

- **全局安装推荐路径**：
  - Windows: `~/.agents/skills/`（即 `C:\Users\你的用户名\.agents\skills\`）
  - macOS / Linux: `~/.agents/skills/`
- **单项目隔离安装**：
  - 复制到项目根目录下的 `.agents/skills/`

### 仓库保存方式

- 16 个中小型 Skill：入口 `SKILL.md` 直接保存在本仓库。
- `frontend-slides`：完整资源体量较大，以固定 commit 的 Git submodule 保存。
- `huashu-design`：包含大量设计案例、脚本、图片/音频等资源，以固定 commit 的 Git submodule 保存。
- 各 Skill 的来源与快照说明见 [`SOURCES.md`](./SOURCES.md)。

---

## 统一调度入口：`qianduan`

平时与 AI 交互时，**不需要记忆任何零碎技能名称**，只需在对话中说：

> **“前端skill：做个类似 Clash Verge 的高颜值暗黑科幻仪表盘”**  
> 或  
> **“前端：实现一个支持拖拽排序的虚拟列表，带平滑动画”**

`qianduan` 会作为顶层总指挥，自动分析任务需求，并按需分流到底层专业 Skill。

---

## 包含的 18 个独立大类 Skill

### 1. 统一调度入口
- **`qianduan`** — 前端统一入口与任务动态分流。

### 2. 视觉美学与设计系统
- **`frontend-design`** — 内容驱动的视觉方向、排版、层级与独特性。
- **`frontend-components`** — 弹窗、抽屉、表单、数据展示等通用组件与业务交互。
- **`shadcn`** — shadcn/ui 组件添加、组合、样式、注册表与无障碍处理。
- **`tailwind-design-system`** — Tailwind CSS 设计 Token、响应式与设计系统规范。
- **`tubiao-auto-icon-selector`** — 图标库选型、特殊图标、离线图标资源与国内网络方案。

### 3. 数据可视化与复杂交互
- **`echarts`** — Apache ECharts 生命周期、响应式、主题、流式/大数据与 SSR。
- **`sortablejs-drag-sort`** — 列表/看板拖拽排序及 SortableJS、dnd-kit 等方案选型。

### 4. 动画与交互动效
- **`gsap`** — GreenSock 动效：Tweens、Timeline、ScrollTrigger、React/Vue/Svelte、插件、性能与 utils。

### 5. 质量与真实验收
- **`webapp-testing`** — 本地真实 UI 验收、交互、控制台、网络与响应式检查。
- **`playwright`** — 浏览器自动化、截图、表单与端到端流程。
- **`web-perf`** — Core Web Vitals、网络链路与性能审计。
- **`vercel-react-best-practices`** — React / Next.js 性能与工程最佳实践。
- **`web-design-guidelines`** — Web UI 规范、可访问性与设计审计。

### 6. 独立专项
- **`huashu-design`** — 高保真 HTML 原型、动画、幻灯片、可视化与专家评审。
- **`frontend-slides`** — 动画丰富的专业 Web 幻灯片与 PPT 转 Web。
- **`theme-factory`** — 主题包选择、定制与应用。
- **`web-coding-workflow`** — VC / Vibecoding 完整工程交付工作流。

---

## 为什么是 Index，而不是“一股脑全局加载”

这个仓库的职责是 **收集、保存、索引**。它不代表 18 个 Skill 应当同时进入每一次 Agent 上下文。实际使用时应让调度入口或项目规则按任务加载必要能力。

下一步可以从这个全集仓库中再建立一个更精炼的个人版，只保留真正能提高前端开发质量、且不与当前模型原生能力高度重合的部分。

---

## License & Attribution

本仓库聚合了不同来源、不同许可证的 Skill。**各 Skill 的原始许可证与上游条款分别生效**；本仓库不以一个统一许可证覆盖第三方内容。具体来源与固定版本见 [`SOURCES.md`](./SOURCES.md)。
