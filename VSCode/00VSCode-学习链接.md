---
date_create: 2025-11-11-星期二
foreword: Software
status: unstarted
source: video
software: VSCode
---
VSCode会自动进行更新
# 00链接
| 序号  |                                  文件                                  | 类型  | 介绍                 |
| :-: | :------------------------------------------------------------------: | :-: | ------------------ |
| 01  | [文件夹-Vim配置参考](file:E:\01Projects\25autumn\03Creation\05Config\Vimrc) | 📙  | 提供可以参考的Vim配置代码     |
| 02  |                            [[VSCodeVim]]                             | 📄  | 讲解了VSCode中Vim插件的文档 |
| 03  |                                                                      |     |                    |


# 00课程

| 序号  |                                                                         链接                                                                         |   作用    | 评价  |
| :-: | :------------------------------------------------------------------------------------------------------------------------------------------------: | :-----: | :-: |
| 01  |                                      [vscode安装教程vscode配置c/c++教程](https://www.bilibili.com/video/BV1tyAtetEd1)                                      |  下载教程   |  ⭐  |
| 02  |                                         [VS Code常用实用必备宝藏插件集合](https://www.bilibili.com/video/BV1Xg411X74K)                                         |  插件下载   | ⭐⭐  |
| 03  | [VsCode五分钟上手教程](https://www.bilibili.com/video/BV1bK411P767/?spm_id_from=333.337.search-card.all.click&vd_source=aef73766b941d8e52cb9a97d24ea42a2) |  入门教程   |  ✅  |
| 04  |                                           [史上最牛Vim+VsCode](https://www.bilibili.com/video/BV1JE421L7pi)                                            |  Vim配置  |     |
| 05  |                                         [在VSCode中使用Vim的正确姿势](https://www.bilibili.com/video/BV1xp4y1Q7rD)                                          |  Vim配置  |     |
| 06  |                                                                                                                                                    |  技巧教程   |     |
| 07  |                                          [VS Code LaTeX安装](https://www.bilibili.com/video/BV18zsbz1ErV/)                                           | Latex下载 |     |
|     |                                                                                                                                                    |         |     |
# 00目录

| 序号  |                              笔记                              | 类型  | 介绍                                                                    | 状态  |
| :-: | :----------------------------------------------------------: | :-: | --------------------------------------------------------------------- | :-: |
| 01  |                      [[01VSCode配置C++]]                       | 📄  | 介绍了VSCode下载教程<br>以及C语言编译器的下载及使用                                       |  ✅  |
| 02  |                       [[02VSCode宝藏插件]]                       | 📄  |                                                                       |  ⏳  |
| 03  |                       [[03VSCode上手教程]]                       | 📄  | 主题颜色修改；字体更改及大小设置；<br>背景图片设置<br>**详见文档**                               |  ✅  |
| 04  |                     [[04-01Vim+VSCode]]                      | 📄  |                                                                       |  ⏳  |
| 05  |                     [[05-02VSCode+Vim]]                      | 📄  | Vim扩展的使用技巧，包括：<br>键位设置、跳转、标签页更换<br>更换成对符号、查看函数定义、光标跳转<br>**详见文档**<br> |  ✅  |
| 06  |                    [[06隔壁的程序员老王-VSCode]]                     | 📄  | 包含VSCode扩展推荐、<br>常用快捷键<br>**详见文档**                                    |  ❌  |
| 07  |                     [[07VSCode配置Latex]]                      | 📄  |                                                                       |     |
|  8  | [vscode 算法刷题神器](https://www.bilibili.com/video/BV1qCPheUE5m) | 📽️ | 通过视频讲解了VSCode中leetcode插件下载和使用<br>同时这也是插件开发作者本人的视频账号                   |  ✅  |

# 99存在问题
| 序号  |                 问题                 | 介绍                                                    | 状态  |    添加时间    |
| :-: | :--------------------------------: | ----------------------------------------------------- | :-: | :--------: |
| 01  |               设置相对行号               | ❌                                                     |  ✅  | 2025-12-09 |
| 02  |        VSBrowser插件无法实时更新URI        | 问题本质是想要在VSCode中打开浏览器，<br>一边浏览网页一边进行代码编辑，<br>结合在一起进行学习 |  ❌  | 2025-12-17 |
| 03  | 在Vim和Jupyter插件同时打开的时候，<br>无法征程输入中文 | ❌                                                     |  ❌  | 2025-12-17 |
|     |                                    |                                                       |     |            |
## 01设置相对行号
`ctrl+shift+P->Open User Setting(Json)` 打开配置文件`settings.json`，在安装了Vim插件后将下方代码复制进配置文件即可；

```json
 {
 "editor.lineNumbers": "relative",
  "vim.smartRelativeLine": true
 }
```










