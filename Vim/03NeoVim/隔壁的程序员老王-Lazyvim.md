---
date_create: 2025-11-23-星期日
type: Software
software: NeoVim
status: stopped
source: video
---
# 00目录
| 序号  |                                                  文件                                                  | 类型  | 简介                                                                                                                  | 状态  |    添加时间    |
| :-: | :--------------------------------------------------------------------------------------------------: | :-: | ------------------------------------------------------------------------------------------------------------------- | :-: | :--------: |
| 01  |                                              Neovim扔掉鼠标                                              | ✏️  | 讲解了如何启动终端；<br>Neo-tree对隐藏文件的显示操作<br>buffer的关闭、插件WhichKey的简单介绍<br>**详见视频**                                           |  ✅  | 2025-12-08 |
| 02  |                                          lsp 让neovim更懂你的代码                                           | ✏️  | 介绍了lsp服务的下载和基础知识；<br>了解了lazyextras的使用；<br>leap.nvim更加详细的理解<br>fzf查找文件的方法<br>行选中模式、增加/减少缩进方法<br>语言函数定义跳转<br>**详见下方** |  ✅  | 2025-12-08 |
| 03  |            [neovim + 最强国产大模型deepseek 自动写代码](https://www.bilibili.com/video/BV15VrLYyEA8)             | 📽️ | neovim集成大模型的插件的使用介绍；未观看和尝试                                                                                          |  ❌  | 2025-12-08 |
| 04  | [neovim编辑技巧](https://www.bilibili.com/video/BV1y4cWeiEnX?vd_source=aef73766b941d8e52cb9a97d24ea42a2) | ✏️  | 处理成对的符号的方式；跳转的方法；如何整块操作；<br>**详见下方**                                                                                |  ✅  | 2025-12-08 |
## 01Neovim扔掉鼠标

| 序号  |                                 内容                                  | 类型  | 介绍                                                           | 状态  |
| :-: | :-----------------------------------------------------------------: | :-: | ------------------------------------------------------------ | :-: |
| 01  |   [nvim打开终端](https://www.bilibili.com/video/BV1TJCvYFE2T?t=440.8)   | 📽️ | `<C-/>` 即可打开或关闭终端                                            |  ✅  |
| 02  |    [显示隐藏文件](https://www.bilibili.com/video/BV1TJCvYFE2T?t=493.7)    | 📽️ | `shift+H` 即可显示或隐藏 隐藏文件                                       |  ✅  |
| 03  |   [关闭buffer](https://www.bilibili.com/video/BV1TJCvYFE2T?t=537.2)   | 📽️ | `<space>+B+D` 为 关闭buffer的方法之一                                |  ✅  |
| 04  | [插件-Which_Key](https://www.bilibili.com/video/BV1TJCvYFE2T?t=553.0) | 📽️ | *演示*：输入 `<leader>` 后有命令含义的提示<br>对于其他命令同样有命令含义的提示<br>**详见视频** |  ✅  |
| 00  |  [Neovim基础配置](https://www.bilibili.com/video/BV1TJCvYFE2T?t=17.8)   | 📽️ | 由于[[现代化Vim教程\|其他相关链接]]已经有详细介绍，故省略                            |  ❌  |
## 02 lsp 让neovim更懂你的代码

|  序号   |                                  内容                                  | 类型  | 介绍                                                                                                    | 状态  |
| :---: | :------------------------------------------------------------------: | :-: | ----------------------------------------------------------------------------------------------------- | :-: |
|  01   |   [lsp服务说明及下载](https://www.bilibili.com/video/BV1up6XYgEzL?t=24.1)   | 📽️ | 过程 **详见视频**；笔记**详见下方**                                                                                |  ✅  |
|  02   |   [pyright讲解](https://www.bilibili.com/video/BV1up6XYgEzL?t=129.4)   | 📽️ | neovim并不懂语言知识，需要与语言服务器<br>pyright是python的语言服务器<br>rust对应 `rust analyzer`、<br>C对应 `clangd`<br>**详见视频** |  ✅  |
|  03   |   [lazyvim文档](https://www.bilibili.com/video/BV1up6XYgEzL?t=212.2)   | 📽️ | 讲解如何从文档中找到扩展中找到相应的说明<br>                                                                              |  ✅  |
|  04   |  [pyright功能展示](https://www.bilibili.com/video/BV1up6XYgEzL?t=274.1)  | 📽️ | 参数显示，自动补全；**详见视频**                                                                                    |  ✅  |
|  05   | [pright-跳转函数定义](https://www.bilibili.com/video/BV1up6XYgEzL?t=352.6) | 📽️ | 具体操作，**详见下方**                                                                                         |  ✅  |
| 05.01 |     [fzf介绍](https://www.bilibili.com/video/BV1up6XYgEzL?t=394.8)     | 📽️ | fzf是一个用来查找文件的工具；其他细节                                                                                  |  ✅  |
|  06   | [插件-leap.nvim](https://www.bilibili.com/video/BV1up6XYgEzL?t=321.5)  | 📽️ | lazyvim自带插件；能够实现长距离移动；**详见下方**                                                                        |  ✅  |
|  07   |    [操作-文件切换](https://www.bilibili.com/video/BV1up6XYgEzL?t=441.9)    | 📽️ | 双击`<leader>` 搜索文件名即可搜索对应文件<br>`<C-j/k>` 光标上/下移动                                                       |  ✅  |
|  08   |    [操作-增加缩进](https://www.bilibili.com/video/BV1up6XYgEzL?t=535.8)    | 📽️ | `>>/<<` 增加/减少缩进                                                                                       |  ✅  |
|  09   |     [操作-注释](https://www.bilibili.com/video/BV1up6XYgEzL?t=553.5)     | 📽️ | 选中需要注释的代码，`gc`即可取消或者注释代码                                                                              |     |
| 09.01 |   [操作-行选中模式](https://www.bilibili.com/video/BV1up6XYgEzL?t=558.3)    | 📽️ | `shift+V`即可进入行选中                                                                                      |  ✅  |
### 01lsp服务说明及下载
- `:LazyExtras` 打开lazyvim的扩展界面，这个界面包含了各种语言的支持插件，还有很多其他的实用可选插件；
- 顶部的提示告诉我们，能够使用 `X` 打开或者关闭扩展；
- 如果想要查找相应的插件，使用基本语法 `/+<find_string>` 进行搜索
### 05函数定义跳转
- 移动光标到函数上
- `g` 还有其他的功能
	- `gd` 直接跳转到函数的定义；
	- [ ] 视频中无法跳转；引文作者工作中使用的neovim版本比较老；需要安装fzf
### 05.01 fzf
- fzf是一个用来查找文件的工具
- 在以前的版本，lazyvim是用telescope插件来实现文件的查找的
### 06插件-leap.nvim
`s + <jump_strings>` 然后根据后面提示的字符进行跳转即可；

## 04neovim编辑技巧
| 序号  |                                   内容                                    | 类型  | 介绍                                                                       | 状态  |
| :-: | :---------------------------------------------------------------------: | :-: | ------------------------------------------------------------------------ | :-: |
| 01  |                                  跳转方法                                   | ✏️  | 常用的几种跳转方式，**详见下方**                                                       |  ✅  |
| 02  |    [删除-dw/diw](https://www.bilibili.com/video/BV1y4cWeiEnX?t=190.7)     | 📽️ | `diw`能够删除整个单词，<br>而`dw`只能够删除光标后半段内容                                      |  ✅  |
| 03  |   [删除+插入-cw/ciw](https://www.bilibili.com/video/BV1y4cWeiEnX?t=220.5)   | 📽️ | `cw/ciw`能够直接删除后进行插入<br>**与** `02`**类似**                                  |  ✅  |
| 04  |                                选中-vw/viw                                | ✏️  | 与上述两个逻辑相同，就不引用视频                                                         |  ✅  |
| 05  | [v/d/ci(-操作括号中的内容](https://www.bilibili.com/video/BV1y4cWeiEnX?t=280.6) | 📽️ | 该方式能够操作，`()`中的内容；<br>同理`"`能够对引号中的内容进行操作<br>**总结**：只要是成对出现的符号都能够使用该方式进行操作 |  ✅  |
| 06  |       [UP建议](https://www.bilibili.com/video/BV1y4cWeiEnX?t=415.0)       | 📽️ | 在使用中去学习，同时留意命令提示                                                         |  ✅  |
### 01跳转方法
| 序号  |                                 内容                                 | 类型  | 介绍                                                                 | 状态  |
| :-: | :----------------------------------------------------------------: | :-: | ------------------------------------------------------------------ | :-: |
| 01  |   [单词跳转-w/b](https://www.bilibili.com/video/BV1y4cWeiEnX?t=48.2)   | 📽️ | `w/b` 分别以单词为单位向后/前移动                                               |  ✅  |
| 02  |     [跳转-f](https://www.bilibili.com/video/BV1y4cWeiEnX?t=65.0)     | 📽️ | `f+<letter>` 接着 `f/shift+f` <br>分别继续向后/前进行跳转<br>再次 `<letter>` 结束跳转 |  ✅  |
| 03  |     [跳转-s](https://www.bilibili.com/video/BV1y4cWeiEnX?t=115)      | 📽️ | `s+<string>`接着输入对应后面的字母即可完成跳转                                      |  ✅  |
| 04  | [方括号跳转-e错误位置](https://www.bilibili.com/video/BV1y4cWeiEnX?t=137.6) | 📽️ | `[/]+e` 分别跳转到上/下一个错误位置                                             |  ✅  |
| 05  | [方括号跳转-a参数跳转](https://www.bilibili.com/video/BV1y4cWeiEnX?t=161.3) | 📽️ | `[/]+a` 跳转到函数上/下一个参数位置                                             |  ✅  |




