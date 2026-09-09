# Sources & Snapshot Notes

This repository is the **collection / index form** of the 18 frontend Skills from the uploaded `前端Skills全集` snapshot.

## Snapshot policy

- The 18 top-level Skill names are preserved.
- The 16 compact Skills keep their uploaded `SKILL.md` entry directly in this repository; companion files may also be retained where useful for browsing or execution.
- Two large, self-contained Skills are pinned as Git submodules so their full template/reference/media trees remain available without flattening tens of megabytes into the index repository.
- Third-party licenses remain with their respective upstream projects/content.
- The repository is a catalog, **not** a recommendation to load all 18 Skills into every Agent context.

## 18-Skill manifest

| Skill | Storage in this repo | Snapshot/source note |
|---|---|---|
| `qianduan` | Vendored entry | Uploaded frontend pack snapshot |
| `frontend-design` | Vendored entry | Uploaded frontend pack snapshot; Apache-2.0 license file retained in the pack |
| `frontend-components` | Vendored entry | Uploaded frontend pack snapshot |
| `shadcn` | Vendored entry | Uploaded frontend pack snapshot |
| `tailwind-design-system` | Vendored entry | Uploaded frontend pack snapshot |
| `tubiao-auto-icon-selector` | Vendored entry | Uploaded frontend pack snapshot |
| `echarts` | Vendored entry + companion files | Uploaded frontend pack snapshot; metadata credits Ihor Orlovskyi, MIT |
| `sortablejs-drag-sort` | Vendored entry | Uploaded frontend pack snapshot |
| `gsap` | Vendored entry | Uploaded frontend pack snapshot |
| `webapp-testing` | Vendored entry | Uploaded frontend pack snapshot |
| `playwright` | Vendored entry | Uploaded frontend pack snapshot |
| `web-perf` | Vendored entry | Uploaded frontend pack snapshot |
| `vercel-react-best-practices` | Vendored entry | Uploaded frontend pack snapshot; metadata credits Vercel, MIT |
| `web-design-guidelines` | Vendored entry | Uploaded frontend pack snapshot; metadata credits Vercel |
| `theme-factory` | Vendored entry | Uploaded frontend pack snapshot |
| `web-coding-workflow` | Vendored entry | Uploaded frontend pack snapshot |
| `frontend-slides` | **Pinned submodule** | `zarazhangrui/frontend-slides` @ `9906a34d640d2111f724544cbc50f7f130569ae1` |
| `huashu-design` | **Pinned submodule** | `alchaincyf/huashu-design` @ `a790f704d85f277cc93d2081b0840d00036969bb` |

## Why the two submodules exist

`frontend-slides` and `huashu-design` contain much larger template / example / script / media trees than the other Skills. Pinning them to explicit commits keeps the index readable and reproducible while avoiding a flattened duplicate of large upstream repositories.

The uploaded pack also contains locally adapted entry instructions, especially around execution boundaries. Those local differences are useful input for the later personalized repository, where the goal will be to select, merge, fix, and modernize the parts that are actually worth keeping.

## Clone with the large Skills

```bash
git clone --recurse-submodules https://github.com/lavine888/frontend-index.git
```

Or after a normal clone:

```bash
git submodule update --init --recursive
```

## Repository intent

`frontend-index` is the **source collection / catalog**. A separate curated repository can later turn this raw collection into a smaller Frontend Skill Kit optimized for a specific Coding Agent workflow.
