# Sources & Snapshot Notes

This repository is the **collection/index form** of the 18 frontend Skills from the uploaded `前端Skills全集` snapshot.

## Snapshot policy

- The 18 top-level Skill names are preserved.
- For 16 compact Skills, the collection vendors the primary `SKILL.md` entry directly in this repository.
- Two large, self-contained Skills are pinned as Git submodules so their full template/reference/media trees remain available without flattening or duplicating them.
- Third-party licenses remain with their respective upstream projects/content.

## 18-Skill manifest

| Skill | Storage in this repo | Snapshot/source note |
|---|---|---|
| `qianduan` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `frontend-design` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `frontend-components` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `shadcn` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `tailwind-design-system` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `tubiao-auto-icon-selector` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `echarts` | Vendored `SKILL.md` | Uploaded frontend pack snapshot; metadata credits Ihor Orlovskyi, MIT |
| `sortablejs-drag-sort` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `gsap` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `webapp-testing` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `playwright` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `web-perf` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `vercel-react-best-practices` | Vendored `SKILL.md` | Uploaded frontend pack snapshot; metadata credits Vercel, MIT |
| `web-design-guidelines` | Vendored `SKILL.md` | Uploaded frontend pack snapshot; metadata credits Vercel |
| `theme-factory` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `web-coding-workflow` | Vendored `SKILL.md` | Uploaded frontend pack snapshot |
| `frontend-slides` | **Pinned submodule** | `zarazhangrui/frontend-slides` @ `9906a34d640d2111f724544cbc50f7f130569ae1` |
| `huashu-design` | **Pinned submodule** | `alchaincyf/huashu-design` @ `a790f704d85f277cc93d2081b0840d00036969bb` |

## Important note about `huashu-design`

The uploaded frontend pack contains a locally adapted `huashu-design/SKILL.md` whose entry instructions differ from the currently pinned public upstream version. The collection keeps the **full public upstream resource tree** as a pinned submodule rather than silently replacing its many scripts/media/assets with a partial copy.

That distinction matters for the later personalized repository: the uploaded local entry is useful evidence for deciding which execution boundaries and design rules should be retained, rewritten, or removed.

## Clone with the large Skills

```bash
git clone --recurse-submodules https://github.com/lavine888/frontend-index.git
```

Or after a normal clone:

```bash
git submodule update --init --recursive
```

## Repository intent

`frontend-index` is the **source collection / catalog**. It intentionally does not claim that every Skill should be globally loaded together. A separate curated repository can later select, merge, fix, and modernize the subset that is actually useful for a specific workflow.
