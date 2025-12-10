---
date_create: 2025-12-08-星期一
type: Software
software:
status: unstarted
source:
---
- 查看vim的配置文件位置
```vim
:echo $MYVIMRC
```


- 注释为 `"`
- 设置Vim字体及其大小
```vimscript
set guifont=<字体名称>:h<字号>
set guifont=CaskaydiaCove Nerd Font:h15
```
- 设置主键
```vimscript
let mapleader = " "
```
- 设置分屏
```vimscript
"上下分屏
nnoremap <leader>sh :split<CR>
"左右分屏
nnoremap <leader>sv :vsplit<CR>

```
- 窗口跳转
```vimscript
nnoremap <C-h> <C-w>h  " Ctrl+h 跳左窗口
nnoremap <C-j> <C-w>j  " Ctrl+j 跳下窗口
nnoremap <C-k> <C-w>k  " Ctrl+k 跳上窗口
nnoremap <C-l> <C-w>l  " Ctrl+l 跳右窗口
```
- 终端键位映射
```vimscript
nnoremap <C-/> :terminal pwsh<CR>
tnoremap <C-/> <C-\><C-n>:q!<CR>

```

### 插件使用
![[最强Vim新手指南#02插件下载]]
![[最强Vim新手指南#03插件配置-NERDTree]]




