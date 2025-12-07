---
date_create: 2025-12-07-星期日
type: Software
software:
status: unstarted
source: weixin
---
[link::[满血版 Zotero + Research Rabbit：打造 2025 最强科研文献工作流](https://mp.weixin.qq.com/s/2N-Qix-AdHN0WgoI_5-rpA)]


**培养良好的文献发掘与整理习惯，是成为一名优秀科研工作者必不可少的基础素养。**在学术研究中，文献管理的效率直接影响着科研产出的质量与速度。然而掣肘文献管理效率的原因，**往往始于检索端的迷茫，终于管理端的混乱**。许多研究者常面临工具割裂的困境：在数据库检索文献，在本地文件夹存储 PDF，再使用独立的软件进行引用，各个环节缺乏联动。

为了解决这一问题，我们需要构建一个从“检索”到“管理”再到“引用”的完整闭环。本文将详细介绍一套高效的文献工作流方案，**即利用 Research Rabbit 进行可视化的文献溯源与挖掘，结合安装了 12 款增强插件的“满血版” Zotero 进行深度管理与阅读。**借助这套整合方案，研究者能够提升文献获取与知识管理的能力，从而构建起更加高效率的科研作业流程。

  

**01**

**强大的文献检索工具 Research Rabbit**

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEDUKHxW1B0Z4LYGIjLEBRicib10ZsvQ6Ig0MgrVlk8yyqoWe7WLRvI5Tg/640?wx_fmt=png&from=appmsg&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=0)

图一：Research Rabbit

https://app.researchrabbit.ai/

  

在将文献导入 Zotero 进行精细化管理之前，首要任务是高效地发现高质量文献。Research Rabbit 是一款基于引文网络的在线文献分析工具，是该工作流中负责“文献检索”的核心环节。

**Research Rabbit 的核心价值在于将线性的文献列表转化为可视化的引文网络图谱。**传统的关键词检索往往只能提供离散的搜索结果，而 Research Rabbit 允许用户导入一篇或多篇核心文献作为种子（seed paper），这些文章也可以通过zotero导入，系统会自动生成以这些文献为中心的网状关系图。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEekE673hicHZJxLXaVooJZd82oZTS7KG7UFe1fpVhn8raguobibu5E6Qg/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=1)

图二：引文网络图谱

  

坐标系的Y轴为引用量，X轴则为发表时间。**这就意味着坐标系左上角的文献往往都是高引用的领域开山之作，而左下角则是最新的领域进展。**连线则直观地展示了文献间的引用关系，这种视图模式能帮助研究者迅速识别出该领域的奠基性工作以及最新的研究热点，理清学术脉络的演进过程。

**除了可视化展示，该工具还具备强大的 AI 智能溯源与推荐功能**。它支持双向检索，既可以向前追溯当前研究引用的理论基础（点击图三左下角Refs选项），也可以向后挖掘引用了该研究的最新成果（点击图三左下角Cited by选项）。同时，系统会根据用户的文献集合特征，利用算法自动推荐高相关度但尚未被用户发现的论文（点击图三左下角Similar选项），有效弥补了关键词搜索的盲区。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGE3icpvqd744xcrwdzIb06v58zotYRr4Ll72bBck7Q9j5U4nRr9zTzHOA/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=2)

图三：选中文章进行深度挖掘

  

找到心仪的文章后可以点击右上角的Save to选项保存在自己设定的标签夹中。**最关键的是，Research Rabbit 提供了与 Zotero 的交互功能。**用户授权后，它可以直接读取 Zotero 的收藏夹生成分析图谱。而在图谱中新发现的有价值文献，也可以通过Research rabbit生成的BibTex文件导入Zotero 客户端，从而实现了从文献检索到管理的无缝衔接。

  

**02**

**利用开源生态满血进化 Zotero** 

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEX5u5md5dSibBM68KE4sbia9M1yiaAicbNORN1L4ibhe59uFezqku9wUWXSA/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=3)

图四：Zotero

https://www.zotero.org/

  

Research Rabbit 解决了文献发现与溯源的问题，而文献的存储、管理与引用则需要一个稳定且强大的本地终端来承接，Zotero 无疑是目前最优的选择。作为一个开源免费的文献管理软件，**Zotero 区别于传统商业软件的核心优势，在于其卓越的网页抓取能力和高度开放的插件生态系统。**

**Zotero 的首要竞争力体现在其数据收集的高效性上。通过浏览器扩展 Zotero Connector**，无论是 Web of Science、IEEE Xplore、PubMed 等外文数据库，还是知网、万方等中文平台，Zotero 都能一键抓取规范的题录元数据，并自动下载关联的 PDF 全文或网页快照。这种自动化的收集方式极大地降低了人工录入的成本，保证了数据库的标准化。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGErAw5ibn7gEtpFq98apvuIlMfgkdp6EHtwicBAbIL2ibKibaqxSUg9tlZsA/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=4)

图五：Zotero Connector

  

在与 EndNote 或 Mendeley 等同类工具的横向对比中，Zotero 的开源特性赋予了它极强的生命力。EndNote 虽然功能成熟但价格昂贵且开发封闭，Mendeley 虽然界面现代但对本地数据加密限制了二次开发。相比之下，**Zotero 免费开源、跨平台兼容，不仅确保了用户对数据的完全掌控，更允许第三方开发者通过插件深度扩展软件功能。**

正是这种可扩展性，使得 Zotero 能够突破原生功能的局限。原生 Zotero 已经是一个合格的文献存储库，配合特定的 .xpi 插件后，它能进化为集 AI 分析、深度阅读、知识管理于一体的综合科研平台。接下来的内容中，**我们将详细解析 11 款经过筛选的实用插件，展示如何通过模块化的配置，解决原生 Zotero 在元数据清洗、笔记管理及 LaTeX 协作等方面的短板，构建一套高效的现代化科研工作流。**

  

1

**元数据清洗与附件管理**

文献管理的质量直接决定了后期写作引用的效率。如果在收集文献阶段，元数据存在标题大小写混乱、期刊缩写不统一或附件命名无序等问题，最后生成参考文献时就会错误百出。以下三个插件分别从元数据格式化、查重和附件管理三个维度解决这些基础问题。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEWwic1K5U8I3WKPesicgibLK5OPFkKXIjC3esyBR4v5bryQv4d0pRkibOzg/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=5)

图六：Linter for Zotero

  

**1. Linter for Zotero：元数据格式化工具**

我们在抓取文献时，经常遇到标题全大写、首字母大小写不规范，或者缺省期刊缩写、大学地点格式不统一的情况。Linter for Zotero 是一个专门用于标准化这些信息的工具。**它的核心功能是规范文献条目的各项属性。它能够一键调整标题的富文本格式**（例如将标题统一转换为句首字母大写 Sentence Case 或标题首字母大写 Title Case）。

**使用方法：** 插件安装后，在 Zotero 主界面选中需要处理的文献条目（支持批量选择），点击鼠标右键，在菜单中找到 Linter 选项。根据需要选择具体的格式化指令，例如修改标题大小写或标准化期刊缩写，插件即会瞬间完成修改。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEHqnt4FXkDCTOfXGIptiaZoTPUtPMiaSL77OON4ibszibO3ZymTZlcKby0Q/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=6)

图七：Zoplicate

  

**2. Zoplicate：专注于重复条目管理**

随着文献库规模的扩大，重复抓取文献是高频发生的现象。虽然 Zotero 原生具备查重功能，但 Zoplicate 将这一功能进行了独立强化。正如其介绍所言，**该插件只做一件事：检测并管理重复项**。相比原生功能，它提供了更细致的查重逻辑和管理界面，能够帮助用户更精准地识别库中的冗余条目，保持数据库的清洁。

**使用方法：** 该插件集成在 Zotero 的工具流中。在进行文献整理时，Zoplicate 会辅助识别疑似重复的条目。用户可以通过它提供的界面对比重复项的详细信息（如添加时间、笔记数量等），从而决定保留哪一个版本，或者将多个条目的信息进行合并，操作逻辑比原生界面更加直观。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGE7Lyoibltk3ibH7aKhqQPQBdrXSXibJjhgaRg536ZCdJNsl7sStD9OaFrg/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=7)

图八：Zotero Attanger

  

**3. Zotero Attanger：附件重命名与路径管理**

Zotero 默认的附件存储方式是将 PDF 放在深层级的随机文件夹中，且文件名往往缺乏语义。对于习惯使用链接附件（Linked Attachment）或者希望附件文件在硬盘上也井井有条的用户，Zotero Attanger 是一个非常实用的附件管理器。**它的主要功能是根据元数据自动重命名 PDF 文件，并将其移动到用户指定的目录中（如Onedrive等个人网盘路径）。**

**使用方法：** 首先在插件首选项中设置好附件存储的根目录（Base Folder）以及期望的文件命名格式。设置完成后，在主界面选中含有附件的条目，右键点击选择 Attanger 菜单下的 Rename and Move 选项。插件会自动依据条目信息重命名 PDF 文件，将其移动到目标文件夹，并更新 Zotero 中的链接索引，确保在软件内依然能正常打开阅读。**在设置选择中请取消勾选“自动移动添加的附件”，避免使用其它插件出现问题。**

  

2

**大模型辅助阅读与分析**

在 AI 介入科研流程的今天，能够直接在 Zotero 内部与大模型对话、生成摘要和提炼观点，已经成为提升阅读效率的关键。本部分介绍两款主流的 AI 插件，它们都致力于将 GPT 类模型的能力引入文献管理，但在设计理念和功能侧重上各有千秋。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGE3jYoE3wdM2ooibdzj503JhXiallicsW3p04y1vNjTEFsv1JQUwqMR1WuA/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=8)

图八：PapersGPT for Zotero

  

**4. PapersGPT for Zotero：更加轻量化**

PapersGPT 是一款扁平化设计的 AI 插件，其最大的亮点**在于对 MCP（Model Context Protocol，模型上下文协议） 的支持以及极广的模型兼容性**。它不局限于 OpenAI 的 ChatGPT，而是打通了几乎所有主流的 AI 服务商。根据项目描述，它支持包括 Gemini 3、Claude、Grok，以及国内备受关注的 DeepSeek、Kimi等模型。

**使用方法：** 安装插件后，用户需要在设置面板中配置对应服务商的 API Key。在阅读文献时，可以通过侧边栏唤起对话窗口，对选中的论文进行提问，或者要求 AI 解释特定的段落。由于支持多种模型，用户可以根据任务难度灵活切换，例如用 Claude 分析单篇文章，用性价比高的 DeepSeek 处理多篇文献回顾。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEwNaA4KBs871UfWsdGf1SrXy0zhkVqjKEcr07VyPQQbZaUYAjc1mHLw/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=9)

图九：PapersGPT for Zotero Summary功能示意

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGE4JLGCoLJiaMzrdY8kYU6aRORPw7ZNvVz4kjVicohBzaSU7a1CkOSEyag/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=10)

图十：Zotero GPT

  

**5. Zotero GPT：经典的交互体验**

Zotero GPT 出自 Zotero 社区高产开发者 MuiseDestiny 之手（也是下文将提到的 Zotero Style 等插件的作者）。这款插件的设计理念更偏向于“原生融合”，旨在让 GPT 的能力无缝融入 Zotero 的界面中。**它提供了稳定的文档问答功能，允许使用内置prompt模板，比如快速生成“文献综述”或“研究方法总结”。**

**使用方法：** 插件安装后，阅读界面左上会增加一个 AI 图标。用户可以选中文本后通过快捷指令发送给 AI 进行翻译或润色，也可以让 AI 读取全文进行总结。它支持将 AI 的回答直接保存为 Zotero 的笔记，方便后续整理引用。

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEr0v0tQUDvhdp0O0AzHTBDI9KuMicpHWf1oibSNUBWvibibcJ3ycVb3icFfQ/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=11)

图十一：Zotero GPT Literature Review功能示意

  

3

**翻译、预览与知识库构建**

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEomPOPwNTpMicV0icicmqWloiarudXdcMzRqUxOMUGFfCagkcWkt1d4HIeA/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=12)

图十二：Zotero PDF2zh 双语翻译效果

  

**6. Zotero PDF2zh：沉浸双语翻译**

阅读英文文献时，频繁在 PDF 阅读器和翻译软件之间切换会严重打断思路。Zotero PDF2zh 是一款专为 Zotero 打造的 PDF 翻译工具，**旨在实现“沉浸式”的中文阅读体验。它的特色在于保留原文的PDF格式，支持使用多种模型api进行翻译，还支持“双语对照”模式。**

**使用方法：** 配置方法请参考原项目指导，笔者推荐使用deepseek api进行翻译，翻译质量优秀且成本低廉。如果读者觉得配置过程过于麻烦，可以使用下位替代**Translate for Zotero**插件进行翻译。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEia2d4MZuZpLlxdzehA72dibicdyzib9ySvAANLjINye1NT3ytbghaH96Wg/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=13)

图十三：Zotero Reference功能示意

  

**7. Zotero Reference：参考文献预览插件**

在阅读学术论文时，我们经常会看到形如“[1]”或“(Smith, 2020)”的引用标记。为了弄清楚这篇引文具体是什么，通常需要翻到论文末尾的参考文献列表查看，不仅麻烦，还容易导致阅读中断，忘记刚才读到的上下文。Zotero Reference 完美解决了这个痛点。**它能够智能识别正文中的引用标记，并将其与 Zotero 库中的条目或 PDF 末尾的参考文献列表进行关联。**

**使用方法：** 该插件主要在 Zotero 的内置 PDF 阅读器中发挥作用。安装后，当你在阅读时遇到文中出现的引用符号，只需将鼠标悬停在上面（或点击），插件就会自动弹出一个小窗口，显示该篇参考文献的标题、作者、年份等详细信息。如果你的数据库里恰好也有这篇被引用的论文，你甚至可以直接点击跳转去阅读那篇文献，真正实现了文献之间的知识互联。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEjLiaAbUSAud32ZraZibKe1dEvhzN2oqOK7luzoI3u9NKHy6tVwiaM12Ow/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=14)

图十四：Zotero Better Notes功能示意

  

**8. Zotero Better Notes：全能笔记管理系统**

Zotero 原生的笔记功能相对基础，难以应对复杂的综述写作或知识库构建需求。Zotero Better Notes 则试图将 Zotero 打造成类似 Obsidian 或 Notion 的“第二大脑”。**它极大地增强了笔记编辑器的功能，支持Markdown语法、双向链接、笔记模板以及思维导图（大纲）模式。**通过它，用户可以将分散在不同论文中的观点汇聚到一个“主笔记”中，构建起自己的知识网络。

**使用方法**： 这是一个功能极深厚的插件。基础用法是创建带有模板的笔记，例如“康奈尔笔记法”模板。进阶用法是利用它的“双向链接”功能：在写笔记时输入特定快捷键（如 [[），快速引用库中的其他文献或笔记。此外，它还支持从 PDF 高亮中自动提取内容填充到笔记模板中，甚至可以将你的笔记库自动同步导出为 Markdown 文件，方便在其他笔记软件中复用。

  

4

**界面个性化与文献库可视化**

![图片](https://mmbiz.qpic.cn/sz_mmbiz_gif/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEF1DQ7LicDjIGjjYQaDTibCZiaiaRiciaCFeN1CsoLm77FOGvliaqRf4KpKicVA/640?wx_fmt=gif&from=appmsg&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=15)

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEdgvGwLdPCFiaicUxls5as0cph8cmAo6KMQnttnarrFozrCzrR4ianZJlQ/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=16)

图十五：Zotero Style功能示意

  

**9. Zotero Style：界面个性化**

Zotero Style 是目前最受欢迎的界面美化插件。它不仅仅是换个“皮肤”，更提供了高度自定义的视图功能。并完美支持夜间模式，减轻长时间工作的眼部负担。更重要的是，它增强了列表视图的功能，允许用户将标签（Tags）直接显示在条目列表中，甚至可以通过颜色区分不同类型的文献（如将“待读”标红，“已读”标绿），让文献状态一目了然。

**使用方法：** 安装后，用户可以在插件设置中选择预设的主题风格。对于进阶用户，它支持通过 CSS 代码微调界面元素。最实用的功能是在“视图”菜单中开启标签列显示，这样你无需点击条目，就能在主界面的列表中直接看到每篇文章的分类标签和阅读进度标记。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEhS19HaoEtVsRj0V2wkVeATic9Uan3To12rsicu06x7HzmHEPF2N3W7Ig/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=17)

图十六：Chartero功能示意

**10. Chartero：文献库数据的全景可视化面板**

Zotero 原生的列表视图虽然清晰，但难以直观呈现文献库背后隐含的结构化信息。Chartero 不仅仅是一个阅读进度追踪器，它更是一个强大的文献库可视化分析工具。正如你在配图中看到的，**它能够基于 Zotero 的元数据自动生成复杂的图表，例如通过桑基图展示第一作者、通讯作者与发表期刊之间的流向关系，帮助研究者快速识别核心学术圈子与高频投稿期刊。**此外，它还支持生成标题词云以发现研究热点，以及生成引文关系图。通过这些可视化视图，用户可以从宏观视角俯瞰整个文献库的知识图谱，发现数据之间潜在的关联。

**使用方法：** 插件安装后，Zotero 主界面上方会增加一个新的可视化入口。用户可以根据分析需求切换不同的视图标签（如“作者关系图”、“引文关系图”或“标题词云图”）。在桑基图模式下，支持自定义节点和连线的筛选条件，将繁杂的元数据转化为具备分析价值的学术图标，非常适合在做文献综述或汇报时展示研究领域的整体架构。

  

**11. Google Scholar Citation Count for Zotero：文献引用量自动抓取**

在筛选和评估文献时，引用次数往往是衡量一篇文章学术影响力和重要性的直观指标，但 Zotero 原生并不具备实时更新这一数据的能力。Google Scholar Citation Count for Zotero 填补了这一空白，**它的主要功能是从 Google Scholar 数据库中自动抓取文献的最新引用频率，并将其填充到 Zotero 条目中。**该插件能够帮助研究者快速识别出领域内的经典高被引论文，避免了需要手动去 Google Scholar 逐条查询的繁琐过程。

使用方法： 插件安装完成后，用户需要在首选项中进行简单的配置，以适配网络环境。在主界面中，用户可以选中一篇或多篇文献，点击右键菜单中的 Update Citation Counts 选项，插件即会在后台运行抓取任务。为了更直观地展示数据，用户可以在 Zotero 的列表表头右键，勾选新增的“Citation Count”列，这样文献列表即可按照引用次数进行排序，极大地提升了筛选高质量文献的效率。

  

5

**写作引用输出**

文献管理的最终目的之一是为了在写作中高效引用。特别是使用 Word还是LaTeX。Zotero 原生功能的灵活性有时难以满足特定的格式需求。

  

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEvkic65J9MagibKEMHBT2u3hTKIYNGOJ4kqDbE9J5qXoVpj8rXBMsLuCw/640?wx_fmt=png&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=18)

图十七：Zotero Better BibTeX

  

**12. Zotero Better BibTeX：LaTeX 用户的核心组件**

对于使用 LaTeX 进行学术写作的用户而言，Zotero Better BibTeX (BBT) 是保证引用管理稳定性的基石。Zotero 原生导出的 BibTeX 文件在引用键的生成上存在不确定性，且容易产生命名冲突。BBT 彻底解决了这一问题，它能够根据用户设定的规则（例如 [auth][year]）自动生成简洁、唯一且固定的 Citation Key，并确保即使修改了条目元数据，该键值也能保持锁定，防止论文中的引用失效。

**使用方法：** 该插件安装后会自动接管系统的引用键生成逻辑。除了生成 Key 之外，**它最强大的功能是支持“保持更新”。用户只需选定一个zotero文库中指定的子文件夹并导出bib文件，随后在该文件夹中添加或修改任何文献，BBT 都会在后台自动更新该 .bib 文件。**这意味着 LaTeX 写作环境中的参考文献库永远与 Zotero 保持实时同步，用户无需再进行手动导出操作，彻底实现了文献引用的自动化。

  

 **插件下载链接合集**

**1. Linter for Zotero**

https://github.com/northword/zotero-format-metadata

**2. Zoplicate** 

https://github.com/ChenglongMa/zoplicate

**3. Zotero Attanger** 

https://github.com/MuiseDestiny/zotero-attanger

**4. PapersGPT for Zotero** 

https://github.com/papersgpt/papersgpt-for-zotero5

**5. Zotero GPT** 

https://github.com/MuiseDestiny/zotero-gpt

**6. Zotero PDF2zh** 

https://github.com/guaguastandup/zotero-pdf2zh

**7. Zotero Reference** 

https://github.com/MuiseDestiny/zotero-reference

**8. Zotero Better Notes** 

https://github.com/windingwind/zotero-better-notes

**9. Zotero Style** 

https://github.com/MuiseDestiny/zotero-style

**10. Chartero** 

https://github.com/volatile-static/Chartero

**11. Google Scholar Citation Count for Zotero**

https://github.com/eschnett/zotero-citationcounts

**12. Zotero Better BibTeX** 

https://github.com/retorquere/zotero-better-bibtex

  

  

**Tips：**国内用户访问 GitHub 可能较慢，如遇下载失败，建议寻找国内镜像源（如 Gitee 或专门的 Zotero 插件搬运站）。下载时请认准 .xpi 格式的安装包。

大多插件需要调用api使用，笔者推荐如下

**deepseek api 获取地址：**

https://platform.deepseek.com/

**Qwen api 获取地址**：  

https://bailian.console.aliyun.com/

  

  

  

**结语**

  

  

通过 Research Rabbit 与深度定制化 Zotero 的结合，我们构建了一套覆盖科研全周期的文献工作流。Research Rabbit 利用可视化技术和 AI 算法解决了文献发现与脉络梳理的难题，而 Zotero 及其丰富的插件生态则在元数据清洗、辅助阅读、笔记管理以及参考文献输出等环节提供了专业支持。掌握这套工具链的意义，在于将研究者从繁琐的格式整理和机械性检索中解放出来，从而将更多精力投入到文献的深度阅读与有效思考中。

  

**作者介绍**

![图片](https://mmbiz.qpic.cn/sz_mmbiz_jpg/8a2n6DYT8Y6G8icNSHtc3y1pvvaMv2zGEJVicTQn7amibM21ibhBXpCcIgxQpZZt4Y2WwwwJrGvvdjLIiclnPhU0zTA/640?wx_fmt=jpeg&from=appmsg&watermark=1&tp=wxpic&wxfrom=5&wx_lazy=1#imgIndex=19)

**吴宜涵**

  吴宜涵，硕士研究生，本科毕业于上海科技大学电子信息工程专业，2023年加入上海科技大学电力电子与再生能源实验室。目前主要研究方向是超高升压比变换器和车顶光伏供电。
