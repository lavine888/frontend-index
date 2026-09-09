---
name: gsap
description: GSAP (GreenSock Animation Platform) 综合动效大类 Skill。统一涵盖核心补间 API (gsap.to/from/fromTo/stagger/easing)、时间轴编排 (Timeline)、滚动视差与触发 (ScrollTrigger)、React/Next.js 生命周期 (@gsap/react useGSAP)、Vue/Svelte 框架挂载、高级插件 (Flip/Draggable/SplitText 等)、高帧率性能调优 (60FPS/GPU) 以及 gsap.utils 工具集。
---

# GSAP Animation Suite

GSAP 是工业级 JavaScript 动效套件，适用于复杂交互、页面转场、时间轴编排与高性能滚动视差。

## 模块导航与详细文档

本 Skill 整合了 GSAP 全套能力，细分子模块详见 `modules/` 目录：
- 核心补间与缓动：`modules/core.md`
- 时间轴编排与多步动效：`modules/timeline.md`
- 滚动触发与视差固定：`modules/scrolltrigger.md`
- React / Next.js 集成：`modules/react.md`
- Vue / Svelte 等框架集成：`modules/frameworks.md`
- 官方扩展插件库：`modules/plugins.md`
- 60FPS 性能与渲染优化：`modules/performance.md`
- 实用工具函数集：`modules/utils.md`

---

## 1. 核心补间 (Core API)

### 常用方法
- `gsap.to(target, vars)`：从当前状态动画至目标状态
- `gsap.from(target, vars)`：从指定状态动画至当前自然状态
- `gsap.fromTo(target, fromVars, toVars)`：显式指定起始与结束状态
- `gsap.set(target, vars)`：立即设置属性（持续时间为 0）

### 补间示例与交错 (Stagger)
```javascript
gsap.to(".card", {
  duration: 0.8,
  y: 0,
  opacity: 1,
  stagger: 0.1, // 每个卡片错开 0.1s 执行
  ease: "power2.out",
  clearProps: "transform" // 动画结束后清理行内变换，保持响应式
});
```

### 响应式与减少动效 (matchMedia)
```javascript
const mm = gsap.matchMedia();

mm.add("(min-width: 768px)", () => {
  // 桌面端专属动效
  gsap.to(".hero-title", { x: 100, duration: 1 });
});

mm.add("(prefers-reduced-motion: reduce)", () => {
  // 无障碍降级：禁用位移，仅保留淡入
  gsap.to(".hero-title", { opacity: 1, duration: 0.3 });
});
```

---

## 2. 时间轴编排 (Timeline)

管理多步骤、复杂序列动画，支持全局暂停、反转、跳跃和播放控制。

```javascript
const tl = gsap.timeline({
  defaults: { duration: 0.6, ease: "power3.out" }
});

tl.from(".header", { y: -40, opacity: 0 })
  .from(".hero-text", { y: 30, opacity: 0 }, "-=0.2") // 重叠 0.2s
  .from(".cta-button", { scale: 0.8, opacity: 0 }, "<0.1") // 在上一动画开始后 0.1s 执行
  .addLabel("scene2")
  .to(".bg-glow", { scale: 1.2, duration: 1 }, "scene2");
```

---

## 3. 滚动视差与吸顶 (ScrollTrigger)

使用 `ScrollTrigger` 实现随页面滚动的视差、吸顶固定（pin）以及横向平移。

```javascript
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

// 基础视差吸附
gsap.to(".feature-card", {
  scrollTrigger: {
    trigger: ".feature-section",
    start: "top center", // 触发元素顶部到达视口中间时
    end: "bottom top",
    scrub: 1, // 平滑跟随滚动
    toggleActions: "play none none reverse"
  },
  y: -80,
  opacity: 1
});
```

### 横向滚动容器 (Horizontal Scroll)
```javascript
const scrollingEl = document.querySelector(".horizontal-el");
const panel = scrollingEl.parentElement;
const getScrollDistance = () => Math.max(0, scrollingEl.scrollWidth - panel.clientWidth);
// Panel = pinned viewport-sized section. .horizontal-wrap = inner content that moves left.
const scrollTween = gsap.to(scrollingEl, { 
  x: () => -getScrollDistance(),
  ease: "none",
  scrollTrigger: {
    trigger: panel,
    pin: true,
    scrub: true,
    invalidateOnRefresh: true,
    end: () => `+=${getScrollDistance()}`
  }
});

// 容器内子元素与主横向滚动联动
gsap.to(".inner-box", {
  y: -50,
  scrollTrigger: {
    trigger: ".inner-box",
    containerAnimation: scrollTween,
    start: "left center",
    toggleActions: "play none none reverse"
  }
});
```

---

## 4. React / Next.js 集成

在 React 中必须遵循生命周期管理，避免 StrictMode 下双重渲染引发的动画冲突与内存泄漏。优先使用 `@gsap/react` 的 `useGSAP`。

```jsx
import { useRef } from "react";
import gsap from "gsap";
import { useGSAP } from "@gsap/react";

gsap.registerPlugin(useGSAP);

export default function HeroSection() {
  const containerRef = useRef(null);

  useGSAP(() => {
    // 自动以 containerRef 为选择器作用域，组件卸载时自动清理
    gsap.from(".title", { opacity: 0, y: 30, duration: 0.8 });
  }, { scope: containerRef, dependencies: [] });

  return (
    <div ref={containerRef} className="hero">
      <h1 className="title">Hello World</h1>
    </div>
  );
}
```

*若未安装 `@gsap/react`，使用 `useLayoutEffect` / `useEffect` 配合 `gsap.context()` 手动清理：*
```jsx
useEffect(() => {
  const ctx = gsap.context(() => {
    gsap.to(".box", { x: 100 });
  }, containerRef);
  return () => ctx.revert(); // 确保卸载时彻底回滚
}, []);
```

---

## 5. Vue / Svelte 框架集成

在 Vue 3 / Nuxt 中使用 `onMounted` 创建并在 `onUnmounted` 中通过 `gsap.context()` 统一清理。

```vue
<script setup>
import { onMounted, onUnmounted, ref } from 'vue';
import gsap from 'gsap';

const root = ref(null);
let ctx;

onMounted(() => {
  ctx = gsap.context(() => {
    gsap.from('.item', { opacity: 0, y: 20, stagger: 0.1 });
  }, root.value);
});

onUnmounted(() => {
  ctx?.revert(); // 清理避免内存泄漏
});
</script>

<template>
  <div ref="root">
    <div class="item">1</div>
    <div class="item">2</div>
  </div>
</template>
```

---

## 6. 高级插件 (Plugins)

使用前必须调用 `gsap.registerPlugin(...)` 显式注册。
- **Flip**：无缝处理 DOM 结构变化、重新排序、展开/折叠过渡。
- **Draggable**：惯性拖拽、滑块、抛掷与边界限制。
- **SplitText / ScrambleText**：逐字/逐词动画与文字乱序解密特效。
- **ScrollSmoother**：页面全局丝滑惯性滚动。
- **DrawSVG / MotionPath**：矢量 SVG 描边动画与复杂曲线运动路径。

```javascript
import { Flip } from "gsap/Flip";
gsap.registerPlugin(Flip);

// 捕获初始状态
const state = Flip.getState(".grid-item");
// 改变 DOM 结构或切换类名
container.classList.toggle("list-layout");
// 执行平滑过渡
Flip.from(state, {
  duration: 0.7,
  ease: "power1.inOut",
  stagger: 0.05
});
```

---

## 7. 60FPS 性能与渲染优化

1. **优先使用硬件加速属性**：
   - 严格使用 `x`, `y`, `scale`, `rotation`, `opacity`。
   - 严禁对 `top`, `left`, `width`, `height`, `margin`, `padding` 频繁执行高频补间（会触发浏览器重排与重绘 Layout Thrashing）。
2. **will-change 规范**：
   - 仅在重度高频动画前设置 `will-change: transform`，动画结束或空闲时清理。
3. **ScrollTrigger 刷新开销控制**：
   - 避免在大量滚动触发器中使用复杂的实时 DOM 计算；对于动态内容使用 `ScrollTrigger.refresh()` 防抖执行。
4. **批量更新**：
   - 多元素动效优先使用 `stagger` 或 `gsap.timeline()`，而非分散生成数百个独立的 `setInterval` 或独立 tween。

---

## 8. gsap.utils 核心工具集

- `gsap.utils.clamp(min, max, value)`：数值区间钳制
- `gsap.utils.mapRange(inMin, inMax, outMin, outMax, value)`：区间数值线性映射
- `gsap.utils.interpolate(start, end, progress)`：插值计算
- `gsap.utils.random(min, max, roundTo)`：生成区间随机数
- `gsap.utils.snap(snapIncrement, value)`：吸附对齐数值
- `gsap.utils.wrap(min, max, value)`：环形循环索引
- `gsap.utils.toArray(selector)`：安全将选择器/节点集合转为真实 Array
- `gsap.utils.pipe(fn1, fn2, fn3)`：函数链式管道组合

```javascript
// 数值映射示例：将鼠标移动位置 (0~window.innerWidth) 映射到 (-50~50) 旋转角度
const mapX = gsap.utils.mapRange(0, window.innerWidth, -50, 50);
window.addEventListener("mousemove", (e) => {
  gsap.to(".tilt-card", { rotationY: mapX(e.clientX), overwrite: "auto" });
});
```
