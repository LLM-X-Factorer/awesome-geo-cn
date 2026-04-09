# Awesome GEO 中文资源 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 中文世界的 GEO（Generative Engine Optimization，生成式引擎优化）资源列表。
>
> 专注于中国 AI 搜索生态：Kimi、DeepSeek、文心一言、豆包、通义千问，以及知乎、小红书等中文内容平台的 GEO 策略。

GEO 的目标不是让你在搜索结果中排名靠前，而是**让 AI 在回答问题时引用你的内容**。这是和传统 SEO 最本质的区别。

---

## 目录

- [入门资源](#入门资源)
- [学术论文](#学术论文)
- [中文 AI 生态地图](#中文-ai-生态地图)
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

---

## 学术论文

| 论文 | 来源 | 核心发现 |
|------|------|---------|
| [GEO: Generative Engine Optimization](https://arxiv.org/abs/2311.09735) | KDD 2024 (IIT Delhi + Princeton) | 权威引述 +43%，统计数据 +33%，答案优先 +18% |
| [Generative Engine Optimization (GEO) and the Future of Search](https://dl.acm.org/doi/10.1145/3726302.3730401) | KDD 2024 Workshop | GEO 概念框架和评估方法 |

### 后续研究（2025+）

| 论文 | 来源 | 核心发现 |
|------|------|---------|
| [大语言模型检索增强生成优化技术研究综述](http://cjc.ict.ac.cn/online/onlinepaper/008_yl-2026227143149.pdf) | 中国科学院计算所《计算机学报》2026 | 中文一手 RAG 综述，覆盖 query 改写、检索增强、知识注入、引用生成等优化技术 |
| [Self-Promotion in LLM Recommendations](https://sorelle.friedler.net/papers/LLMselfpromotion.pdf) | Friedler et al. 2025 | LLM 推荐 AI 产品时存在自我推广偏差：供应商模型 ranking 平均提升 0.2，OpenAI 最显著 |
| [LLMs are Biased Evaluators But Not Biased for Fact-Centric Contexts](https://aclanthology.org/2025.findings-acl.1369.pdf) | ACL 2025 Findings | RAG 场景下的偏差层级：事实性偏差 > 顺序偏差 > 自我偏好偏差 |

### 关键量化数据（来自 KDD 2024 论文）

| 优化策略 | AI 可见度提升 |
|---------|-------------|
| 引用权威来源（Cite Credible Sources） | +43% |
| 嵌入统计数据（Add Statistics） | +33% |
| 答案优先结构（Answer-first） | +18% |
| 技术术语优化 | +11% |
| 关键词堆砌 | **负效果** |

---

## 中文 AI 生态地图

中文 AI 搜索不是独立产品之间的竞争，是四大互联网大厂生态闭环之间的竞争。每家大厂的结构包含：大模型产品 + 内容平台矩阵 + 创作者入口 + 开放文档。

### 字节系

**大模型**：豆包大模型（算法备案号 [网信算备110108823483901230031号](https://www.doubao.com/legal/instructions)）

**生态构成**：根据官方算法备案公示，豆包大模型算法应用于 **今日头条 / 抖音 / 剪映 / 番茄小说 / 西瓜视频 / 飞书 / 豆包 / 悟空浏览器 / 懂车帝** 9 个平台。

**官方资源**：

- [火山引擎文档中心](https://www.volcengine.com/docs) — 总入口
- [豆包助手 API](https://www.volcengine.com/docs/82379/1978533) — 同源企业级 API
- [火山方舟 RAG 解决方案](https://www.volcengine.com/docs/82379/1263276) — 官方 RAG 实现
- [豆包语音 API](https://www.volcengine.com/docs/6561/1096680) — 多模态能力
- [豆包算法备案公示](https://www.doubao.com/legal/instructions) — 法定公开的算法说明

**独立搜索产品**：AI 抖音 / 头条搜索 / 悟空搜索 / 闪电搜索

**关键数据**：

- 2026 年 2 月 MAU 2.26 亿（QuestMobile）
- 2025 年 9 月底日均 token 调用量 30 万亿（艾瑞《2025 年中国 AI+互联网媒体行业研究报告》）

### 腾讯系

**大模型**：腾讯混元大模型（Tencent HY，备案号 网信算备440305295988701230071号）

**生态构成**：腾讯元宝（C 端 AI 助手）+ 微信公众号 + 视频号 + 微信搜一搜 + QQ 浏览器

**官方资源**：

- [腾讯混元大模型产品页](https://cloud.tencent.com/product/tclm) — 总入口
- [混元 API 概览](https://cloud.tencent.com/document/product/1729/101848) — 完整 API 列表
- [混元 OpenAI 兼容接口](https://cloud.tencent.com/document/product/1729) — SDK 与开发者文档
- [混元 API Key 管理](https://cloud.tencent.com/document/product/1729/111008) — 开发者入口

**模型系列**：Tencent HY 2.0 Think / Instruct、Hunyuan-T1、Hunyuan-TurboS、Hunyuan-A13B、Hunyuan-Translation、Hunyuan-Vision

**关键事实**：元宝打通微信公众号内容库，可直接调用微信公众号、视频号等内容资源（2025 年腾讯官方公告）

### 阿里系

**大模型**：通义千问（Qwen）系列

**生态构成**：千问 App（C 端超级入口，2025 年 11 月上线）+ 夸克（AI 搜索入口）+ UC 浏览器 + 淘宝 AI

**官方资源**：

- [阿里云百炼 Model Studio](https://help.aliyun.com/zh/model-studio/) — 总入口
- [千问 API 参考](https://help.aliyun.com/zh/model-studio/qwen-api-reference/) — API 文档
- [百炼插件广场](https://help.aliyun.com/zh/model-studio/plug-in-overview) — 含 `quark_search` 官方搜索插件
- [AI 网关联网搜索策略](https://help.aliyun.com/zh/api-gateway/ai-gateway/user-guide/networked-search) — 官方文档明确"搜索引擎支持：夸克搜索引擎"
- [Qwen GitHub](https://github.com/QwenLM) — 开源模型仓库

**关键数据**：

- 2026 年 1 月千问 MAU 破 1 亿，DAU 3500-4000 万
- Qwen 系列全球累计下载 6 亿次，衍生模型 17 万（2025 年 11 月阿里官方数据）
- Qwen3-Max 基于 36T tokens 训练，覆盖 119 种语言

### 百度系

**大模型**：文心一言（ERNIE Bot）

**生态构成**：文心一言（C 端）+ 百度搜索 AI 概览 + 百家号 + 百度百科 + 百度文库

**官方资源**：

- [百度智能云千帆平台](https://qianfan.cloud.baidu.com/) — 总入口
- [文心一言 C 端入口](https://yiyan.baidu.com/) — 对话产品
- [ERNIE 开发文档](https://ai.baidu.com/ai-doc/WENXINWORKSHOP/) — 开发者文档
- [百度智能云 API 中心](https://cloud.baidu.com/doc/API/index.html) — API 总目录
- [千帆社区](https://qianfan.cloud.baidu.com/qianfandev/) — 开发者社区

**关键数据**：

- 百度搜索份额从 86.8%（2021 年 11 月）下降到 55.9%（2024 年 5 月），数据来源：沙利文《2025 年中国 AI 搜索行业白皮书》

### 独立内容平台

不属于四大大厂、但被所有中文 AI 引擎广泛引用的高质量内容社区：

| 平台 | 类型 | 备注 |
|------|------|------|
| [知乎](https://www.zhihu.com/) | 问答社区 | 中文 AI 引擎广泛引用，引用率数据见 [行业数据](#行业数据) |
| [小红书](https://www.xiaohongshu.com/) | 图文 + 短视频 | 内容被百度索引后可间接影响百度系 AI |
| [B 站](https://www.bilibili.com/) | 视频 + 专栏 | 字幕可被 AI 索引 |

### 独立大模型产品

不属于大厂生态、在中文市场有影响力的第三方 AI 产品：

| 产品 | 公司 | 备注 |
|------|------|------|
| [Kimi](https://kimi.moonshot.cn/) | 月之暗面 | 长上下文优势，相对中立 |
| [DeepSeek](https://www.deepseek.com/) | 深度求索 | 开源推理模型，相对中立 |

---

## 技术实现

### llms.txt

为 AI 爬虫提供结构化的网站内容导航。类似于 sitemap.xml 对搜索引擎的作用。

- [llms.txt 官方规范](https://llmstxt.org/)

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

常用类型：`FAQPage` / `Person` / `Course` / `HowTo` / `Article`。

参考：[Schema.org 官方文档](https://schema.org/)

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
