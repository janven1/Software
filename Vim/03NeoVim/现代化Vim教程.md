---
date_create: 2025-11-22-星期六
type: Software
status: unstarted
source: video
software: NeoVim
---
# 00链接
| 序号  |                            内容                            | 类型  | 介绍                                  | 状态  |
| :-: | :------------------------------------------------------: | :-: | ----------------------------------- | :-: |
| 01  | [gitee-scoop配置](https://gitee.com/scoop-installer/scoop) | 🌐  | 详细介绍了scoop的安装和使用                    |  ✅  |
| 02  |         [lazyvim下载教程](https://www.lazyvim.org/)          | 🌐  | lazyvim的官方下载教程                      |  ✅  |
| 03  |     [UP‘s lazyvim配置](https://github.com/pdcxs/nvim)      | 🌐  | UP提供了一个修改neovim配置文件夹改变的脚本，避免C盘占用内存； |  ✅  |
| 04  |         [NerdFont官网](https://www.nerdfonts.com/)         | 🌐  | 可下载相应的字体用于neovim插件需要的图标显示           |  ✅  |
| 05  |     [neovide网址](https://github.com/neovide/neovide)      | 🌐  | 用于下载安装neovide                       |  ✅  |
# 01课程
## 00目录

| 序号  |                                     内容                                     | 类型  | 介绍                                                                                     | 状态  |
| :-: | :------------------------------------------------------------------------: | :-: | -------------------------------------------------------------------------------------- | :-: |
| 02  |       [UP经验-Vim](https://www.bilibili.com/video/BV1HJRyYgE9k?t=1.5)        | 📽️ | 对目前使用Vim的现状进行了说明(*听得不是很明白*) <br>Vim学习理由、该教程特点、lazyvim作用(可以将配置省略，和大多数IDE相同)<br>**详见视频** |  ✅  |
| 01  |                                    环境搭建                                    |  ⏳  | 使用scoop介绍了LazyVim的安装教程<br>**详见下方**                                                     |  ⏳  |
| 03  |                               UP个人lazyvim配置                                | ✏️  | 请结合 [[Neovim从零配置\|📄Neovim从零配置]] 了解neovim配置的基础文件结构和逻辑：                                 |     |
|     | [操作-PowerToys修改键位映射](https://www.bilibili.com/video/BV1HJRyYgE9k?t=1434.5) | 📽️ | 将ESC键映射为大写锁定 **略**                                                                     |  ❌  |
|     |                                    UP主题                                    |     |                                                                                        |     |
## 01环境搭建
|  序号   |                                   文件                                    | 类型  | 介绍                                              | 状态  |
| :---: | :---------------------------------------------------------------------: | :-: | ----------------------------------------------- | :-: |
|  01   |    [Scoop使用教程1](https://www.bilibili.com/video/BV1HJRyYgE9k?t=221.1)    | 📽️ | 提供了网址，即 `00-01`                                 |  ✅  |
|  02   | [Powershell添加环境变量](https://www.bilibili.com/video/BV1HJRyYgE9k?t=269.7) | 📽️ | 应用场景：自定义scoop环境变量<br>**实际操作的经验及代码如下**           |  ✅  |
|  03   |    [scoop安装及配置](https://www.bilibili.com/video/BV1HJRyYgE9k?t=335.4)    | 📽️ | 完成 `02` 后进行该步骤<br>**详见视频**                      |  ✅  |
|  05   |  [更改nvim配置文件夹位置](https://www.bilibili.com/video/BV1HJRyYgE9k?t=372.0)   | 📽️ | 具体逻辑和内容 **详见下方**<br>具体操作和文件夹细节 **见视频**          |  ✅  |
| 05.01 |       [xgd脚本](file:E:\01Projects\25autumn\03Creation\11sh\01xgd)        | 📙  | **详见文件夹**                                       |  ✅  |
|  06   |       [具体安装](https://www.bilibili.com/video/BV1HJRyYgE9k?t=627.9)       | 📽️ | 具体lazyvim官网安装讲解 <br>**详见视频**<br>具体安装软件 **整理如下** |  ✅  |
### 02Powershell添加环境变量
```powershell
[Environment]::SetEnvironmentVariable('<用户变量中的的具体某个变量>', '<Path>', 'USER')
```
- **配置后重启Powershell**，即可；
- [ ] 实际使用的过程中其实，是将路径添加了用户变量中
- [ ] **注意**：最好不要使用因为可能覆盖原来的环境变量；
- [ ] 同时在windows中可执行的文件需要配置在PATH的环境变量中才能够运行；
### 05更改neovim配置文件夹位置
Neovim的默认配置文件夹位置为
```powershell
cd $env:LOCALAPPDATA
```
其配置文件会下载插件导致C盘空间占用较大，需要更改配置文件夹位置；
- 其配置文件夹名称为 `nvim` 和 `nvim-data`(主要内存占用的文件夹)
原理——
- nvim支持xgd的格式❓，设置好相应的环境变量即可；
操作——
- UP提供相应的脚本链接 `00-03` 具体脚本位于 `../01-05.01`
### 06具体安装
| 序号  |   软件   | 介绍        | 状态  |
| :-: | :----: | --------- | :-: |
| 01  | Neovim | 注意软件安装的版本 |     |
| 02  |  Git   | 已经在安装     |     |
| 03  |        |           |     |
|     |        |           |     |



## UP个人lazyvim配置
| 序号  |                                  内容                                  | 类型  | 介绍                                                                                  | 状态  |
| :-: | :------------------------------------------------------------------: | :-: | ----------------------------------------------------------------------------------- | :-: |
| 00  |   [config说明](https://www.bilibili.com/video/BV1HJRyYgE9k?t=1033.2)   | 📽️ | 视频开头；链接为 `00-03`                                                                    |  ✅  |
| 01  | [autocmds.lua](https://www.bilibili.com/video/BV1HJRyYgE9k?t=1040.6) | 📽️ | 用于xmake管理C++项目-*配置修改*<br>python-*配置修改*—**实际文件已经改动不再有该内容**<br>**代码如下**               |  ✅  |
| 02  |                               lazy.lua                               |  ❌  | 基本未改动                                                                               |  ✅  |
| 03  |                             options.lua                              | ✏️  | 配置了neovide的显示设置；以及neovim的自身设置<br>**详见下方**                                           |  ✅  |
| 04  | [keymaps.lua](https://www.bilibili.com/video/BV1HJRyYgE9k?t=1217.3)  | 📽️ | 配置了neovide中显示调节的快捷键；<br>**代码如下**                                                    |  ✅  |
| 05  |   [plugins](https://www.bilibili.com/video/BV1HJRyYgE9k?t=1378.1)    | 📽️ | 记录了UP的主题rose-pine配置代码；**代码如下**<br>从Deepseek中学习了如何更换主题以及取消主题显示和删除具体的插件的文件路径 **详见下方** |  ✅  |
### 01autocmds.lua
```lua
if not vim.g.vscode then
  vim.cmd([[
    if has('win32') || has('win64')
      let &shell = executable('pwsh') ? 'pwsh' : 'powershell'
      let &shellcmdflag = '-NoLogo -ExecutionPolicy RemoteSigned -Command [Console]::InputEncoding=[Console]::OutputEncoding=[System.Text.UTF8Encoding]::new();$PSDefaultParameterValues[''Out-File:Encoding'']=''utf8'';Remove-Alias -Force -ErrorAction SilentlyContinue tee;'
      let &shellredir = '2>&1 | %%{ "$_" } | Out-File %s; exit $LastExitCode'
      let &shellpipe  = '2>&1 | %%{ "$_" } | tee %s; exit $LastExitCode'
      set shellquote= shellxquote=
    endif
    ]])

  vim.api.nvim_create_autocmd("FileType", {
    pattern = "lua",
    callback = function()
      -- 获取当前缓冲区文件名（不含路径）
      local filename = vim.fn.fnamemodify(vim.api.nvim_buf_get_name(0), ":t")
      -- 仅当文件名为 xmake.lua 时禁用格式化
      if filename == "xmake.lua" then
        vim.b.autoformat = false
      end
    end,
  })

  vim.api.nvim_create_autocmd("FileType", {
    pattern = "java",
    callback = function()
      vim.keymap.set("n", "<leader>cj", function()
        local filename = vim.fn.expand("%:t") -- 获取带扩展名的文件名
        local file_dir = vim.fn.expand("%:p:h")
        vim.cmd("w")
        local cmd = string.format("java %s", filename)
        Snacks.terminal(cmd, {
          cwd = file_dir,
          auto_close = false,
          interactive = true,
        })
      end, { desc = "Run Java File", buffer = true })
      vim.keymap.set("n", "<leader>cJ", function()
        local filename = vim.fn.expand("%:t") -- 获取带扩展名的文件名
        local classname = vim.fn.expand("%:t:r") -- 获取类名（无扩展名）
        local file_dir = vim.fn.expand("%:p:h")
        vim.cmd("w")
        local cmd = string.format("javac %s && java %s", filename, classname)
        Snacks.terminal(cmd, {
          cwd = file_dir,
          auto_close = false,
          interactive = true,
        })
      end, { desc = "Compile & Run Java File", buffer = true })
    end,
  })

  -- 停止 markdown 拼写检查
  -- vim.api.nvim_del_augroup_by_name("lazyvim_wrap_spell")
end
```
- [ ] 具体的代码含义尝试求助Deepseek，但是没有看懂；
### 03options.lua
| 序号  |                                 文件                                 | 类型  | 介绍       | 状态  |
| :-: | :----------------------------------------------------------------: | :-: | -------- | :-: |
| 01  | [neovide配置](https://www.bilibili.com/video/BV1HJRyYgE9k?t=1108.4)  | 📽️ | **代码如下** |  ✅  |
| 02  | [vim.opt 配置](https://www.bilibili.com/video/BV1HJRyYgE9k?t=1154.7) | 📽️ | **代码如下** |  ✅  |
#### 01neovide配置
```lua
if vim.g.neovide then
  -- set the size and type of font
  vim.o.guifont = "CaskaydiaCove Nerd Font:h15"
  -- set the mode of cursor_mode
  vim.g.neovide_cursor_vfx_mode = "railgun"
  vim.g.neovide_scale_factor = 0.9
  -- turn off animate becuase we are using neovide
  vim.g.snacks_animate = false
  -- vim.g.neovide_fullscreen = true
end
```
#### 02vim.opt 配置 
```lua
local opt = vim.opt

-- 自动换行
opt.wrap = true
-- 检查语法，添加 "cjk"不检查中文语法，否则输入中文会报错
opt.spelllang = { "en", "cjk" }
-- 中文断行
opt.linebreak = false

-- 仅将当前工作目录（Current Working Directory）作为根目录
vim.g.root_spec = { "cwd" }
```
### 04kemaps.lua
```lua
if vim.g.neovide then
  -- 屏幕缩小
  vim.keymap.set({ "n", "v" }, "<C-=>", ":lua vim.g.neovide_scale_factor = vim.g.neovide_scale_factor + 0.1<CR>")
  -- 屏幕放大
  vim.keymap.set({ "n", "v" }, "<C-->", ":lua vim.g.neovide_scale_factor = vim.g.neovide_scale_factor - 0.1<CR>")
  -- 屏幕初始化大小
  vim.keymap.set({ "n", "v" }, "<C-0>", ":lua vim.g.neovide_scale_factor = 0.9<CR>")
  -- 全屏覆盖
  vim.keymap.set({ "n", "v" }, "<C-f>", ":lua vim.g.neovide_fullscreen = not vim.g.neovide_fullscreen<CR>")
end
```
### 05plugins
```lua
-- lua/plugins/rose-pine.lua
return {
  "rose-pine/neovim",
  name = "rose-pine",
  config = function()
    vim.cmd("colorscheme rose-pine")
  end,
}
```
- 将代码以文件 `rose-pine.lua` 保存并将其放置在其保存在路径 `nvim/lua/plugins/rose-pine.lua` 等待重新启动nvim自动安装更新即可；
取消主题的使用——
- 1.**保留插件但禁用自动加载**
```lua
return {
  "rose-pine/neovim",
  name = "rose-pine",
  lazy = true,  -- 设置为懒加载
  -- 移除 config 部分或者注释掉
}
```
- 2.**切换主题**
```vim
:colorscheme default
```
- 3.**完全移除插件**
	- 1. 删除 `lua/plugins/rose-pine.lua` 文件
	- 2. 运行 `:Lazy clean` 命令移除未使用的插件


# Summary
## 01存在问题
| 序号  | 问题  | 介绍  | 状态  | 添加时间 |
| :-: | :-: | --- | :-: | :--: |
| 01  |     |     |     |      |
| 02  |     |     |     |      |
| 03  |     |     |     |      |
|     |     |     |     |      |

## 02优秀之处
| 序号  |      内容       | 介绍  | 状态  |
| :-: | :-----------: | --- | :-: |
| 01  | 下载并了解了wezterm |     |     |
| 02  |               |     |     |
| 03  |               |     |     |
|     |               |     |     |







