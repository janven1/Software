---
date_create: 2025-10-08
---

### 基本递归查找（推荐）
- 基础
```powershell
ls *.log
```

- 查找当前目录包括子目录中的 `.log` 文件
```powershell
Get-ChildItem -Recurse -Filter "*.log"
```
### 删除文件夹
```powershell
# 删除空文件夹 
Remove-Item -Path "C:\path\to\folder"
# 递归删除非空文件夹（强制删除） 
Remove-Item -Path "C:\path\to\folder" -Recurse -Force
```
```powershell
Remove-Item  .ssh -Recurse -Force
```


```powershell

```

![[2.基础命令行代码#13-vi编辑器|Vim 基础]]
