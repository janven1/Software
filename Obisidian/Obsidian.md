---
date_create: 2025-10-08
type: Software
source: video
status: updating
---

|    序号     | 功能                                                                                                                                                  | 完成进度 |
| :-------: | --------------------------------------------------------------------------------------------------------------------------------------------------- | :--: |
|    0.1    | [Obsidian学习文档](https://coffeetea.top/zh/)                                                                                                           |      |
|    0.2    | [PKMer](https://pkmer.cn/index_old/)                                                                                                                |      |
| **1.1.1** | [说到用Obsidian打数学](https://www.bilibili.com/video/BV13baozkETT/?spm_id_from=333.337.search-card.all.click&vd_source=aef73766b941d8e52cb9a97d24ea42a2) |  ⏳   |
| **1.1.2** | [Latex Suite](https://zhuanlan.zhihu.com/p/1931395948728259558)                                                                                     |  ⏳   |
|   1.1.1   | [链接到具体的一句话](https://www.bilibili.com/video/BV1Hj411E7ra?t=316.9)                                                                                    |  ❌   |
|   1.1.2   | [嵌入笔记](https://www.bilibili.com/video/BV1Hj411E7ra?t=406.2)                                                                                         |  ❌   |
|   1.2.1   | [斜体](https://www.bilibili.com/video/BV1Hj411E7ra?t=671.5)                                                                                           |  ❌   |
|   1.2.2   | [删除线](https://www.bilibili.com/video/BV1Hj411E7ra?t=699.9)                                                                                          |  ❌   |
|   1.3.1   | [标注](https://www.bilibili.com/video/BV1Hj411E7ra?t=1078.3)                                                                                          |  ❌   |
|   1.3.2   | [标注折叠](https://www.bilibili.com/video/BV1Hj411E7ra?t=1227.6)                                                                                        |  ❌   |
|    1.4    | [注释](https://www.bilibili.com/video/BV1Hj411E7ra?t=1258.4)                                                                                          |  ❌   |
|    2.1    | [Templates](https://www.bilibili.com/video/BV1c64y1W7c2?t=52.0)                                                                                     |  ❌   |
|    3.1    | [Obsidian流程图](https://zhuanlan.zhihu.com/p/1936544558864398155)                                                                                     |  ⏳   |
|    3.2    | [Templater](https://www.bilibili.com/video/BV1c64y1W7c2?t=480.9)                                                                                    |      |
|  3.2.1.1  | [`tp.file`](https://www.bilibili.com/video/BV1c64y1W7c2?t=627.9)                                                                                    |  ✅   |
|  3.2.1.2  | [`tp.date`](https://www.bilibili.com/video/BV1c64y1W7c2?t=689.9)                                                                                    |  ✅   |
|  3.2.1.3  | [`tp.system`](https://www.bilibili.com/video/BV1c64y1W7c2?t=724.5)                                                                                  |  ✅   |
|  3.2.1.4  | [实际演示1-模板转笔记](https://www.bilibili.com/video/BV1c64y1W7c2?t=822)                                                                                    |  ✅   |
|  3.2.1.5  | [实际演示2-应用模板](https://www.bilibili.com/video/BV1c64y1W7c2?t=1068.4)                                                                                  |  ✅   |
|  3.2.1.6  | [实际演示3-文件夹指定模板](https://www.bilibili.com/video/BV1c64y1W7c2?t=1178.6)<br>                                                                           |  ✅   |
# 0. 相关链接
# 1. 基础语法
# 2. 核心插件
# 3. 第三方插件
## 2. Templater
使用模板可以让我们保持笔记格式的统一，同时也能提升我们的效率。本期视频我想和你聊聊如何使用核心插件templates和第三方插件templater来进行模板的相关操作。希望可以给到你帮助和启发。
### 0. 相关链接
| 序号  | 链接                                                         |
| :-: | ---------------------------------------------------------- |
|  1  | [Templater官方文档](https://silentvoid13.github.io/Templater/) |
### 1. 基础内容
#### 1. `tp.file`
```templater
<% tp.file.title %>
<% tp.file.creation_date() %>
<% tp.file.cursor()%>
```
创建文档的时候写入时候就生成
1. 获取文档标题
2. 获取文档创建时间
3. [指定光标位置](https://www.bilibili.com/video/BV1c64y1W7c2?t=1014.5)：指定文档光标位置，其中 `()` 内可以填写数字
#### 2. `tp.date`
```templater
<% tp.date.now("YYYY-MM-DD") %>
<% tp.date.tomorrow("YYYY-MM-DD") %>
<% tp.date.yesterday("YYYY-MM-DD") %>
```
#### 3. `tp.system`
```templater
<% tp.system.prompt("提示") %>
<% tp.system.suggester(["to-read", "reading", "done"],["to-read", "reading", "done"],true, '提示') %>
```
弹出一些框让你去选择，去输入 ；
- 第一行，输入根据 `提示` 填写内容；
- 第二行，选择的框：第一个列表表示的选择的内容，第二个列表表示实际添加到笔记的内容，参数 `true` 表示不选择任何内容的话笔记不会创建，最后一个字符串用于提示你选择的内容；
#### 4. 实际演示1-模板转笔记
快捷键 `Ctrl + P` 输入 `templater` 观察到选项：
- `Templater: Replace templates in the active file`：自动把当前模板套用到当前笔记；
	- 会将当前的模板转换为笔记，可以用于测试模板代码；
#### 5. 实际演示2-应用模板
1. 创建一篇笔记
2. 快捷键 `Ctrl + P` 输入 `templater` 选择选项 `Templater: Open Insert Template modal` ，表示插入你的模板；
3. 选择你的模板；
#### 6. 实际演示3-文件夹指定模板
1. 进入 `templater` 设置界面，找到 `Folder Templates` ，功能是 给指定文件夹以固定的模板；
2. 点击 `Add New` 点击 加号，选择文件夹以及希望使用到的模板；
3. 然后右键点击文件夹创建文件就可以直接使用模板；
### 2. 进阶内容

#### 1. 进阶模板


#### 2. Capture 随时记录想法
[[Capture]]


#### 3. 插入脚注
[[Insert Callouts]]



```templater

```


.
