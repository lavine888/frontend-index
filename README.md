<div align="center">

# Frontend Index

### 18 个前端 Agent Skills 的可浏览索引与集合

从视觉设计、组件系统、数据可视化和 GSAP 动效，到 React 性能、Playwright、真实 UI 验收与专项 HTML 设计工作流。

[![Skills](https://img.shields.io/badge/Skills-18-2563EB?style=flat-square)](#skill-索引)
[![Frontend](https://img.shields.io/badge/Focus-Frontend-0F172A?style=flat-square)](#skill-索引)
[![Agent Skills](https://img.shields.io/badge/Format-SKILL.md-14B8A6?style=flat-square)](#怎么用)

</div>

---

## 这个仓库是做什么的

`frontend-index` 是一个 **前端 Agent Skill 全集索引仓**。

它参考 [`CityU-CS-Notes`](https://github.com/lavine888/CityU-CS-Notes) 的课程索引思路：先在首页把全部内容做成清晰可导航的目录，再让每一个条目进入自己的 Skill 目录。

**这个仓库只负责“收全”，不负责“替你删”。**

- 🗂️ **全集存档**：保留这套前端 Skills Pack 的 18 个独立入口。
- 🧭 **快速索引**：按场景和类别找到对应 Skill，不需要背名称。
- 🧩 **独立组合**：设计、组件、动效、图表、测试、性能等能力可以按项目选用。
- 🔬 **精选版底座**：之后会另开一个仓库，专门做去重、修正和适合个人工作流的版本。

> **全集 ≠ 建议 18 个全部全局加载。** 这里首先是 collection / catalog，不代表每次 Agent 工作都应该把所有 Skill 一次性塞进上下文。

---

## Skill 索引

<table>
<colgroup>
<col width="23%">
<col width="16%">
<col width="39%">
<col width="22%">
</colgroup>
<thead>
<tr>
<th>Skill</th>
<th>类别</th>
<th>主要用途</th>
<th>目录 / 保存方式</th>
</tr>
</thead>
<tbody>
<tr><th colspan="4" align="left">01 · 统一入口 / Workflow</th></tr>
<tr><td><code>qianduan</code></td><td>路由</td><td>“前端 skill”统一入口，根据任务分流到设计、组件、动效、图表与验收能力。</td><td><a href="qianduan"><code>qianduan/</code></a></td></tr>
<tr><td><code>web-coding-workflow</code></td><td>工程流程</td><td>完整 VC / vibe coding 工程流程：需求、架构、实现、调试与验收。</td><td><a href="web-coding-workflow"><code>web-coding-workflow/</code></a></td></tr>

<tr><th colspan="4" align="left">02 · 视觉设计 / Design System</th></tr>
<tr><td><code>frontend-design</code></td><td>视觉设计</td><td>视觉方向、排版、色彩、层级与页面构图，减少模板化 AI 审美。</td><td><a href="frontend-design"><code>frontend-design/</code></a></td></tr>
<tr><td><code>frontend-components</code></td><td>组件体系</td><td>表格、表单、导航、反馈、数据展示等 UI 组件与业务交互模式。</td><td><a href="frontend-components"><code>frontend-components/</code></a></td></tr>
<tr><td><code>shadcn</code></td><td>组件框架</td><td>shadcn/ui 的组件搜索、添加、组合、调试、样式与 registry 使用。</td><td><a href="shadcn"><code>shadcn/</code></a></td></tr>
<tr><td><code>tailwind-design-system</code></td><td>设计系统</td><td>Tailwind CSS v4、Design Tokens、响应式组件与设计系统。</td><td><a href="tailwind-design-system"><code>tailwind-design-system/</code></a></td></tr>
<tr><td><code>theme-factory</code></td><td>主题</td><td>为 Slides、Docs、报告和 HTML Artifact 选择与应用成套主题。</td><td><a href="theme-factory"><code>theme-factory/</code></a></td></tr>
<tr><td><code>tubiao-auto-icon-selector</code></td><td>图标</td><td>图标库选型、特殊图标查找、SVG 与离线图标资源。</td><td><a href="tubiao-auto-icon-selector"><code>tubiao-auto-icon-selector/</code></a></td></tr>

<tr><th colspan="4" align="left">03 · 数据可视化 / Complex Interaction</th></tr>
<tr><td><code>echarts</code></td><td>图表</td><td>Apache ECharts 生命周期、Resize、主题、大数据、流式更新与 SSR。</td><td><a href="echarts"><code>echarts/</code></a></td></tr>
<tr><td><code>sortablejs-drag-sort</code></td><td>拖拽</td><td>拖拽排序方案选择与实现，包括 SortableJS、dnd-kit 等。</td><td><a href="sortablejs-drag-sort"><code>sortablejs-drag-sort/</code></a></td></tr>

<tr><th colspan="4" align="left">04 · Motion / Animation</th></tr>
<tr><td><code>gsap</code></td><td>动效</td><td>GSAP Tween、Timeline、ScrollTrigger、React/Vue/Svelte、插件与性能调优。</td><td><a href="gsap"><code>gsap/</code></a></td></tr>

<tr><th colspan="4" align="left">05 · Testing / Performance / Quality</th></tr>
<tr><td><code>webapp-testing</code></td><td>UI 验收</td><td>真实 UI 验收：交互、响应式、浏览器日志、资源加载与基础可访问性。</td><td><a href="webapp-testing"><code>webapp-testing/</code></a></td></tr>
<tr><td><code>playwright</code></td><td>浏览器自动化</td><td>浏览器导航、表单、截图、快照、数据提取与 UI Flow 调试。</td><td><a href="playwright"><code>playwright/</code></a></td></tr>
<tr><td><code>web-perf</code></td><td>性能</td><td>Core Web Vitals、加载链路、缓存、布局偏移与页面性能诊断。</td><td><a href="web-perf"><code>web-perf/</code></a></td></tr>
<tr><td><code>vercel-react-best-practices</code></td><td>React / Next.js</td><td>Vercel React / Next.js 性能规范：waterfall、bundle、server/client 与 rendering。</td><td><a href="vercel-react-best-practices"><code>vercel-react-best-practices/</code></a></td></tr>
<tr><td><code>web-design-guidelines</code></td><td>设计审查</td><td>按 Web Interface Guidelines 审查 UI、UX、可访问性与界面规范。</td><td><a href="web-design-guidelines"><code>web-design-guidelines/</code></a></td></tr>

<tr><th colspan="4" align="left">06 · 独立专项 / Specialty</th></tr>
<tr><td><code>huashu-design</code></td><td>高保真设计</td><td>HTML 高保真原型、动画演示、设计方向对比与按需媒体导出。</td><td><a href="huashu-design"><code>huashu-design/</code></a> · submodule</td></tr>
<tr><td><code>frontend-slides</code></td><td>Web Slides</td><td>从零制作或从 PPT 转换动画丰富的 16:9 HTML 演示文稿。</td><td><a href="frontend-slides"><code>frontend-slides/</code></a> · submodule</td></tr>
</tbody>
</table>

**共 18 个 Skill。** 每个 Skill 都以 `SKILL.md` 为主要入口；部分能力还带有 `references/`、`modules/`、`scripts/`、模板或媒体资产。

---

## 怎么用

### 1. 当作前端能力地图

先确定任务，再点进对应目录：

```text
做页面视觉         → frontend-design
做 UI / 业务组件    → frontend-components / shadcn
做滚动和时间轴动效 → gsap
做数据大屏         → echarts
做拖拽排序         → sortablejs-drag-sort
验收页面是否真能用 → webapp-testing / playwright
查 Next.js 性能    → vercel-react-best-practices
做高保真概念 Demo  → huashu-design
做 Web 演示文稿     → frontend-slides
```

### 2. 克隆完整集合

两个大型 Skill 使用固定 commit 的 Git submodule，因此推荐：

```bash
git clone --recurse-submodules https://github.com/lavine888/frontend-index.git
```

如果已经普通 clone：

```bash
git submodule update --init --recursive
```

### 3. 按需安装

把需要的目录复制进你的 Agent Skill 目录。不同 Coding Agent 的路径约定不同，以你的实际环境为准，例如：

```bash
# 共享 Skills
cp -R gsap ~/.agents/skills/gsap

# 项目级隔离
mkdir -p .agents/skills
cp -R echarts .agents/skills/echarts
```

不建议因为这个仓库叫“全集”就机械地一次性加载全部 18 个。

---

## 仓库结构

```text
frontend-index/
├── README.md
├── SOURCES.md
├── .gitmodules
├── qianduan/
├── frontend-design/
├── frontend-components/
├── shadcn/
├── tailwind-design-system/
├── theme-factory/
├── tubiao-auto-icon-selector/
├── echarts/
├── sortablejs-drag-sort/
├── gsap/
├── webapp-testing/
├── playwright/
├── web-perf/
├── vercel-react-best-practices/
├── web-design-guidelines/
├── web-coding-workflow/
├── huashu-design/      # pinned submodule
└── frontend-slides/    # pinned submodule
```

---

## 来源与 License

这套集合包含不同作者、不同来源和不同许可证的 Skill，因此**不使用一个顶层许可证覆盖全部第三方内容**。

- 已有 License / 作者 / 版本信息尽量原样保留。
- 两个大型 Skill 固定到明确的 upstream commit，避免“永远指向最新”导致内容漂移。
- 具体快照与来源关系见 [`SOURCES.md`](SOURCES.md)。

---

## 关于这个系列

**仓库 1：`frontend-index`**  
负责收集、索引、存档，不做强行删减。

**仓库 2：Frontend Skill Kit（下一步）**  
会从这里出发，把重合能力、过时流程和有问题的实现拆掉，重新组合成更适合实际 Coding Agent / Codex 工作流的轻量版本。

---

整理：[@lavine888](https://github.com/lavine888)

如果这个索引对你有帮助，可以点个 **Star**。
