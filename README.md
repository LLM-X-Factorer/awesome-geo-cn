# Awesome GEO 中文资源 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 中文世界的 GEO（Generative Engine Optimization，生成式引擎优化）资源列表。
>
> 专注于中国 AI 搜索生态：Kimi、DeepSeek、文心一言、豆包、通义千问，以及知乎、小红书等中文内容平台的 GEO 策略。

GEO 关注内容在 AI 生成回答中被引用的情况；传统 SEO 关注内容在搜索结果中的排名。

---

## 目录

- [入门资源](#入门资源)
- [学术论文](#学术论文)
- [中文 AI 生态地图](#中文-ai-生态地图)
- [技术实现](#技术实现)
- [工具](#工具)
- [课程与教程](#课程与教程)
- [行业数据](#行业数据)
- [实测研究与测评](#实测研究与测评)
- [中文研究与索引项目](#中文研究与索引项目)
- [英文资源（精选）](#英文资源精选)
- [贡献指南](#贡献指南)

---

## 入门资源

### GEO 是什么

- **GEO（Generative Engine Optimization）** — 针对生成式 AI 搜索引擎优化内容，使其被 AI 引用和推荐的策略
- **核心区别**：SEO 优化搜索排名（争点击），GEO 优化 AI 引用（争被引用）
- **关键数据**：ChatGPT / Gemini / Copilot 引用的 URL 中，仅 12% 位于 Google 该查询的前 10 名（[Ahrefs 2025](https://ahrefs.com/blog/ai-search-overlap/)）

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
| [GEO: Generative Engine Optimization](https://arxiv.org/abs/2311.09735) | KDD 2024 (IIT Delhi + Princeton) | 添加引语 +41%、添加统计数据 +31%（位置加权字数，相对基线）；关键词堆砌 −8% |

### 后续研究（2025+）

| 论文 | 来源 | 核心发现 |
|------|------|---------|
| [大语言模型检索增强生成优化技术研究综述](http://cjc.ict.ac.cn/online/onlinepaper/008_yl-2026227143149.pdf) | 中国科学院计算所《计算机学报》2026 | 中文一手 RAG 综述，覆盖 query 改写、检索增强、知识注入、引用生成等优化技术 |
| [Self-Promotion in LLM Recommendations](https://sorelle.friedler.net/papers/LLMselfpromotion.pdf) | WebSci 2026（Dubash & Friedler） | LLM 推荐 AI 产品时存在自我推广偏差：供应商自家模型排名比基准表现应得位置平均高约 0.2 位 |
| [LLMs are Biased Evaluators But Not Biased for Fact-Centric Contexts](https://aclanthology.org/2025.findings-acl.1369.pdf) | ACL 2025 Findings | RAG 场景下的偏差层级：事实性偏差 > 顺序偏差 > 自我偏好偏差 |
| [C-SEO Bench: Does Conversational SEO Work?](https://openreview.net/forum?id=oTeixD3oZO) | NeurIPS 2025 D&B | 多任务 / 多领域 / 多竞争密度严格控制下，多数 GEO 方法基本无效；多方同时使用 GEO 时效果互相抵消 |
| [AutoGEO: What Generative Search Engines Like and How to Optimize Web Content Cooperatively](https://openreview.net/forum?id=K8EinVWtUB)（[GitHub](https://github.com/cxcscmu/AutoGEO)） | ICLR 2026 | 由前沿 LLM 自动抽取生成式引擎的内容偏好规则，并以 GRPO 训练小模型 AutoGEO_Mini 执行改写，提出"协作式"内容优化框架 |
| [MAGEO: Multi-Agent GEO via Reusable Strategy Learning](https://github.com/Wu-beining/MAGEO) | ACL 2026 Findings | Multi-agent 协作学习 GEO 策略，把"经验"沉淀为可复用技能 |
| [E-GEO: A Testbed for GEO in E-Commerce](https://arxiv.org/abs/2511.20867) | 2025 | 电商 GEO benchmark（v2：13,747 条 query，各配 10 个 Amazon listing），评测 15 种 rewriting heuristics |
| [Generative Engine Optimization: How to Dominate AI Search](https://arxiv.org/abs/2509.08919) | 2025 | AI 搜索引擎系统性偏向 earned media（第三方报道、行业媒体）而非品牌自有内容 |
| [What Gets Cited: Competitive GEO in AI Answer Engines](https://arxiv.org/abs/2605.25517) | SIGIR 2026（Sprinklr） | 双文档受控测试床、252,000 次成对 A/B：主题相关性与列表位置影响最大，明确价格与较新时间戳稳定有益，纯格式化改动影响可忽略 |
| [Source Coverage and Citation Bias in LLM vs. Traditional Search](https://arxiv.org/abs/2512.09483) | 2025 | 5.6 万查询实证：37% 被引域名为 LLM 搜索引擎独有、信源更多样，但可信度 / 政治中立性 / 安全性未优于传统搜索 |
| [Don't Measure Once: Measuring Visibility in AI Search](https://arxiv.org/abs/2604.07585) | 圣加仑大学 2026 | 主张可见度应作为分布而非单点测量；4 引擎 45 天实测，相邻两日被引信源集合重叠仅 34–42% |
| [Structural Feature Engineering for GEO（GEO-SFE）](https://arxiv.org/abs/2603.29979) | 东京大学等 2026 | 纯结构（非语义）三层级特征工程使引用率相对提升 17.3%（p<0.001，n=200），覆盖 6 个生成引擎 |
| [GEO: A VLM and Agent Framework for Pinterest Acquisition Growth](https://arxiv.org/abs/2602.02961) | Pinterest 2026 | 生产级多模态 GEO 框架，部署于数十亿图片 / 数千万合集，带来 20% 自然流量增长 |
| [SAGEO Arena: Evaluating Search-Augmented GEO](https://arxiv.org/abs/2602.12187) | KDD 2026 | 含检索与重排的端到端生成式搜索环境：现有 GEO 方法在真实条件下大多不实用，且常降低检索与重排表现；结构化信息（如 Schema）可缓解 |
| [How Generative AI Disrupts Search](https://arxiv.org/abs/2604.27790) | SIGIR 2026 | 11,500 条真实查询：51.5% 触发 AI Overview；Google 搜索 / AIO / Gemini 信源平均 Jaccard <0.2；屏蔽 Google AI 爬虫的站点更少被 AIO 检索 |
| [CHASE: How Content Ecosystems Are Reshaped When Ranking Is the Only Target](https://arxiv.org/abs/2608.30466) | COLM 2026 | 模拟内容创作者反复针对 LLM 排序信号优化文档时，内容生态随之变化（同质化）的受控框架 |
| [Position: GEO Creates Underexamined Risks](https://arxiv.org/abs/2606.12439) | ICML 2026 Position Track | 指出 GEO 的三类风险：影响力集中、未披露的商业影响、学界与产业评测之间的盲区 |
| [A Critical Survey of GEO (2023–2026)](https://arxiv.org/abs/2607.14035) | 2026 | 45 项研究的批判性综述：主题相关性与上下文位置是最可复现的因素；未发现在跨平台、纵向上稳定提升自然可发现性的技术 |
| [GEO-Flag: Detecting and Measuring GEO-Optimized Web Content](https://arxiv.org/abs/2608.16824) | 2026 | GEO 内容检测基准与方法；在 10,095 个真实检索页面中估计 GEO 优化内容占 8.90%，2026 年修改的页面中占 16.36% |

### 中文 AI 搜索实证研究

| 论文 | 来源 | 核心发现 |
|------|------|---------|
| [What Do Chinese-Language Generative Search Engines Cite and Surface?](https://arxiv.org/abs/2607.15771) | 2026 | 4 个主流中文平台 Web + App 共 8 个入口、16 万条引用记录：品牌从引用池进入答案的比例 8.3%；被引页面半衰期约 39 天（高时效查询）/ 68 天（低时效）；同平台 App 与 Web 信源集合存在系统性差异 |
| [Auditing Source Exposure in Baidu and Google AI Search](https://arxiv.org/abs/2609.24407) | WAC @ EMNLP 2026 | 百度与 Google 的 AI 概览跨语言审计：各平台-语言组合在概览触发率与可见信源上差异显著，信源域名重叠度低 |
| [Who Anchors AI Overviews in Health? Baidu, Google, and the Geography of Authority](https://arxiv.org/abs/2609.06798) | 2026 | 12 国 4 语言 1,920 条健康查询：百度与 Google 的 AI 概览均倾向引向自家平台；改用当地官方语言提问，本地信源占比提升约 3.5–13.5 倍 |

### 引用机制与对抗性研究

| 论文 | 来源 | 核心发现 |
|------|------|---------|
| [What Evidence Do Language Models Find Convincing?（ConflictingQA）](https://arxiv.org/abs/2402.11782) | ACL 2024 | LLM 判断证据时高度依赖与查询的相关性，基本忽略是否含科学引用、是否中立语气等风格特征 |
| [ConflictBank](https://arxiv.org/abs/2408.12076) | NeurIPS 2024 D&B | 7.4M claim-evidence 对，研究 LLM 在外部内容与训练数据冲突时如何抉择 |
| [GASLITE: SEO Attacks on Dense Retrieval](https://arxiv.org/abs/2412.20953) | CCS 2025 | 向 880 万段语料插入 10 段文本（≤0.0001%），6/9 个检索器对同概念未见查询的 appeared@10 超过 50% |
| [Adversarial SEO for LLMs](https://arxiv.org/abs/2406.18382) | ICLR 2025 | 网页中的 prompt injection 可使 Bing 推荐目标产品的概率达对照产品的 2.5 倍 |
| [Ranking Manipulation for Conversational Search](https://arxiv.org/abs/2406.03589) | EMNLP 2024 | 通过 prompt injection 操纵对话式搜索排名 |
| [Dynamics of Adversarial Attacks on LLM-Based Search](https://arxiv.org/pdf/2501.00745) | ICML 2026 Workshop | 将 LLM 搜索中内容发布者间的攻击行为建模为无限重复囚徒困境 |
| [GEO-Bench: Benchmarking Ranking Manipulation in GEO](https://arxiv.org/abs/2605.29107) | 2026 | GEO 攻防统一基准：黑盒内容改写在排名提升上可匹配 / 超过白盒梯度攻击，且文本更流畅、可同时规避关键词与困惑度检测 |
| [FACTUM: Mechanistic Detection of Citation Hallucination in Long-Form RAG](https://arxiv.org/abs/2601.05866) | ECIR 2026 | 将"引用幻觉"建模为注意力与前馈通路的协调失败，4 种机制性打分法检测虚假引用，AUC 较 SOTA 最高 +37.5% |
| [Counter-GEO-Bench](https://arxiv.org/abs/2609.02316) | EMNLP 2026 | 针对信息扭曲型 GEO 的防御基准：3 种现成防护（Granite Guardian / Llama Guard 3 / NeMo）攻击成功率相对降幅最多 5.7% |
| [One Polluted Page Is Enough（FORGE）](https://arxiv.org/abs/2606.13610) | EMNLP 2026 Findings | 12 个 LLM 推荐系统均受网页污染影响：单个污染页面误荐率最高 27%，前 3 条全部替换时达 73.8%；推理模式不能缓解 |
| [SafeGEO: GEO Risks in Recommendation Agents](https://arxiv.org/abs/2606.28356)（[GitHub](https://github.com/QianfengWen/SafeGEO)） | EMNLP 2026 | 22 种 GEO 攻击变体 × 600 个推荐案例：缺陷产品进入推荐集的比例最多提升 83.2 个百分点 |
| [Evaluating Deep-Search Agents under Hierarchical Web Evidence Poisoning（HAE-GEO）](https://arxiv.org/abs/2609.06027) | 2026 | 追踪深度搜索智能体从接触投毒证据到识别、修正的完整轨迹的基准 |
| [Assessing Attack Surfaces in Generative Search Engines through Publisher Attributes](https://arxiv.org/abs/2608.15814) | CIKM 2026 | 政治领域生成式搜索引擎的投毒攻击面分析，从引用选择与个性化两个角度 |

### 关键量化数据（来自 KDD 2024 论文）

论文 Table 1，指标为位置加权字数（Position-Adjusted Word Count，Overall），相对无优化基线（19.3）：

| 优化策略 | 可见度变化 |
|---------|-----------|
| 添加引语（Quotation Addition） | +41% |
| 添加统计数据（Statistics Addition） | +31% |
| 流畅度优化（Fluency Optimization） | +28% |
| 引用来源（Cite Sources） | +27% |
| 技术术语（Technical Terms） | +18% |
| 易懂化（Easy-to-Understand） | +14% |
| 权威语气（Authoritative） | +10% |
| 独特词汇（Unique Words） | +6% |
| 关键词堆砌（Keyword Stuffing） | −8% |

另：Cite Sources 对原 SERP 排名第 5 的来源可见度提升 115.1%（论文 Table 2）。

---

## 中文 AI 生态地图

以下按四大互联网厂商生态组织，每个生态包含：大模型产品 + 内容平台矩阵 + 创作者入口 + 开放文档。

### 字节系

**大模型**：豆包大模型（算法备案号 [网信算备110108823483901230031号](https://www.doubao.com/legal/instructions)）

**生态构成**：根据官方算法备案公示，豆包大模型算法应用于 **今日头条 / 抖音 / 剪映 / 番茄小说 / 西瓜视频 / 飞书 / 豆包 / 悟空浏览器 / 懂车帝** 9 个平台。

**官方资源**：

- [火山引擎文档中心](https://www.volcengine.com/docs) — 总入口
- [豆包助手 API](https://www.volcengine.com/docs/82379/1978533) — 同源企业级 API
- [火山方舟 RAG 解决方案](https://www.volcengine.com/docs/82379/1263276) — 官方 RAG 实现
- [豆包语音 API](https://www.volcengine.com/docs/6561/1096680) — 多模态能力
- [豆包算法备案公示](https://www.doubao.com/legal/instructions) — 法定公开的算法说明

**创作者规则**：

- [抖音内容标识使用规范](https://95152.douyin.com/article/7151778480801102) — AI 生成、转载、营销推广等内容须添加对应自主声明标识，未标或错标可被限制传播（2023-09 首发，2026-05-11 修订生效）
- [抖音关于升级 AI 内容标识功能的公告](https://95152.douyin.com/article/69831756697378034) — 创作者主动声明"内容由 AI 生成"，平台对未标识的疑似 AI 内容补充显式标识，并为所有 AI 内容写入隐式标识（2025-09-01 起试行）
- [抖音关于 AI 生成内容管理的答疑公告](https://95152.douyin.com/article/15741764841795469) — 主动声明或含 AI 数字水印的内容不影响分发；未声明而被判定"疑似 AI"的内容可能影响分发（2025-12）
- [抖音关于加强 AI 生成内容管理的公告](https://95152.douyin.com/article/98871770975704696) — 未主动声明的 AI 视频限制传播；重点整治类型含"利用 AI 搭建矩阵账号，批量生成低质内容"（2026-02）
- [抖音关于持续规范信息来源标注的公告（第一期）](https://95152.douyin.com/article/27471774868064641) — 时事、公共政策、社会热点类内容须标注信息来源（2026-03）
- [豆包搜索：站点权威度分级说明](https://www.volcengine.com/docs/87772/2518319) — 豆包搜索将信源分为非常权威 / 正常权威 / 一般权威 / 一般不权威四级，并列出"非常权威"站点范围（政府网站、央媒、985/211 高校官网等）（火山引擎，2026-06 首发，2026-08 更新）

**独立搜索产品**：AI 抖音 / 头条搜索 / 悟空搜索 / 闪电搜索

**关键数据**：

- 2026 年 6 月月活 3.82 亿（[QuestMobile《2026 年 AI 应用市场发展半年报》](https://www.questmobile.com.cn/research/report/2076954943839809537/)）
- 截至 2026 年 6 月日均 tokens 调用量 180 万亿（2026 火山引擎 FORCE 大会，[IT之家](https://www.ithome.com/0/967/330.htm)）

### 腾讯系

**大模型**：腾讯混元大模型（Tencent HY，备案号 网信算备440305295988701230071号）

**生态构成**：腾讯元宝（C 端 AI 助手）+ 微信公众号 + 视频号 + 微信搜一搜 + QQ 浏览器

**官方资源**：

- [腾讯混元大模型产品页](https://cloud.tencent.com/product/tclm) — 总入口
- [混元 API 概览](https://cloud.tencent.com/document/product/1729/101848) — 完整 API 列表
- [混元 OpenAI 兼容接口](https://cloud.tencent.com/document/product/1729) — SDK 与开发者文档
- [混元 API Key 管理](https://cloud.tencent.com/document/product/1729/111008) — 开发者入口

**创作者规则**：

- [微信公众平台运营规范](https://mp.weixin.qq.com/mp/opshowpage?action=newoplaw) — 3.16 不当影响微信搜索及展示行为（关键词堆砌等）/ 3.27 非真人自动化创作行为（不得利用 AI、脚本、接口替代真人完成创作与发布）/ 3.28 套路化模板写作行为
- [微信公众号和服务号推荐运营规范](https://mp.weixin.qq.com/cgi-bin/announce?action=getannouncement&key=11697600328G0Tbo&version=1&lang=zh_CN&platform=2) — 7.4 低价值 AIGC 内容：AIGC 生成主体占比显著高于人工且未声明 AI 辅助创作等
- [关于进一步规范人工智能生成合成内容标识的公告](https://mp.weixin.qq.com/cgi-bin/announce?action=getannouncement&announce_id=117567151189fSNU&version=&lang=zh_CN) — 微信公众平台 AI 生成合成内容显式 / 隐式标识与发布者主动声明要求（2025-09-01）
- [微信视频号运营规范](https://weixin.qq.com/cgi-bin/readtemplate?lang=zh_CN&t=weixin_agreement&s=video) — 6.4 生成式 AI 等生成合成的非真实音视频内容应显著标识
- [为什么微信公众号文章搜不到｜搜一搜优化教程 02](https://mp.weixin.qq.com/s/FTNvYMAYvvgfg0qtH4QsGQ) — 微信搜一搜助手列出导致文章搜索封禁的 10 类因素（2023-01）

**模型系列**：[Hy4 preview](https://www.stdaily.com/web/gdxw/2026-08/28/content_571433.html)（2026-08 开源，总参数 770B / 激活 49B）、[Hy3](https://www.tencent.com/zh-cn/articles/2202320.html)（2026-04 preview）、Tencent HY 2.0 Think / Instruct、Hunyuan-T1、Hunyuan-TurboS、Hunyuan-A13B、Hunyuan-Translation、Hunyuan-Vision

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

**创作者规则**：

- [神马站长平台](https://zhanzhang.sm.cn/) — 神马搜索站点收录与提交入口；服务条款 2.6 条规定平台发布内容可自动同步至夸克、UC、大鱼号等阿里业务平台

**关键数据**：

- 2026 年 6 月千问 App 月活 1.67 亿（[QuestMobile 半年报](https://www.questmobile.com.cn/research/report/2076954943839809537/)）
- 2026 年 2 月千问（Qwen）C 端应用月活超 3 亿（阿里巴巴 2026 财年 Q3 财报）
- Qwen 系列全球累计下载超 30 亿次，衍生模型超 30 万个（阿里巴巴 2027 财年 Q1 财报，2026-08，[快科技](https://news.mydrivers.com/1/1145/1145195.htm)）
- [Qwen3.8](https://www.stdaily.com/web/gdxw/2026-08/03/content_558298.html) 2026-08-03 发布，总参数 2.4 万亿，Qwen3.8-Max / Qwen3.8-27B 已开源

### 百度系

**大模型**：文心大模型（ERNIE）

**生态构成**：文心 App（C 端，原文心一言，2025-11 更名）+ 百度搜索 AI 概览 + 百家号 + 百度百科 + 百度文库

**官方资源**：

- [百度智能云千帆平台](https://qianfan.cloud.baidu.com/) — 总入口
- [文心 C 端入口](https://wenxin.baidu.com/) — 对话产品（原 yiyan.baidu.com 已跳转至此）
- [ERNIE 开发文档](https://ai.baidu.com/ai-doc/WENXINWORKSHOP/) — 开发者文档
- [百度智能云 API 中心](https://cloud.baidu.com/doc/API/index.html) — API 总目录
- [千帆社区](https://qianfan.cloud.baidu.com/qianfandev/) — 开发者社区
- [百度搜索资源平台](https://ziyuan.baidu.com/) — 站长工具与收录提交（同时影响百度搜索 AI 概览结果池）
- [百度搜索学堂](https://ziyuan.baidu.com/college) — 官方搜索算法说明、白皮书与开发者教程
- [文心大模型 5.0（ERNIE 5.0）](https://ernie.baidu.com/blog/posts/ernie5.0/) — 原生全模态、2.4 万亿参数，2026-01-22 正式版（官方博客）
- [文心大模型 5.1（ERNIE 5.1）](https://ernie.baidu.com/blog/posts/ernie-5.1-0508-release/) — 官方称 LMArena Search Arena 1223 分（国产第一、全球第四），2026-05 发布（官方博客）

**创作者规则**：

- [AI 流量分析功能上线公告](https://ziyuan.baidu.com/wiki/3519) — 百度搜索资源平台提供站点内容被 AI 引用、曝光、点击的数据，分阶段开放（2026-09-15）
- [百度搜索的工作原理](https://ziyuan.baidu.com/college/articleinfo?id=3541) — 抓取、索引、排序流程，排序维度含相关性、权威性、时效性（2023-12）
- [百度搜索优质内容解读](https://ziyuan.baidu.com/college/articleinfo?id=3137) — 百度搜索对优质内容的定义与评估维度（2023-11）
- [百度搜索违规低质页面问题说明](https://ziyuan.baidu.com/college/articleinfo?id=3528) — 影响索引与展现的低质、作弊问题类型（2023-08）
- [百家号内容基础红线规则](https://ziyuan.baidu.com/college/articleinfo?id=3537) — 百家号内容审核红线与处罚机制（2023-10）

**关键数据**：

- 百度搜索份额从 86.8%（2021 年 11 月）下降到 55.9%（2024 年 5 月），数据来源：沙利文《2025 年中国 AI 搜索行业白皮书》

### 算法备案与监管

中文生成式 AI 服务受《互联网信息服务算法推荐管理规定》《互联网信息服务深度合成管理规定》《生成式人工智能服务管理暂行办法》约束，各厂商模型的网信算备号、备案状态以官方备案系统公示为准。

- [互联网信息服务算法备案系统](https://beian.cac.gov.cn) — 网信办官方备案查询入口，可核验各厂商网信算备编号
- [第十八批深度合成服务算法备案信息公告](https://www.cac.gov.cn/2026-07/17/c_1786032856662750.htm) — 网信办 2026-07-17 发布（深度合成算法按批次公示）
- [2025 年生成式人工智能服务已备案信息公告](https://www.cac.gov.cn/2026-01/09/c_1769688009588554.htm) — 截至 2025-12-31 累计 748 款服务备案、435 款应用登记（网信办）
- [生成式人工智能服务已备案信息公告（2026 年 7–8 月）](https://www.cac.gov.cn/2026-09/14/c_1791136833136332.htm) — 截至 2026-08-31 累计 1112 款服务备案、731 款应用登记（网信办）
- [人工智能拟人化互动服务管理暂行办法](https://www.cac.gov.cn/2026-04/10/c_1777558395078289.htm) — 五部门 2026-04-10 发布、2026-07-15 施行，规范持续性情感互动类 AI 服务
- [人工智能生成合成内容标识办法](https://www.cac.gov.cn/2025-03/14/c_1743654684782215.htm) — 四部门 2025-03-14 印发、2025-09-01 施行，规定 AI 生成合成内容的显式 / 隐式标识
- [「清朗·整治AI应用乱象」专项行动](https://www.cac.gov.cn/2026-04/30/c_1779289298718765.htm) — 中央网信办 2026-04-30 部署；整治问题中列明"使用 GEO（生成式搜索引擎优化）技术恶意营销等方式实施 AI 数据投毒"及"对引用信源缺乏交叉验证和风险提示机制，未标注引用信息链接"（[第一阶段](https://www.news.cn/politics/20260706/4ce1356eb1b34e878c3fa1e2d9e5da1f/c.html) / [第二阶段](https://www.cac.gov.cn/2026-09/02/c_1790099041364574.htm)工作通报）

### 独立内容平台

不属于四大大厂、但被所有中文 AI 引擎广泛引用的高质量内容社区：

| 平台 | 类型 | 备注 |
|------|------|------|
| [知乎](https://www.zhihu.com/) | 问答社区 | 中文 AI 引擎广泛引用，引用率数据见 [行业数据](#行业数据) |
| [小红书](https://www.xiaohongshu.com/) | 图文 + 短视频 | 内容被百度索引后可间接影响百度系 AI |
| [B 站](https://www.bilibili.com/) | 视频 + 专栏 | 字幕可被 AI 索引 |

**平台规则**：

- [知乎协议](https://www.zhihu.com/term/zhihu-terms) — 禁止抓取知乎内容用于大语言模型等研发或训练；知乎直答自动检索知乎社区、合作版权与互联网公开内容生成回答（2025-03-25 生效）
- [B 站：关于 AI 生成内容有序标识的公告](https://www.bilibili.com/opus/1106496554576904197) — 投稿时在「创作声明」中声明使用人工智能合成技术，未声明的由平台添加标识（2025-08）
- [B 站：关于整治 AI 技术滥用的公告](https://www.bilibili.com/opus/1065945930120822784) — 覆盖虚假信息、侵权、恶意行为、内容标识四类，未标注的 AI 内容限制传播或下架（2025-05）
- [B 站：关于开展「清朗·整治AI应用乱象」专项公告](https://www.bilibili.com/opus/1202507670848798745) — AI 标识选项前置至投稿一级页面，漏标内容按补标 / 打回 / 下架阶梯处置（2026-05）
- [B 站：关于自媒体信息来源标注规范的公告](https://www.bilibili.com/opus/1194416450727575574) — 引用新闻、媒体素材须在简介或画面标注来源与信源链接（2026-04）

### 独立大模型产品

不属于大厂生态、在中文市场有影响力的第三方 AI 产品：

| 产品 | 公司 | 备注 |
|------|------|------|
| [Kimi](https://www.kimi.com/) | 月之暗面 | 长上下文大模型，K 系列模型开源（[Kimi K3](https://www.news.cn/tech/20260717/01c04372f89a46e480206e1da2fb8e8c/c.html)，2026-07） |
| [DeepSeek](https://www.deepseek.com/) | 深度求索 | 开源大模型（V / R 系列；[V4 预览版](https://news.sciencenet.cn/htmlnews/2026/4/563641.shtm)，2026-04） |

---

## 技术实现

### llms.txt

为 AI 爬虫提供结构化的网站内容导航。类似于 sitemap.xml 对搜索引擎的作用。

- [llms.txt 官方规范](https://llmstxt.org/)
- [thedaviddias/llms-txt-hub](https://github.com/thedaviddias/llms-txt-hub) — llms.txt 采用站点目录与示例库，附 llmstxt-cli
- [Google：Optimizing for Generative AI Features on Google Search](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide) — Google 搜索官方 AI 功能优化指南，写明 Google 搜索不需要 llms.txt 等额外 AI 文本文件，并介绍 Search Console 生成式 AI 效果报告

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

**主流 AI 爬虫官方文档**（User-Agent、IP 段与 robots.txt 控制）：

- [OpenAI 爬虫总览](https://developers.openai.com/api/docs/bots) — GPTBot（训练）/ OAI-SearchBot（ChatGPT 搜索引用索引）/ ChatGPT-User / OAI-AdsBot
- [Anthropic 爬虫说明](https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler) — ClaudeBot（训练）/ Claude-User / Claude-SearchBot（搜索）
- [Perplexity 爬虫文档](https://docs.perplexity.ai/docs/resources/perplexity-crawlers) — PerplexityBot（搜索索引）/ Perplexity-User
- [Amazon 爬虫文档](https://developer.amazon.com/amazonbot) — Amazonbot / Amzn-SearchBot（Alexa、Rufus）/ Amzn-User
- [Applebot 与 Applebot-Extended](https://support.apple.com/en-us/119829) — 可在 robots.txt 中退出 Apple 基础模型训练
- [Google 常用爬虫文档](https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers) — 含 Google-Extended（控制 Gemini 训练与 grounding，无独立 User-Agent，不影响 Google 搜索）
- [百度 Baiduspider 说明](https://help.baidu.com/question?prod_en=master&class=Baiduspider) — 百度搜索爬虫官方 FAQ（百度未公布独立的 AI 训练退出 token）
- [华为 PetalBot 说明](https://webmaster.petalsearch.com/site/petalbot) — Petal 搜索爬虫官方说明

### 内容访问与许可标准

robots.txt 之上正在形成的机器可读 AI 用途 / 许可声明机制。

- [Cloudflare Content Signals Policy](https://blog.cloudflare.com/content-signals-policy/) — robots.txt 扩展，定义 search / ai-input / ai-train 三类用途信号（CC0，2025-09）
- [Cloudflare Pay Per Crawl](https://blog.cloudflare.com/introducing-pay-per-crawl/) — 以 HTTP 402 向未付费 AI 爬虫返回定价；配套 AI Crawl Control 已正式可用。2026-07 起 AI 爬虫按 Search / Training / Agent 三类管理，2026-09-15 起启用新默认值（[公告](https://blog.cloudflare.com/content-independence-day-ai-options/)）
- [RSL（Really Simple Licensing）1.0](https://rslstandard.org/rsl) — 机器可读内容许可标准，区分 ai-train / ai-input / ai-index / search 等用途（2025-12 发布）
- [IETF AI Preferences（aipref）工作组](https://datatracker.ietf.org/wg/aipref/about/) — 标准轨草案：AI 用途偏好词汇 + HTTP `Content-Usage` 头附着机制（更新 RFC 9309）

### 内容协商（向 AI 返回 Markdown）

同一 URL 对 AI 爬虫返回干净 Markdown、对人类返回 HTML 的开源方案。

- [dodopayments/dualmark](https://github.com/dodopayments/dualmark) — 基于 HTTP 内容协商的 AEO 基础设施，识别 24 个 AI bot、12 个内置转换器，附一致性评分 CLI（Apache 2.0）
- [continuedev/next-geo](https://github.com/continuedev/next-geo) — Next.js App Router 中间件，按 Accept 头 / `.md` 后缀 / User-Agent 返回 Markdown，并生成 llms.txt（Apache 2.0，2026-03 起已归档）

### Schema 结构化数据

常用类型：`FAQPage` / `Person` / `Course` / `HowTo` / `Article`。

参考：[Schema.org 官方文档](https://schema.org/) ｜ [版本发布记录](https://schema.org/docs/releases.html)（词汇逐版本变更，最新 v30.1，2026-09）

---

## 工具

### GEO 监测

| 工具 | 说明 | 价格 |
|------|------|------|
| [Ahrefs Brand Radar](https://ahrefs.com/brand-radar) | 追踪 ChatGPT / Perplexity / Gemini / Copilot / AI Overviews / AI Mode 中的品牌提及与引用 | 付费 |
| [Semrush AI Visibility Toolkit](https://www.semrush.com/kb/1493-ai-visibility-toolkit) | AI 搜索可见度分析（Semrush 已于 2026-04 被 Adobe 收购） | 付费 |
| [Profound](https://www.tryprofound.com/) | AI 搜索引用监测 | 付费 |
| [新榜智汇 Geowise](https://geo.newrank.cn/) | 中文 AI 搜索可见度与信源监测，覆盖豆包 / 元宝 / DeepSeek / 千问等 | 付费 |

### 开源工具

| 工具 | 说明 |
|------|------|
| [AI2HU/gego](https://github.com/AI2HU/gego) | Go 实现的 GEO 工具，追踪跨 LLM 的品牌曝光，提供 REST API |
| [aircodelabs/llms-txt-generator](https://github.com/aircodelabs/llms-txt-generator) | AI 驱动的 llms.txt / llms-full.txt 生成器，支持 MCP 集成 Cursor 与 Claude Desktop |
| [apify/actor-llmstxt-generator](https://github.com/apify/actor-llmstxt-generator) | Apify Actor 形式的 llms.txt 生成器，基于 Website Content Crawler |
| [Blimeo/llms-txt-generator](https://github.com/Blimeo/llms-txt-generator) | Web 应用 + Worker 系统，自动监控静态站点变化并生成 llms.txt |
| [nowork-studio/notfair-plugin](https://github.com/nowork-studio/notfair-plugin) | 面向 AI agent 的开源 SEO / GEO / 营销 skills 集（原 toprank） |
| [ngmisl/llmstxt](https://github.com/ngmisl/llmstxt) | Python 工具，将代码仓库压缩为 LLM 友好的单一 .txt 文件 |
| [infiniflow/ragflow](https://github.com/infiniflow/ragflow) | 开源 RAG 引擎，基于深度文档理解（GitHub 91k+ stars） |
| [danishashko/geo-aeo-tracker](https://github.com/danishashko/geo-aeo-tracker) | 开源、本地优先的 AI 可见性 dashboard（BYOK），覆盖 ChatGPT / Perplexity / Gemini / Copilot / Google AIO / Grok |
| [Auriti-Labs/geo-optimizer-skill](https://github.com/Auriti-Labs/geo-optimizer-skill) | 基于 Princeton KDD 2024 研究的 GEO 工具：审计 / 优化 / AI 可见性测试 |
| [onvoyage-ai/gtm-engineer-skills](https://github.com/onvoyage-ai/gtm-engineer-skills) | Claude Code skill 形式的 AEO/GEO 工具集，16 项基础检查 + 6 维度智能分析 |
| [aaron-he-zhu/seo-geo-claude-skills](https://github.com/aaron-he-zhu/seo-geo-claude-skills) | 20 个 SEO/GEO Claude Code skills，覆盖 keyword research / content writing / technical audits / rank tracking |
| [zubair-trabzada/geo-seo-claude](https://github.com/zubair-trabzada/geo-seo-claude) | GEO-first Claude Code skill：citability scoring / AI crawler analysis / brand authority / schema markup |
| [daijinma/geo_marketing](https://github.com/daijinma/geo_marketing) | 中文 AI 搜索 GEO 监测工具（LLM Sentry），本地优先桌面客户端，覆盖 DeepSeek / 豆包 / 博查，含引用域名提取与声量占比 |
| [yaojingang/yao-geo-skills](https://github.com/yaojingang/yao-geo-skills) | 中文 GEO Skill 开源合集，17 个 AI agent skill（运营 / 策略 / 内容 / 度量等七类），交付支持 Markdown/HTML/Word/PDF |
| [ViryaZheng/recomby-geo](https://github.com/ViryaZheng/recomby-geo) | GEO 工作流编排插件，整合 6 个 GEO skill + 七阶段协作工作流命令，含多种 agent CLI 与办公工具集成清单 |
| [FayAndXan/xanlens](https://github.com/FayAndXan/xanlens) | GEO 审计引擎，向 7 个 AI 引擎（含 DeepSeek / Qwen）发真实查询，自动生成模拟查询并按可引用性 0–100 评分 |
| [elmohq/elmo](https://github.com/elmohq/elmo) | AI 可见性追踪平台，监测 prompt 并分析跨平台引用（ChatGPT / Gemini / Copilot / Grok / Perplexity） |
| [anyin-ai/aperture](https://github.com/anyin-ai/aperture) | 自托管 AI 可见性监测（BYOK），追踪 ChatGPT / Perplexity 中的品牌呈现，含竞品基准与引用追踪 |
| [IJONIS/geo-lint](https://github.com/IJONIS/geo-lint) | GEO/SEO 内容 linter，按 97 条规则扫描 Markdown/MDX 并输出修复建议，提供 `npx geo-lint` CLI |
| [zilisrikle/geo-audit-skill](https://github.com/zilisrikle/geo-audit-skill) | 面向 Claude Code 的多 agent GEO 审计 skill，检测 15 个 AI 爬虫 + 六维可引用性评分（非商用协议） |
| [yaojingang/GEORank](https://github.com/yaojingang/GEORank) | 开源 GEO 诊断平台：可见性诊断、问答、拓词与结构化工具，支持私有化部署（Apache 2.0） |
| [HeiGeAi/HeiGe-GEO-SEO](https://github.com/HeiGeAi/HeiGe-GEO-SEO) | 面向豆包 / 千问 / DeepSeek / 文心 / 元宝的 GEO + SEO 内容优化系统，兼容 Claude Code / Codex（MIT） |
| [limelit-co/open](https://github.com/limelit-co/open) | 自托管 AI 可见性追踪（BYOK），单 Go 二进制 + SQLite，覆盖 ChatGPT / Claude / Perplexity / Gemini / AIO（Apache 2.0） |
| [leopard627/fire-your-seo-agency](https://github.com/leopard627/fire-your-seo-agency) | SEO / AEO / GEO / LLMO 审计与优化 Claude Code skill，含韩国 Naver 支持（MIT） |
| [OranAi-Ltd/orangeo-ai-visibility-skill](https://github.com/OranAi-Ltd/orangeo-ai-visibility-skill) | AI 可见性准备度检查 skill：robots.txt / llms.txt / Schema / 引用信号 / 竞品差距（MIT） |

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

---

## 行业数据

| 数据点 | 来源 |
|--------|------|
| 美国 58.5% / 欧盟 59.7% 的 Google 搜索为零点击 | [SparkToro × Datos 2024](https://sparktoro.com/blog/2024-zero-click-search-study-for-every-1000-us-google-searches-only-374-clicks-go-to-the-open-web-in-the-eu-its-360/) |
| 19 个 GA4 站点 AI 来源会话同比 +527%（2025 年 1–5 月 vs 2024 年同期） | [Previsible 2025](https://searchengineland.com/ai-traffic-up-seo-rewritten-459954) |
| ChatGPT / Gemini / Copilot 引用的 URL 仅 12% 位于 Google 前 10 | [Ahrefs 2025](https://ahrefs.com/blog/ai-search-overlap/) |
| AI 搜索访客价值（按转化率）为传统自然搜索访客的 4.4 倍 | [Semrush 2025](https://www.semrush.com/blog/ai-search-seo-traffic-study/) |
| Ahrefs 自家站点 AI 搜索访客转化率为传统自然搜索的 23 倍（单站案例） | [Ahrefs 2025](https://ahrefs.com/blog/ai-search-traffic-conversions-ahrefs/) |
| 自设问题集测评中，AI 助手引用知乎频率 29.9%，内容社区中最高（B 站 7.6%） | [量子位智库 2025/05](https://www.qbitai.com/2025/05/285761.html) |
| 中国生成式 AI 用户规模突破 7 亿、普及率超 50%（截至 2026 年上半年） | [CNNIC《生成式人工智能应用发展报告（2026）》](https://www.21jingji.com/article/20260929/herald/b55c0ac8c4012cc9f5320c6bf5156b67.html) |
| AI 原生 App 月活 4.99 亿（2026-06：豆包 3.82 / 千问 1.67 / DeepSeek 1.29 亿） | [QuestMobile 2026 半年报](https://www.questmobile.com.cn/research/report/2076954943839809537/) |
| YouTube 提及与 AI 可见度相关性最高（≈0.737），高于品牌网络提及（0.66–0.71） | Ahrefs 2025（75K 品牌） |
| AI 搜索被引域名整体 Top：Reddit、YouTube、LinkedIn、Wikipedia、Forbes | Peec AI 2026（3000 万来源） |

---

## 实测研究与测评

除上文"行业数据"章节的单点数据外，以下是完整的评测基准和研究报告。

### 中文评测与报告

| 资源 | 机构 | 备注 |
|------|------|------|
| [SuperCLUE-AISearch](https://www.superclueai.com/) | SuperCLUE | 中文 AI 搜索专项基准测评 |
| [AI 搜索产品评估 2025](https://my.idc.com/getdoc.jsp?containerId=prCHC53702325) | IDC 中国 2025/07 | 百度 / 夸克 / 豆包 / DeepSeek 场景化对比，覆盖金融、法律、旅行规划等 |
| [2025 中国生成式 AI 市场五大趋势](https://www.rolandberger.com/zh/Insights/Publications/2025中国生成式AI市场的五大趋势分享.html) | 罗兰贝格 2025 | AI 智能体、多模态、硬件融合等趋势分析 |
| [2026 年 GEO 生成式引擎优化行业研究报告](https://pdf.dfcfw.com/pdf/H3_AP202602111819871548_1.pdf) | 艾瑞咨询 2026 | 中文 GEO 行业研究报告：定义、误区、案例、市场规模 |
| [GEO White Paper 2026](https://cn.ceibs.edu/sites/portal.prod1.dpmgr.ceibs.edu/files/GEO_White_Paper_2026.pdf) | 中欧国际工商学院（CEIBS）2026 | 学术机构发布的中文 GEO 白皮书 |
| [《生成式人工智能应用发展报告（2026）》](https://www.21jingji.com/article/20260929/herald/b55c0ac8c4012cc9f5320c6bf5156b67.html) | CNNIC 2026/09 | 截至 2026 年上半年生成式 AI 用户规模突破 7 亿、普及率超 50%；76.0% 用户用于智能问答 |
| [第 57 次《中国互联网络发展状况统计报告》](https://www.news.cn/tech/20260302/66c4ab06b6f34f8d806b416b3acc9f0b/c.html) | CNNIC 2026 | 截至 2025-12 生成式 AI 用户规模 6.02 亿、普及率 42.8%（较 2024 年底增长 141.7%） |
| [QuestMobile 2026 年 AI 应用市场发展半年报](https://www.questmobile.com.cn/research/report/2076954943839809537/) | QuestMobile 2026/07 | 2026-06 AI 原生 App 月活 4.99 亿（同比 +85.4%）；豆包 / 千问 / DeepSeek 月活 3.82 / 1.67 / 1.29 亿 |
| [QuestMobile 2026 年一季度 AI 应用洞察](https://www.questmobile.com.cn/research/report/2046482337382842370/) | QuestMobile 2026/04 | AI 原生 App 月活 4.46 亿；豆包 / 千问 / DeepSeek 月活 3.45 / 1.66 / 1.27 亿，活跃率 33.5% / 17.1% / 21% |
| [新榜智汇 AI 引用数据分析](https://www.newrank.cn/report/detail/433) | 新榜研究院 2026/03 | 1683.6 万联网信源拆解：元宝引用源约 10% 为微信公众号，豆包 TOP5 信源 3 个来自字节系 |
| [QuestMobile AI 平台采信逻辑与信源偏好研究](https://news.qq.com/rain/a/20260526A03HGO00) | QuestMobile 2026/05 | 按行业拆解豆包 / 千问 / DeepSeek 信源结构（旅游"目的地发现类"携程引用率 58.3% 居首） |
| [QuestMobile 2026 上半年 AI 旅游应用趋势洞察](https://news.ifeng.com/c/8sswh42rgQI) | QuestMobile 2026/05 | 携程在旅游问答整体引用率豆包 82.6% / 千问 75.9% / DeepSeek 64%；66.2% 用户仍回传统 App 二次核实 |
| [SuperCLUE 中文大模型基准测评](https://www.superclueai.com/) | SuperCLUE | 中文通用大模型综合基准，按月发布榜单 + 年度报告（区别于 SuperCLUE-AISearch 搜索专项） |
| [消费决策场景 AI 搜索洞察——2026 年重点行业 GEO 差异化策略研究报告](https://report.iresearch.cn/report/202608/4849.shtml) | 艾瑞咨询 2026/08 | 消费决策中的 AI 搜索行为，B2C / B2B 细分行业 GEO 策略与案例 |

### 英文评测与研究报告

| 资源 | 机构 | 核心发现 |
|------|------|---------|
| [AI Search Visits Surging in 2025](https://videos.brightedge.com/assets/blog/ai-search-visits-in-surging-2025/Industry%20Report%20Sep%202025.pdf) | BrightEdge 2025/09 | Fortune 100 品牌实测：AI 搜索双位数月增长，但目前 <1% 总流量占比 |
| [AI Overviews One Year Review](https://videos.brightedge.com/assets/SGE-Guide/BrightEdge%20Report%20-%20AIO%20Overviews%20One%20Year%20Review%20Research%20Paper%20and%20Deep%20Dive%20.pdf) | BrightEdge 2025/05 | Google AI Overviews 上线一年：搜索量 +49%，CTR -30% |
| [Platform Citation Preferences](https://www.hashmeta.ai/en/geo/research/platform-citation-preferences) | Hashmeta 2025/01 | 6 大 AI 平台 / 15,000+ 引用 / 3,400+ 查询的跨平台引用偏好分析 |
| [LLM Citation Study by Industry](https://blog-v2.writesonic.com/llm-ai-search-industry-citation-study) | Writesonic 2025/11 | 不同行业的 LLM 引用模式差异；GPT 不同版本间引用重叠率仅 7% |
| [Top Brand Visibility Factors（75K 品牌）](https://ahrefs.com/blog/ai-brand-visibility-correlations/) | Ahrefs 2025/12 | 跨 ChatGPT / AI Mode / AI Overviews：YouTube 提及相关性最高（≈0.737），站点页面数量几乎无相关性（≈0.194） |
| [38% of AI Overview Citations Pull From The Top 10](https://ahrefs.com/blog/ai-overview-citations-top-10/) | Ahrefs 2026/03 | 全量引用 URL 中位于自然结果前 10 的占比从约 76%（2025/07）降至 37.9%；约 31% 来自 100 名之外 |
| [AI Platform Citation Patterns（6.8 亿引用）](https://www.tryprofound.com/blog/ai-platform-citation-patterns) | Profound 2025/06 | Wikipedia 占 ChatGPT 全部引用 7.8%（前 10 来源中 47.9%）；Reddit 占 Perplexity 前 10 来源 46.7% |
| [AIO Impact on Google CTR: 2026 Update](https://www.seerinteractive.com/insights/aio-impact-on-google-ctr-2026-update) | Seer Interactive 2026/04 | 53 品牌 / 547 万 query：AIO query 自然 CTR 自 2025/12 低点 1.3% 回升至 2026/02 的 2.4%；被引用页多 +120% 自然点击 |
| [89K LinkedIn URLs Cited in AI Search](https://www.semrush.com/blog/linkedin-ai-visibility-study/) | Semrush 2026/03 | LinkedIn 平均在 11% 的 AI 回答中被引用；被引文章集中在 500–2000 词，约 95% 为原创 |
| [AI Search Has a Citation Problem](https://www.cjr.org/tow_center/we-compared-eight-ai-search-engines-theyre-all-bad-at-citing-news.php) | 哥伦比亚大学 Tow Center 2025/03 | 8 款 AI 搜索（含 DeepSeek Search）1600 次引用测试：整体错误率超 60%，Perplexity 最低 37%、Grok-3 最高 94% |
| [Top Domains Cited by AI Search（3000 万来源）](https://peec.ai/blog/top-domains-cited-by-ai-search-analysis-based-on-30m-sources) | Peec AI 2026/03 | 五平台域名引用偏好：整体 Top 为 Reddit / YouTube / LinkedIn / Wikipedia / Forbes |
| [The Top 100 Gen AI Consumer Apps（6th）](https://a16z.com/100-gen-ai-apps-6/) | a16z 2026/03 | 网页端 ChatGPT 流量为第二名 Gemini 的 2.7 倍，移动端 MAU 2.5 倍；ChatGPT 周活达 9 亿 |
| [AI Traffic Grows but Retail Sites Lag in AI Search Visibility（2026 Q1）](https://business.adobe.com/blog/ai-traffic-surge-retail-sites-not-machine-readable) | Adobe Analytics 2026/04 | 2026 Q1 美国零售站点 AI 来源流量同比 +393%；2026/03 AI 流量转化率较非 AI 高 42% |
| [How Query Language Reshapes AI Citations](https://www.tryprofound.com/blog/how-query-language-reshapes-ai-citations) | Profound 2026 | 32.5 亿条 AI 引用、7 个模型、14 个国家：按查询语言对比信源类型分布差异 |
| [Social Media AI Citations Study 2026](https://higoodie.com/blog/social-media-ai-citations-study-2026/) | Goodie 2026/09 | 2026 年 1–8 月社交媒体在 AI 搜索引用中的占比由 4.9% 升至 7.2% |
| [Q3 2026 AI Citation Trends Report](https://tinuiti.com/research-insights/research/ai-citation-trends-report/) | Tinuiti 2026 | 季度 AI 引用趋势报告 |
| [2026 Generative AI Landscape Report](https://www.similarweb.com/corp/reports/2026-generative-ai-landscape/) | Similarweb 2026 | 生成式 AI 平台流量、引荐与市场格局年度报告 |

---

## 中文研究与索引项目

| 项目 | 说明 |
|------|------|
| [LLM-X-Factorer/cn-seo-geo-atlas](https://github.com/LLM-X-Factorer/cn-seo-geo-atlas) | 中文 SEO/GEO 技术调研图谱：14+1 张跨平台技术卡覆盖 8 维度，68 条可证伪元假说 |

---

## 英文资源（精选）

| 资源 | 说明 |
|------|------|
| [awesome-geo](https://github.com/luka2chat/awesome-geo) | 英文 GEO 资源列表 |
| [awesome-generative-engine-optimization](https://github.com/amplifying-ai/awesome-generative-engine-optimization) | 英文 GEO 资源指南 |
| [DavidHuji/Awesome-GEO](https://github.com/DavidHuji/Awesome-GEO) | 学术研究方向论文索引 |
| [Backlinko GEO Guide](https://backlinko.com/generative-engine-optimization-geo) | Backlinko 的 GEO 分步指南（2026-06 更新） |
| [Search Engine Land - What is GEO](https://searchengineland.com/what-is-geo-generative-engine-optimization) | 定义和概述 |
| [Mastering GEO in 2026 (Search Engine Land)](https://searchengineland.com/mastering-generative-engine-optimization-in-2026-full-guide-469142) | 完整的 GEO 实操指南（2026 版） |
| [Kevin Indig - Growth Memo](https://www.growth-memo.com/) | 数据驱动的 GEO / AI 搜索研究博客（22k+ 订阅，曾分析 1.2M ChatGPT 回答） |
| [Webflow - How AI is reshaping search](https://webflow.com/blog/ai-reshaping-search) | AEO 与 AI 搜索的基础介绍 |
| [Can You Fake Expertise in AI Search? (Authoritas)](https://www.authoritas.com/blog/can-you-fake-it-til-you-make-it-in-the-age-of-ai-search) | 测试 9 个 AI 模型的专家引用偏好研究 |
| [The AI Search Manual (iPullRank)](https://ipullrank.com/ai-search-manual) | Michael King 团队的免费在线 AI 搜索方法论手册（24 章 + 附录：术语表 / 工具目录 / prompt 配方 / 测量模板） |
| [Learn AI Search (Aleyda Solis)](https://learningaisearch.com/) | 免费 AI 搜索优化学习路线图，覆盖 GEO/AEO/LLMO 基础、KPI 测量、电商专项、工具清单 + 优化 checklist |
| [How China's fragmented search ecosystem is reshaping SEO in 2026](https://searchengineland.com/china-fragmented-search-ecosystem-seo-476465) | Search Engine Land：面向英文读者梳理中国分裂式搜索 / AI 生态与各厂商信源绑定关系 |

---

## 贡献指南

欢迎提交 PR 添加中文 GEO 相关资源。请确保：

1. 资源与中文 GEO 生态相关（中国 AI 搜索引擎、中文内容平台、中文创作者）
2. 提供简要说明
3. 优先收录有数据支撑或实操价值的内容

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
