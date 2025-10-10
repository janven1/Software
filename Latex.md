---
date_create: 2025-05-27
type: Software
source: document
---
# 前言：Latex介绍
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=3&selection=9,0,10,4&color=yellow|📖]])**Latex是什么**？
> Latex是一个**排版工具**，方便对文章排版，作者只需要做内容产出，其具有非常强大的插入数字公式和图片的工程
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=3&selection=20,0,21,4&color=yellow|📖]])**Latex怎么用**？
> 有**线上Latex编辑环境**，比如**Overleaf**。也可以在电脑上安装环境，推荐Vscode+Texlive
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=3&selection=34,0,35,4&color=yellow|📖]])**Latex好用吗**？
> 易：**使用Latex排版一个标准格式的论文**是很简单的，20分钟足够速通 
> 难：**想开发一个自己设计的Latex模板文件还是相对比较困难的**，不过一般也不需要
# Latex快速入门 
### 认识Latex模板
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=6&selection=13,1,15,6&color=yellow|📖]])**Latex模板是什么**？
> Latex模板规定了一篇文章的<font color="#ff0000">所有格式</font>
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=6&selection=24,0,26,8&color=yellow|📖]])**拿到Latex模板后要干什么**？
> 修改标题，作者，撰写正文，插入公式、图表，添加引用等
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=6&selection=34,0,35,8&color=yellow|📖]])**Latex排版有什么好处**？
> 各种数模竞赛轻松排版，<font color="#ff0000">省时美观 </font>
> 科研论文<font color="#ff0000">标准撰写</font>，拒绝因格式返稿
#### 模板里有些什么？
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=7&selection=16,0,16,2&color=yellow|📖]])**注释**
> Latex文件<font color="#ff0000">注释</font>使用“%”，在一行中“%”号后面的内容均会被注释掉，生成PDF文件时不会显示
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=7&selection=20,0,20,7&color=yellow|📖]])**命令或特殊符号**
> “\”符号出现，表示这是一个<font color="#ff0000">命令</font>或者<font color="#ff0000">特殊符号</font>
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=7&selection=34,1,35,4&color=yellow|📖]])**普通文本**
> 标题、摘要、正文、图表标题等都是<font color="#ff0000">普通文本</font>
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=8&selection=14,0,15,29&color=yellow|📖]])**Latex中的特殊符号（因为有特殊含义，所以不能直接当成文本打出来）**
> “%”——在LaTeX中，百分号是作为注释符号 
> “&”——在LaTeX用于表格或数学公式中的位置对齐符号 
> “$”——这个符号被用作数学公式标记符：被框在两个该符号中间的内容将会翻译为数学公式 
> “~”——保留强制空格，非常古老的用法 
> “^”和“\_”——上三角和下划线用作上下标标记 
> “{”和“}” ——左右花括号表示将其中的内容作为一个整体对待 
> “#”——编写宏包时使用
### 正文
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=10&selection=12,0,12,9&color=yellow|📖]])**设定区域和正文区域**
> • 设定区域 
>  \documentclass{…}、\usepackage{…}为设定区域，规定论文格式，导入相关依赖包等 
>  一般不会对生产的PDF产生影响 
>  设定区域会随着我们不断添加新的元素而丰富 
>  Latex常用宏包
>  • 正文区域 
>   \begin…\end 命令中建的这个区域 
>   所有在最终PDF文件的可见内容均在此区域添加，包括文字，图表，公式 
>   在正文区域，我们需要先输入一篇论文的基本内容，设定论文题目，摘要，关键字等
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=11&selection=12,0,12,6&color=yellow|📖]])**正文各级标题**
> • chapter——章，一般只用于可以成书的文章 
> • section——节 
> • subsection——小节 
> • subsubsection——小小节 
> • 也就是对应着我们的多级标题
### 数学公式
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=13&selection=12,0,13,5&color=yellow|📖]])**Latex的数学公式**
> • Tex（LaTeX）火遍大江南北便是由于其杰出的数学公式排版功能 
> • 没有更好用，只有最好用
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=13&selection=28,0,28,6&color=yellow|📖]])**数学公式分类**
> • 正文行中特殊字符及短公式 
> • 单行、多行公式带编号 
> • 单行、多行公式不带编号 
> • 分情况讨论公式
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=14&selection=12,0,12,7&color=yellow|📖]])**单行公式带编号**
> • \begin｛equation｝\label｛公式标签｝ 
> …… 
> \end{equation} 
> • 自动引用\autoref{公式标签}（需要导入依赖包\usepackage{hyperref}）
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=14&selection=39,0,39,13&color=yellow|📖]])**正文行中的特殊字符和短公式**
> • 使用两个\$符号：\$公式\$
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=14&selection=52,0,52,5&color=yellow|📖]])**无编号公式**
> • \\[ 公式 \\]
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=15&selection=32,0,32,4&color=yellow|📖]])**多行公式**
> • 使用\begin{split}…\end{split} （需要导入依赖包\usepackage{amsmath}，有的环境可能自带）
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=15&selection=12,0,12,5&color=yellow|📖]])**分情况讨论**
> • 属于多行公式一种，使用\begin{cases}…\end{cases} （需要导入依赖包\usepackage{amsmath}， 有的环境可能自带） 
> • 需要用正文样式输出的地方用\text｛｝
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=16&selection=12,0,13,6&color=yellow|📖]])**公式生成神器Axmath**
> • 支持公式和Latex双向转换，且公式输入方便快捷
### 图片
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=18&selection=11,1,12,4&color=yellow|📖]])**插入图片**
> • 依赖包graphicx（有的环境可能自带） 
> • 常用模板 
```
\begin{figure}[htbp] 
	\centering 
	\includegraphics[图片大小][图片路径] 
	\centering{图片标题、说明} 
	\centering{图片标签} 
\end{figure}
```
 > • \[图片大小] 
 > 图片大小使用height和width规定，单位可以采用cm或in（inch），如果止规顶高或宽其中一个，图片将保持高宽比插入，所以一般只需要规定图片宽度。 
 > • \[图片路径] 
 > 图片相对于tex文件的路径
 > • htbp 是 LaTeX 中用于控制浮动体位置的一个选项集。浮动体（如图表或表格）通常不会被直接放置在代码所在的位置，而是由 LaTeX 根据排版需要放置在页面的其他位置。htbp 用于指定浮动体的偏好位置。这些选项的含义如下： 
 >    h（here）: 尽量将浮动体放置在代码所在的位置。然而，如果页面的顶部或底部能够更好地容纳浮动体，LaTeX可能会选择这样做。 
 >    t（top）: 将浮动体放置在页面的顶部。 
 >    b（bottom）: 将浮动体放置在页面的底部。 
 >    p（page）: 将浮动体放置在一个单独的页面上。 
 >    这些选项可以组合使用，例如 ht 表示首选放置在页面顶部，但如果不行就放置在代码所在的位置。默认情况下，如果你不提供任何选项，LaTeX 会使用 tbp 作为默认值。 
 >    例如，\begin{figure}\[htbp] 表示在尽量放在当前位置，如果不行就放在页面顶部，底部，或者单独一页。
### 表格
```
\documentclass{article}
\usepackage{array} % 确保表格功能正常
\begin{document}
\begin{table}[htb]
\centering
\caption{Beecy.}
\label{table:1}
\begin{tabular}{|c|c|c|}
\hline
\textbf{Algorithms} & \textbf{Complexity} & \textbf{Overhead} \\
\hline
algorithm 1 & high & low \\
\hline
algorithm 2 & high & low \\
\hline
algorithm 3 & low & low \\
\hline
\end{tabular}
\end{table}
\end{document}
```
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=22&selection=12,0,12,2&color=yellow|📖]])**表格**
> • \begin{table}\[htb] 表示Table的参数
> • |c|是来约定表格的每列属性的
> • 其他命令
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=23&selection=12,0,12,2&color=yellow|📖]])**表格**
> • 目前有很多Latex表格在线生成工具，可视化制作表格，生成LaTex代码 
> • 常用网站：
> 	https://www.latex-tables.com/
> 	[Create LaTeX tables online – TablesGenerator.com](https://www.tablesgenerator.com/)
### 引用文献
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=25&selection=12,0,12,4&color=yellow|📖]])**参考文献-1**
> • 添加参考文献的方法很多，最简单的方法就是直接在LaTex文件里直接引用 
> • 文中引用格式 \cite{lable1}， \cite{lable2} …%这里lable1， lable2可随意替换，和文末标签对应即可文末参考文献格式：
```
\begin{thebibliography}{99}%99表示引用上限 
\bibitem{lable1} Anita G ,V. B V ,John P .Hybrid model with optimal features for non-invasive blood glucose monitoring from breath biomarkers[J].Biomedical Signal Processing and Control,2024,88(PC): 
\bibitem{lable2}Zhining C ,Jianzhou W ,Li Y , et al.A hybrid electricity load prediction system based onweighted fuzzy time series and multi-objective differential evolution[J].Applied Soft Computing,2023,149(PB): 
\end{thebibliography}
```
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=26&selection=12,0,12,4&color=yellow|📖]])**参考文献-2**
> • 如果一次引用文献很多，可以使用BiBTex来管理文献，设定区域添加\bibliographystyle{unsrt} 
> • 首先通过谷歌学术搜索文献，找到BiB格式的文献引用条目，然后添加至bib文件中
```
@article{yu2019review, 
title={A review of recurrent neural networks: LSTM cells and network architectures}, 
author={Yu, Yong and Si, Xiaosheng and Hu, Changhua and Zhang, Jianxun}, 
journal={Neural computation}, 
volume={31}, 
number={7}, 
pages={1235--1270}, 
year={2019}, 
publisher={MIT Press One Rogers Street, Cambridge, MA 02142-1209, USA journals-info~…} }
```
> • 文中需要插入文献的地方用\cite{yu2019review}进行引用，文末参考文献位置加\bibliography{bib文件名}
> ([[30分钟速成Latex【数模加油站出品】.pdf#page=27&selection=12,0,12,4&color=yellow|📖]])**参考文献-3**
> • 右上角引用 
> 	如果想要右上角引用需要首先在设定区域添加\newcommand{\upcite}\[1]{\textsuperscript{\cite{#1}}} 
> 	然后文中引用\cite{}改为\upcite{}

















