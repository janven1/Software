---
date_create: 2025-11-05-星期三
type: Software
status: unstarted
source:
---
| 序号  |                                  内容                                  | 介绍                                                                                                                                                                                                 | 评价  |
| :-: | :------------------------------------------------------------------: | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-: |
| 01  |     [00背景介绍](https://www.bilibili.com/video/BV1tW42197za?t=0.0)      | 双系统互相使用各自命令；<br>docker以及显卡直通<br>WindowsSubsystemForLinux                                                                                                                                           |     |
| 02  |   [00wsl1/2原理](https://www.bilibili.com/video/BV1tW42197za?t=23.7)   |                                                                                                                                                                                                    |     |
| 03  |                              01wsl使用前提                               | 两个前提：<br>1.CPU虚拟化2.                                                                                                                                                                                |     |
| 04  |    [CUP虚拟化](https://www.bilibili.com/video/BV1tW42197za?t=103.5)     |                                                                                                                                                                                                    |     |
| 05  | [开启2个Windows功能](https://www.bilibili.com/video/BV1tW42197za?t=129.0) |                                                                                                                                                                                                    |     |
| 06  |     [02安装](https://www.bilibili.com/video/BV1tW42197za?t=145.2)      |                                                                                                                                                                                                    |     |
| 07  | [02.01其他发行版本下载](https://www.bilibili.com/video/BV1tW42197za?t=189.8) | `wsl --list --online`展示所有的可安装的发行版<br>`wsl --install <subsystem_name> --web-download`<br>安装其他发行版                                                                                                    |     |
| 08  |     [启动停止](https://www.bilibili.com/video/BV1tW42197za?t=216.7)      | `wsl --list -v`显示机器上安装的Linux子系统列表；<br>`wsl --set -default <subsystem_name>`<br>`wsl --list -v`查看Linux发行版状态<br>下拉点击对应的Linux发行版即可；<br>老版的cmd输入命令`wsl -d <subsystem_name>`<br>退出使用 `exit`             |     |
| 09  |    [03卸载和备份](https://www.bilibili.com/video/BV1tW42197za?t=305.0)    | `wsl --unregister <subsystem_name>`卸载发行版<br>`wsl --export <subsystem_name> <file_name>.tar`备份发行版<br>导入发行版：首先终端进入进入到安装的目录，<br>使用命令`wsl --import <subsystem_name> <install_path> <export_file_path>` |     |
| 10  |  [wsl2的本质补充说明](https://www.bilibili.com/video/BV1tW42197za?t=372.6)  | 导入备份文件后显示的是`Hyperv`镜像文件，<br>wsl中的Linux子系统的一切文件都存在这个镜像文件里面；                                                                                                                                         |     |
| 11  |    [04文件共享](https://www.bilibili.com/video/BV1tW42197za?t=389.2)     | 待整理                                                                                                                                                                                                |  ⏳  |
| 12  |     [WSLg](https://www.bilibili.com/video/BV1tW42197za?t=537.5)      |                                                                                                                                                                                                    |  ⏳  |
| 13  |                                  ⏳                                   |                                                                                                                                                                                                    |     |
| 14  |                                                                      |                                                                                                                                                                                                    |     |



