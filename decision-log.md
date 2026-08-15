# Decision Log

## 2026-08-15 — Three-system profile redesign

### Decision

- 用 `Trading OS / Content OS / Agent Product Lab` 展示 full picture。
- 采用极简系统架构地图，而不是动态统计、动画和技术徽章墙。
- 中文负责叙事，英文负责系统名、contract 与可扫描关键词。
- 每套系统固定使用 `Outcome / System Map / Products / Now / Next`。

### Why

旧 Profile 同时承载方法论、路线图、repo 清单、参考项目和 To-Do，内容完整但缺乏视觉优先级。新的结构保留全貌，同时把默认视图收敛到系统、状态和真实产品入口。

### Gotchas

- GitHub Profile 是公开页面；本地存在或登录后可访问，不代表外部访客能够打开。
- `READY` 必须表示存在可用入口和明确核心结果，不能由 green tests、部署或 README 单独推导。
- README 中的 SVG 必须同时适配 GitHub light/dark theme，并保留文本替代内容。
