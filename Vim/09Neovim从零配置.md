---
date_create: 2025-11-21-星期五
type: Software
status: unstarted
source: video
---
```Vim
#确认NeoVim的配置文件位置
:echo stdpath("config")
```
# 课程

| 序号  |                                内容                                 | 介绍                                                   | 状态  |
| :-: | :---------------------------------------------------------------: | ---------------------------------------------------- | :-: |
| 01  | [经验-NeoVim配置](https://www.bilibili.com/video/BV1Td4y1578E?t=4.5)  | 项目大的时候，使用VSCode体验不好；<br>电脑配置有限，不同主机都能快速配置            |     |
| 02  |    [教程说明](https://www.bilibili.com/video/BV1Td4y1578E?t=41.0)     | NeoVim版本：插件要求的版本可能较高；<br>NeoVim安装下载介绍                |     |
| 03  |  [操作-创建配置文件](https://www.bilibili.com/video/BV1Td4y1578E?t=58.8)  | 创建配置的文件；<br>详见下方                                     |     |
| 04  |   [操作-基础配置](https://www.bilibili.com/video/BV1Td4y1578E?t=91.6)   | lua是编程语言，文件需要使用lua的语法，<br>操作—增加行号: 可以用于测试是否配置有效<br>略 |     |
| 05  | [操作-模块化方式配置](https://www.bilibili.com/video/BV1Td4y1578E?t=131.6) | 功能细分为不同文件，更像写项目代码<br>具体操作详见下方                        |     |
| 06  | [操作-选项基础配置](https://www.bilibili.com/video/BV1Td4y1578E?t=165.3)  | 由于代码说明详细无预览；详见下方                                     |     |
| 07  |  [操作-键位配置](https://www.bilibili.com/video/BV1Td4y1578E?t=326.4)   | 详见下方                                                 |     |
| 08  | [操作-插件管理下载](https://www.bilibili.com/video/BV1Td4y1578E?t=491.6)  | 视频使用的为packer⏳<br>不过现在好像使用lazynvim的数量更多后续再查看          |  ⏳  |
| 09  |                                                                   |                                                      |     |
| 10  |                                                                   |                                                      |     |
| 11  |                                                                   |                                                      |     |
| 12  |                                                                   |                                                      |     |
| 13  |                                                                   |                                                      |     |
| 14  |                                                                   |                                                      |     |
| 15  |                                                                   |                                                      |     |
| 16  |                                                                   |                                                      |     |
| 17  |                                                                   |                                                      |     |
| 18  |                                                                   |                                                      |     |
| 19  |                                                                   |                                                      |     |
|     |                                                                   |                                                      |     |

## 03操作-创建配置文件
```bash
mkdir -p .config/nvim
cd .config/nvim
touch init.lua
```
## 04操作-基础配置
```lua

```
## 05操作-模块化配置
![[04NVim文件配置树.png]]
- 能够按照图示结构创建相应的文件夹和文件即可
```bash
mkdir lua
cd lua
mkdir core %可以取其他名
touch options.lua
```
## 06操作-配置基础选项功能
- options.lua
```lua
local opt = vim.opt

--字体设置
opt.guifont = "Hack Nerd Font Mono:h12"  -- GUI版本（如Neovim-qt）
vim.g.nerdfont = true  -- 显式声明使用Nerd Font

--行号
opt.relativenumber = true
opt.number = true

--缩进
opt.tabstop = 4
opt.shiftwidth = 4
opt.expandtab = true
opt.autoindent = true

--防止包裹
opt.wrap = false

--光标行
opt.cursorline = ture

--启用鼠标
opt.mouse:append("a")

--系统剪切板
opt.clipboard:append("unnamedplus")

--默认新窗口右和下
opt.splitright = true
opt.splitbelow = true

--搜索
opt.ignorecase = true
opt.smartcase =true

--外观
opt.termguicolors = true
opt.signcolumn = "yes"

```
- init.lua
```lua
require("core.options")
```
- 引用的时候前面不需要加lua文件夹名字，NeoVim会自动识别到这里
- 文件夹的分级可以用英语句号`.`来分割
- 不需要标注`.lua`后缀名
## 07操作-键位配置
```lua
--设置主键为空格
vim.g.mapleader = " "

local keymap = vim.keymap

-- --------------插入模式------------- --
keymap.set("i", "jk", "<ESC>")
--参数1为模式，参数2为改后的键位，参数3为原来键位

-- --------------视觉模式------------- --
-- 单行或多行移动
keymap.set("v", "J", ":m '>+1<CR>gv=gv")
keymap.set("v", "K", ":m '<-2<CR>gv=gv")

-- --------------正常模式------------- --
-- 窗口
keymap.set("n", "<leader>sv", "<C-w>v") --水平新增窗口
keymap.set("n", "<leader>sh", "<C-w>s") --垂直新增窗口

-- 取消高亮
keymap.set("n", "<leader>nh", ":nohl<CR>")
```
- 改键一开始不要改动太多，不然容易遗忘或与系统键位冲突


















