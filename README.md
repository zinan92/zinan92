# 嘿，我是 parkzz

> 我自动化交易，自动化写代码，自动化做视频。
> 正在研究怎么自动化睡觉。

📍 上海

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Claude](https://img.shields.io/badge/-Claude-000000?style=flat-square&logo=anthropic&logoColor=white)
![SQLite](https://img.shields.io/badge/-SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Shell](https://img.shields.io/badge/-Shell-121212?style=flat-square&logo=gnu-bash&logoColor=white)

---

## 在造的东西

### 数据 `采集 → 清洗 → 分析 → 可视化`

📊 **[quant-data-pipeline](https://github.com/zinan92/quant-data-pipeline)** — 量化数据管线
> `采集 → 清洗 → 存储 → 查询` · 输入: AKShare/TuShare/Yahoo 行情 → 输出: 标准化 SQLite 数据库
> 自动拉取 A 股/美股/期货行情，清洗入库，提供 FastAPI 查询接口。定时任务，增量更新

🧠 **[qualitative-data-pipeline](https://github.com/zinan92/qualitative-data-pipeline)** — 定性信号情报系统
> `采集 → 聚类 → 叙事 → 可视化` · 输入: 10+ 信息源（Twitter/HN/Substack/新浪等） → 输出: 事件图谱 + AI 摘要 + 标的影响评分
> 跨源事件自动聚类，LLM 生成叙事摘要，标的价格影响量化，力导向星座图可视化

### 内容 `收集 → 分析 → 生产 → 分发`

#### 📥 收集

🍴 **[XHS-Downloader](https://github.com/JoeanAmier/XHS-Downloader)** — 小红书媒体提取器
> `收集` · 输入: 小红书链接/用户主页/搜索词 → 输出: 图片/视频/音频原始文件 + 元数据
> 单向提取工具，专注把内容从小红书拉出来。TUI/CLI/API/MCP 四种模式，异步断点续传，原子写入。适合研究、分析、归档。10k+ ⭐。**vs RedBox**: 这个是纯提取工具拿媒体文件，RedBox 是完整创作工作台覆盖采集→创作→发布全流程

🍴 **[MediaCrawler](https://github.com/NanmiCoder/MediaCrawler)** — 多平台主动爬虫
> `收集` · 输入: 关键词/用户ID/帖子链接 → 输出: 帖子/评论/用户数据（JSON/CSV）
> 主动爬取，需登录态。覆盖小红书、抖音、快手、B站、微博。搜索、评论、IP 代理池。**vs res-downloader**: 这个是主动爬虫拿结构化数据，res-downloader 是被动代理拦截拿媒体文件

🍴 **[res-downloader](https://github.com/putyy/res-downloader)** — 跨平台被动资源嗅探器
> `收集` · 输入: 正常浏览任意平台 → 输出: 视频/音频/图片原始文件
> 代理拦截模式，无需登录无需 API。覆盖视频号、小程序、抖音、快手、小红书、直播流、m3u8、酷狗、QQ音乐。**vs MediaCrawler**: 这个是被动嗅探拿媒体文件，MediaCrawler 是主动爬虫拿结构化数据

🍴 **[Scrapling](https://github.com/D4Vinci/Scrapling)** — 自适应通用爬虫框架
> `收集` · 输入: URL + CSS/XPath 选择器 → 输出: 结构化数据（JSON/JSONL）
> 通用网页爬虫框架，不限平台。自适应解析（页面改版自动定位），Cloudflare 绕过，断点续爬，MCP 服务器。**vs MediaCrawler**: 这个是通用框架爬任何网站，MediaCrawler 是针对特定中文平台的专用爬虫

📥 **[douyin-downloader](https://github.com/zinan92/douyin-downloader-1)** — 抖音内容管线
> `收集` · 输入: 抖音视频链接/用户主页 → 输出: 视频文件 + Whisper 转录文本（Markdown/JSON）
> 下载 → 本地 Whisper 转录 → 结构化归档。支持批量、时间序列、并发下载

🍴 **[wechat-article-exporter](https://github.com/wechat-article/wechat-article-exporter)** — 微信公众号文章批量下载
> `收集` · 输入: 公众号名称 → 输出: HTML/JSON/Excel/Markdown/DOCX 文章文件 + 阅读量/评论数据
> 在线工具无需搭建环境，支持 Docker/Cloudflare 私有部署，HTML 格式 100% 还原排版。8k+ ⭐

🍴 **[RedBox](https://github.com/Jamailar/RedBox)** — 小红书创作者工作台
> `收集` · 输入: 小红书账号/关键词/创作灵感 → 输出: 本地知识库 + AI 生成的内容草稿 + 封面设计 + 定时发布
> 双向工具，既能采集也能发布。内置浏览器一键采集、本地知识库、多工位隔离、AI 写作助手、智囊团群聊、RedClaw 自动化。**vs XHS-Downloader**: 这个是完整创作工作台覆盖采集→创作→发布，XHS-Downloader 是纯提取工具只做下载

#### 🔍 分析

🔍 **[content-intelligence](https://github.com/zinan92/content-intelligence)** — 内容情报分析
> `分析` · 输入: 小红书/抖音采集数据 → 输出: 趋势报告 + 内容策略建议
> 分析爆款规律、内容趋势、竞品动态，告诉你下一步该做什么内容

🧪 **[intelligence](https://github.com/zinan92/intelligence)** — 多品类研究引擎
> `分析` · 输入: MediaCrawler/抖音/小红书 JSONL → 输出: 归一化样本 + 加权评分 + JSON/MD/HTML 决策报告
> 品类无关的研究框架，Project Pack 机制隔离品类逻辑。零外部依赖，纯标准库。**vs content-intelligence**: 这个是通用研究引擎可扩展任意品类，content-intelligence 聚焦内容趋势策略

#### ✨ 生产

✂️ **[videocut](https://github.com/zinan92/videocut)** — 口播内容工厂
> `生产` · 输入: 一段录像 → 输出: 剪辑视频 + 字幕 + 文章 + 卡片 + 8 平台发布稿
> 一个命令 7 阶段：录制 → 剪辑 → 内容生成 → 卡片 → manifest → 发布。Web Dashboard 管理

🍴 **[text-to-image-prompt-optimizer](https://github.com/manzxiao/text-to-image-prompt-optimizer)** — 全平台图片 Prompt 优化器
> `生产` · 输入: 中文/英文产品描述 → 输出: 2-3 个风格变体 Prompt（Midjourney/Flux/DALL-E/Stable Diffusion/Gemini）
> 万能入口，把任何描述变成各平台最优图片 Prompt，中英双语输出。**vs midjourney-replicate-flux**: 这个覆盖全平台通用场景，后者专精产品摄影

🍴 **[midjourney-replicate-flux](https://github.com/rawveg/skillsforge-marketplace)** — 产品摄影 Prompt + 出图
> `生产` · 输入: 产品描述/场景需求 → 输出: 5 层结构化 Prompt（主体→风格→光影→技术→艺术参考）+ 可选直接调 Replicate API 出图
> 有产品摄影模板（白底电商图、生活场景等），适合翡翠/珠宝等实物拍摄场景。**vs text-to-image-prompt-optimizer**: 这个专精产品摄影可直接出图，前者是全平台通用优化

🎬 **[seedance-expert](https://github.com/zinan92/seedance-expert)** — 即梦 2.0 AI 导演
> `生产` · 输入: 文字描述/参考图片 → 输出: 即梦 2.0 视频生成提示词
> Claude Code 技能，10 种任务类型（文生视频/图生视频/延展/编辑等），50+ 提示词模板。**vs seedance-2.0-prompter**: 这个是全功能导演工具覆盖 10 种任务，后者专注单条 Prompt 的结构化 JSON 输出

🍴 **[seedance-2.0-prompter](https://github.com/pexoai/pexo-skills)** — Seedance 2.0 结构化 Prompt 生成
> `生产` · 输入: 视频创意描述 → 输出: 结构化 JSON（prompt + 参数），可直接丢进 Seedance 2.0
> 专注 Prompt 工程，支持多素材引用，输出 JSON 格式即用即走。**vs seedance-expert**: 这个输出结构化 JSON 适合自动化管线，前者是交互式全功能导演

🍴 **[seedance-storyboard](https://github.com/elementsix/elementsix-skills)** — Seedance 分镜脚本生成
> `生产` · 输入: 故事/创意大纲 → 输出: 多段分镜脚本 + 每段对应的 Seedance Prompt
> 适合多段短视频制作，把一个故事拆成分镜，每个镜头自动生成 Prompt

🧪 **[AI-videos](https://github.com/zinan92/AI-videos)** — 虚拟角色视频管线
> `生产` · 输入: 人物照片 + 动作参考 → 输出: 换装/动作迁移后的 AI 视频
> Klein 换装 + Kling 动作迁移 + RunningHub 模型跑分，全流程 workflow

🍴 **[mm-easy-voice](https://github.com/openclaw/skills/tree/main/skills/blue-coconut/mm-easy-voice)** — 语音生成技能
> `生产` · 输入: 文本 + 风格参数 → 输出: AI 语音音频
> OpenClaw 技能，调用 MiniMax 语音合成，支持情绪和语速控制

🍴 **[frontend-slides](https://github.com/zarazhangrui/frontend-slides)** — 动画演示文稿生成
> `生产` · 输入: 主题描述 或 PPT 文件 → 输出: 动画丰富的 HTML 演示文稿
> Claude Code 技能，从零创作或从 PowerPoint 转换，自带过渡动画和交互效果

🍴 **[gsap-skills](https://github.com/greensock/gsap-skills)** — GSAP 官方动画 AI 技能包
> `生产` · 输入: 动画需求描述 → 输出: 符合最佳实践的 GSAP 动画代码
> 8 个专项技能（核心动画/时间轴/ScrollTrigger/插件/性能优化/React/Vue/Svelte），支持 40+ AI 编程助手

#### 🚀 分发

🍴 **[libtv-skills](https://github.com/libtv-labs/libtv-skills)** — LibLib.tv AIGC 平台发布技能
> `分发` · 输入: 生成好的图片/视频 → 输出: 发布到 LibLib.tv 平台
> AI agent 技能，通过 OpenAPI 接口自动发图发视频，批量上传

### 交易 `分析 → 决策 → 执行`

#### 📊 分析

🍴 **[daily_stock_analysis](https://github.com/ZhuLinsen/daily_stock_analysis)** — LLM 驱动的每日股票分析
> `分析` · 输入: A/H/美股股票代码 + 行情数据（AKShare/TuShare/YFinance）+ 实时新闻 → 输出: 买卖信号仪表盘 + 多渠道推送（微信/飞书/Telegram）
> GitHub Actions 零成本定时运行，LLM 综合研判，回测 agent，每日自动生成分析报告

#### 📈 决策

📈 **[trading-copilot](https://github.com/zinan92/trading-skills-catalog)** — 交易副驾驶
> `决策` · 输入: 你的交易想法（自然语言） → 输出: 方法论匹配 + 结构化交易建议
> 44 套交易方法论 system prompt + MiniMax/Anthropic 双引擎，免费在线使用

### 开发工具 `框架 → 自动化 → 增强`

#### 🏗️ 框架

🤖 **[agent-core](https://github.com/zinan92/agent-core)** — Agent 操作系统
> `框架` · 输入: agent 配置 → 输出: 可运行的 agent 实例
> 一个由 agent 自己造的 agent OS，提供生命周期管理、工具注册、记忆系统

🧩 **[skills-repo](https://github.com/zinan92/skills-repo)** — AI Agent 技能仓库
> `框架` · 输入: 技能名称/领域 → 输出: frontmatter 路由匹配的技能文件
> 61 个技能，按领域分组（交易/内容/开发/分析），支持 Claude Code / OpenClaw

🔭 **[proactive-explorer](https://github.com/zinan92/proactive-explorer)** — 产品方向探测器
> `框架` · 输入: GitHub repo URL → 输出: 5 维竞品分析 + 优先级排序的产品方向
> 帮 v1 项目找到下一步该造什么，竞品分析 + 社区信号 + 机会评估

#### 🔧 自动化

🍴 **[CLI-Anything](https://github.com/HKUDS/CLI-Anything)** — 任何软件一键生成 CLI
> `自动化` · 输入: 源代码（本地或 GitHub） → 输出: 生产级 Python CLI 包（Click + JSON 输出 + REPL + 测试）
> 7 阶段管线：分析 → 设计 → 实现 → 测试 → 文档 → 发布。让所有软件 Agent-Native

🍴 **[bb-browser](https://github.com/zinan92/bb-browser)** — 浏览器即 API
> `自动化` · 输入: 自然语言指令 → 输出: 浏览器操作结果
> CLI + MCP 服务器，让 AI agent 操控 Chrome，网页数据提取

🍴 **[opencli](https://github.com/zinan92/opencli)** — 网站变 CLI
> `自动化` · 输入: 网站 URL + 操作意图 → 输出: 提取的数据/操作结果
> AI 原生浏览器自动化，把任何网站变成命令行工具

🍴 **[agent-browser](https://github.com/zinan92/agent-browser)** — Agent 浏览器自动化
> `自动化` · 输入: 页面快照 + 操作指令 → 输出: 交互结果 + 截图
> 快照驱动的浏览器自动化 CLI，配合 dev server 测试和 E2E 验证

#### 🔌 增强

🍴 **[superpowers](https://github.com/obra/superpowers)** — AI 编程工作流引擎
> `增强` · 输入: 功能需求/开发任务 → 输出: 设计文档 + 实现计划 + 测试通过的代码 + 代码审查报告
> 完整的 7 阶段开发方法论（设计 → 计划 → 编码 → 测试 → 审查 → 验证 → 完成），强制 TDD，子 agent 并行分解任务

🍴 **[web-access](https://github.com/eze-is/web-access)** — Claude Code 完整联网能力
> `增强` · 输入: 自然语言查询 → 输出: 网页内容/截图/提取数据
> 三层通道调度（WebSearch → CDP 浏览器 → curl），登录态保持，并行子 agent 调研，站点知识持久化

🍴 **[lossless-claw](https://github.com/zinan92/lossless-claw)** — 无损上下文管理
> `增强` · 输入: OpenClaw 会话 → 输出: 压缩前自动保存的上下文快照
> OpenClaw 插件，防止上下文压缩丢失关键信息

🍴 **[skill-vetter](https://github.com/openclaw/skills/tree/main/skills/spclaudehome/skill-vetter)** — 技能质量检查
> `增强` · 输入: 技能文件 → 输出: 质量评分 + 改进建议
> 自动检查技能的 frontmatter、触发条件、模板规范

🍴 **[self-improving-agent](https://github.com/zhaono1/agent-playbook/tree/main/skills/self-improving-agent)** — 自我进化 Agent
> `增强` · 输入: agent 运行日志 → 输出: 优化后的 agent 配置
> 分析执行历史，自动调优 agent 行为和提示词

---

## 活跃度

![GitHub Contribution Graph](https://ghchart.rshah.org/zinan92)

---

## 冷知识

我所有的 repo 要么是为了赚钱，要么是为了省时间。通常两个都是。

```
行情走势:  ████████████████▄▄  📈
我的睡眠:  ▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄  📉
```
