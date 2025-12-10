---
date_create: 2025-12-08-星期一
software: vim
status: completed
source: video
---
# 00链接
| 序号  |                         文件                          | 类型  | 介绍              | 状态  |    添加时间    |
| :-: | :-------------------------------------------------: | :-: | --------------- | :-: | :--------: |
| 01  |        [VimAwesome](https://vimawesome.com/)        | 🌐  | 收集了各种Vim插件      |  ✅  | 2025-12-08 |
| 02  |  [vim-plug](https://github.com/junegunn/vim-plug)   | 🌐  | 用于安装插件；GitHub网址 |  ✅  | 2025-12-08 |
| 03  | [UP配置文件](https://github.com/MarsWang42/My-Vim-Conf) | 🌐  | GitHub网址        |  ✅  | 2025-12-08 |
# 01课程

## 00目录
| 序号  |                                   内容                                    | 类型  | 介绍                                                           | 状态  |
| :-: | :---------------------------------------------------------------------: | :-: | ------------------------------------------------------------ | :-: |
| 01  |                                  基础操作                                   | ✏️  | 记录了一些我不太熟悉的命令<br>**详见下方**                                    |  ✅  |
| 02  |  [插件下载-NERDTree](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=1028.2)  | 📽️ | Up强烈推荐使用Vimplug下载安装插件<br>进行了尝试，总结了一些问题，**详见下方**<br>          |  ✅  |
| 03  |  [插件配置-NERDTree](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=1197.9)  | 📽️ | 将NERDTree的命令进行快捷键<br>**详见下方及视频**                             |  ✅  |
| 04  |                                UP的Vim配置                                 | ✏️  | 基本展示；<br>学习了在NERDTree下添加标签页<br>以及添加了标签页切换的键位设置代码<br>**详见下方** |  ✅  |
| 05  | [UP对比-Vim与VSCode](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=1287.1) | 📽️ | Vim插件使得Vim使用体验相差不大，<br>但是运行速度更快                              |  ✅  |
### 01基础操作

| 序号  |                               文件                               | 类型  | 介绍                                         | 状态  |
| :-: | :------------------------------------------------------------: | :-: | ------------------------------------------ | :-: |
| 01  |    [G](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=486.4)    | 📽️ | 到达文件最下方，对应VSCode中的`End`<br>具体效果 **详见下方**   |  ✅  |
| 02  | [<C-U/D>](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=490.9) | 📽️ | 分别对应向上/下翻页                                 |  ✅  |
| 03  |                      `:h <command_line>`                       | 💬  | 通过该方式可以查看命令的含义<br>例如：`:h aw`               |  ✅  |
| 04  | [c+c/4j](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=686.0)  | 📽️ | 分别为删除该行并进入插入模式；<br>删除下4行进入插入模式<br>**详见视频** |  ✅  |
#### 01G
- [ ] 2025-12-08 12:55: 实际在VSCode中进行尝试，但是直接使用键盘 `End` 无法到达V文档最后一行；
### 02插件下载
#### 01操作步骤
- 该视频下载使用的是韩国人开发的 `00-02` vim-plug，下载教程详见视频和网站；
```powershell
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
    ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/nvim-data/site/autoload/plug.vim" -Force
```

```vimscript
call plug#begin()

" List your plugins here
Plug 'scrooloose/nerdtree'

call plug#end()
```
- 将该代码放置于 `:echo $MYVIMRC` 所展示的文件中
- 然后重启，使用vim打开，并输入命令 `:PlugInstall` 即可安装插件；
-  `:NERDTree` 即可打开文档树

#### 02存在问题

| 序号  |                  问题                  | 介绍                  | 状态  |    添加时间    |     |
| :-: | :----------------------------------: | ------------------- | :-: | :--------: | :-: |
| 01  |                插件存储位置                | 插件位置好像位于C盘占用空间      |  ❌  | 2025-12-08 |     |
| 02  | 无法通过Neovim进行<br>命令`:PlugInstall`下载插件 | ✅到达插件安装位置将其卸载后重新安装； |  ✅  | 2025-12-08 |     |
| 03  |             vim的命令缺少自动补全             | ❌                   |  ❌  | 2025-12-08 |     |
### 03插件配置-NERDTree
- [ ] 代码来源为deepseek
```vimscript
nnoremap <leader>e :NERDTreeToggle<CR>
```
- *提示*：将该代码放置于 `:echo $MYVIMRC` 所展示的文件中
- 通过主键+e，即可打开文件树；
- 通过 `o` 打开文件及文件夹
### 04UP的Vim配置
| 序号  |                                 内容                                 | 类型  | 介绍                            | 状态  |    添加时间    |
| :-: | :----------------------------------------------------------------: | :-: | ----------------------------- | :-: | :--------: |
| 01  |   [Vim主题](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=1236.2)    | 📽️ | 主题使用为`Groovbox`，<br>该主题对比度比较低 |  ✅  | 2025-12-08 |
| 02  | [操作-文件打开/切换](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=1243.9) | 📽️ | 标签页操作及键位映射修改<br>**详见下方**      |  ✅  | 2025-12-08 |
| 03  |  [展示-代码报错](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=1268.1)   | 📽️ | **详见视频**                      |  ✅  | 2025-12-08 |
| 04  |  [展示-自动补全](https://www.bilibili.com/video/BV1UQ4y1z7q5?t=1275.1)   | 📽️ | **详见视频**                      |  ✅  | 2025-12-08 |
#### 02操作-文件打开/切换
**标签页操作**

| 序号  | 键位  | 介绍        | 状态  |
| :-: | :-: | --------- | :-: |
| 01  | `o` | 当前标签页打开文件 |  ✅  |
| 02  | `t` | 新建标签页打开文件 |  ✅  |
| 03  |     |           |     |
|     |     |           |     |
**键位映射**
- [ ] 代码来源为deepseek
```vimscript
nnoremap <S-H> :tabprevious<CR> 
nnoremap <S-L> :tabnext<CR>
```
- *提示*：将该代码放置于 `:echo $MYVIMRC` 所展示的文件中
- 能够更换buffer

