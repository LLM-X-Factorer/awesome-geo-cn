# Awesome GEO 中文资源 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 中文世界的 GEO（Generative Engine Optimization，生成式引擎优化）资源列表。
>
> 专注于中国 AI 搜索生态：Kimi、DeepSeek、文心一言、豆包、通义千问，以及知乎、小红书等中文内容平台的 GEO 策略。

GEO 的目标不是让你在搜索结果中排名靠前，而是**让 AI 在回答问题时引用你的内容**。这是和传统 SEO 最本质的区别。

---

## 目录

- [入门资源](#入门资源)
- [学术论文](#学术论文)
- [中文 AI 搜索引擎](#中文-ai-搜索引擎)
- [中文平台 GEO 策略](#中文平台-geo-策略)
- [技术实现](#技术实现)
- [工具](#工具)
- [课程与教程](#课程与教程)
- [行业数据](#行业数据)
- [英文资源（精选）](#英文资源精选)
- [贡献指南](#贡献指南)

---

## 入门资源

### GEO 是什么

- **GEO（Generative Engine Optimization）** — 针对生成式 AI 搜索引擎优化内容，使其被 AI 引用和推荐的策略
- **核心区别**：SEO 优化搜索排名（争点击），GEO 优化 AI 引用（争被引用）
- **关键数据**：SEO 排名靠前的页面和 AI 引用率高的页面，重叠率只有 12%（Ahrefs 2025）

### SEO 和 GEO 的关系

| 维度 | SEO | GEO |
|------|-----|-----|
| 优化对象 | Google/百度排名 | AI 生成回答中的引用 |
| 核心机制 | 关键词匹配 + 链接权重 | 内容质量 + 结构化 + 权威性 |
| 流量模式 | 用户点击链接 | AI 引用你的内容 |
| 衡量指标 | 排名、CTR、流量 | 引用频率、品牌提及 |

**结论**：SEO 是地基，GEO 是新楼层。96% 被 AI 引用的内容都有强 E-E-A-T 信号——SEO 基本功仍然是一切的基础。

---

## 学术论文

| 论文 | 来源 | 核心发现 |
|------|------|---------|
| [GEO: Generative Engine Optimization](https://arxiv.org/abs/2311.09735) | KDD 2024 (IIT Delhi + Princeton) | 权威引述 +43%，统计数据 +33%，答案优先 +18% |
| [Generative Engine Optimization (GEO) and the Future of Search](https://dl.acm.org/doi/10.1145/3726302.3730401) | KDD 2024 Workshop | GEO 概念框架和评估方法 |

### 关键量化数据（来自 KDD 2024 论文）

| 优化策略 | AI 可见度提升 |
|---------|-------------|
| 引用权威来源（Cite Credible Sources） | +43% |
| 嵌入统计数据（Add Statistics） | +33% |
| 答案优先结构（Answer-first） | +18% |
| 技术术语优化 | +11% |
| 关键词堆砌 | **负效果** |

---

## 中文 AI 搜索引擎

### 平台概览

| 平台 | 公司 | 引用偏好 | GEO 策略要点 |
|------|------|---------|-------------|
| **Kimi** | 月之暗面 | 相对中立 | 内容质量优先，独立站有机会 |
| **DeepSeek** | 深度求索 | 相对中立 | 同上，对结构化内容友好 |
| **文心一言** | 百度 | 偏爱百度系 | 百家号、百度百科优先，独立站需额外努力 |
| **豆包** | 字节跳动 | 偏爱字节系 | 抖音、头条内容优先 |
| **通义千问** | 阿里巴巴 | 偏爱阿里系 | 阿里系平台内容优先 |

### 关键发现

- **知乎是唯一被所有中文 AI 引擎引用的平台**，AI 引用率达 29.9%
- 各平台引用来源重叠率极低（英文三大平台仅 11%，中文可能更低）
- Kimi 和 DeepSeek 对独立网站最友好（无平台偏见）

---

## 中文平台 GEO 策略

### 知乎（最高优先）

知乎在中文 GEO 中的地位 = Reddit 在英文 GEO 中的地位（Reddit AI 引用率 40.1%）。

**为什么知乎重要**：
- 问答格式天然匹配 AI 检索逻辑
- 投票机制帮 AI 做了一层质量预筛选
- 不属于任何 AI 公司，所有引擎都引用

**优化要点**：
- 回答第一段直接给结论（答案优先 +18%）
- 加入具体数据和来源引用（统计数据 +33%）
- 核心段落控制在 40-60 词，方便 AI 提取
- 盐值影响内容分发权重

### 小红书

- 百度收录率高，间接影响文心一言引用
- 图文格式需要配合文字版内容
- 适合消费决策类 GEO（"XX 推荐""XX 对比"）

### 微信公众号

- 微信搜一搜是独立的搜索生态
- 公众号文章被微信搜一搜收录后，可被微信内的 AI 功能引用
- 长文深度内容效果好

### B 站

- 字幕内容可被 AI 索引
- 适合教程类、评测类 GEO 内容

---

## 技术实现

### llms.txt

为 AI 爬虫提供结构化的网站内容导航。类似于 sitemap.xml 对搜索引擎的作用。

- [llms.txt 官方规范](https://llmstxt.org/)
- [llms.txt 实战：Hugo 课程网站配置案例](https://factorer.app/course/week-05/lesson-02-llms-txt-and-ai-crawlers/) — 45KB 结构化内容导航的设计思路

### robots.txt AI 爬虫配置

```
User-agent: GPTBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: Google-Extended
Allow: /
```

### Schema 结构化数据

- **FAQPage** — 最适合教育/知识类内容，天然匹配 AI 的"问题-答案"检索模式
- **Person + sameAs** — 建立跨平台实体一致性
- **Course / HowTo / Article** — 帮助 AI 理解内容类型

### 答案优先写作结构

```
## [问题式 H2 标题]

[50-80 字的答案块：直接回答问题，含具体数据或可操作结论]

[展开解释：为什么是这个答案，背景信息]

[补充细节：边缘情况、注意事项]
```

---

## 工具

### GEO 监测

| 工具 | 说明 | 价格 |
|------|------|------|
| [Ahrefs AI Overviews Tracker](https://ahrefs.com/) | 追踪 AI Overviews 中的品牌引用 | 付费 |
| [Semrush AI SEO Toolkit](https://www.semrush.com/) | AI 搜索可见度分析 | 付费 |
| [Profound](https://www.tryprofound.com/) | AI 搜索引用监测 | 付费 |

### 开源工具

| 工具 | 说明 |
|------|------|
| [gego](https://github.com/searchgame/gego) | GEO 优化命令行工具 |
| [geo-optimizer](https://github.com/nicolegoebel/geo-optimizer) | 内容 GEO 分析脚本 |

### 内容生成

| 工具 | 说明 |
|------|------|
| [md2red](https://github.com/LLM-X-Factorer/md2red) | Markdown 转小红书图文卡片 |

---

## 课程与教程

| 课程 | 语言 | 说明 |
|------|------|------|
| [SEO + GEO 入门课程](https://factorer.app/) | 中文 | 10 周 29 课，基于 KDD 2024 论文，覆盖 SEO + GEO + 中文 AI 平台策略。前 3 周免费 |
| [AI SEO: Mastering GEO](https://www.coursera.org/learn/seo-mastering-generative-engine-optimization-geo) | 英文 | Coursera 上的 GEO 课程 |
| [万智匯 SEOxGEO 入门课](https://geniushub.cc/geo/geo-course-recommendation/) | 繁体中文 | 61 单元视频课程 |

---

## 行业数据

| 数据点 | 来源 |
|--------|------|
| ChatGPT 月活 8.91 亿，占搜索 17.6% | SparkToro 2025 |
| Google 占搜索 77.9% | SparkToro 2025 |
| 60% Google 搜索不产生点击 | SparkToro 2025 |
| AI 搜索流量同比增长 527% | BrightEdge 2025 |
| SEO 和 GEO 排名重叠率仅 12% | Ahrefs 2025 |
| 出现在 4+ 平台的内容被引用概率 ×2.8 | KDD 2024 |
| 被 AI 引用的访客转化率是普通搜索的 4.4-23 倍 | BrightEdge 2025 |
| 知乎 AI 引用率 29.9% | IT 之家 2026 |
| Reddit AI 引用率 40.1% | SparkToro 2025 |

---

## 英文资源（精选）

| 资源 | 说明 |
|------|------|
| [awesome-geo](https://github.com/luka2chat/awesome-geo) | 英文 GEO 资源列表（244 stars） |
| [awesome-generative-engine-optimization](https://github.com/amplifying-ai/awesome-generative-engine-optimization) | 英文 GEO 资源指南（289 stars） |
| [Backlinko GEO Guide](https://backlinko.com/geo) | Brian Dean 的 GEO 指南 |
| [Search Engine Land - What is GEO](https://searchengineland.com/what-is-geo-generative-engine-optimization) | 定义和概述 |

---

## 贡献指南

欢迎提交 PR 添加中文 GEO 相关资源。请确保：

1. 资源与中文 GEO 生态相关（中国 AI 搜索引擎、中文内容平台、中文创作者）
2. 提供简要说明
3. 优先收录有数据支撑或实操价值的内容

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
