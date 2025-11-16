---
date_create: 2025-11-15-星期六
type: Software
status: unstarted
source: video
---
# 00课程

| 序号  |                                                                       链接                                                                        | 评价  | 状态  |                       优势                        |              缺陷               |
| :-: | :---------------------------------------------------------------------------------------------------------------------------------------------: | :-: | :-: | :---------------------------------------------: | :---------------------------: |
| 01  |                                            [Docker实战攻略](https://www.bilibili.com/video/BV1THKyzBER6)                                            |     |     |                                                 |                               |
| 02  | [Docker入门教程](https://www.bilibili.com/video/BV14s4y1i7Vf/?spm_id_from=333.337.search-card.all.click&vd_source=aef73766b941d8e52cb9a97d24ea42a2) |     |  ✅  | 动画清晰易懂地介绍了Docker中的重要概念<br>基本清晰地了解到Docker使用的常见功能 | 缺乏实际的项目实践，<br>并不利于直接的docker使用 |
| 03  |                                       [2025国内10个高速docker镜像源](https://www.bilibili.com/video/BV17CRXYdEij)                                       |     | ✏️  |                                                 |                               |
| 04  |                                         [搭建docker私人专属镜像站](https://www.bilibili.com/video/BV1eYZQYsEpi)                                          |     |     |                                                 |                               |
| 05  |                   [技术爬爬虾-Docker实践支撑](https://www.bilibili.com/video/BV1vm421T7Kw/?vd_source=aef73766b941d8e52cb9a97d24ea42a2)                   | ⭐⭐⭐ |     |                                                 |                               |
| 06  |                                            [Pull, 找镜像](https://www.bilibili.com/video/BV1fS411A71Y)                                             |     |     |                                                 |                               |
# 00链接
| 序号  |                                  链接                                  |   评价   |
| :-: | :------------------------------------------------------------------: | :----: |
| 01  | [tech-srimp-Docker](https://github.com/tech-shrimp/docker_installer) |        |
| 02  |    [2025年国内可用docker镜像源](https://www.dhzy.fun/archives/6852.html)     |   ⭐⭐   |
| 03  |      [离线镜像源下载](https://github.com/wukongdaily/DockerTarBuilder)      |        |
| 04  |              [web-镜像查找](https://docker.fxxk.dedyn.io/)               | ❌好像失效了 |
### 02国内可用docker镜像源

- `docker-desktop->setting->Docker Engine`修改配置文件中“"registry-mirrors"的网站名

```
{
  "builder": {
    "gc": {
      "defaultKeepStorage": "20GB",
      "enabled": true
    }
  },
  "experimental": false,
  "registry-mirrors": [
    "https://docker.m.daocloud.io",
    "https://docker.1panel.live",
    "https://docker.1ms.run",
    "https://hub.rat.dev"
  ]
}
```

- docker.1ms.run
- docker.domys.cc
- docker.imgdb.de
- docker-0.unsee.tech
- docker.hlmirror.com
- cjie.eu.org
- docker.m.daocloud.io
- hub.rat.dev
- docker.1panel.live
- docker.rainbond.cc

# 01[[Docker实战攻略]]


# 02[[Docker入门教程]]


# 04
文字教程：https://www.dhzy.fun/archives/6861.html 
亚马逊云12月免费服务器：https://aws.amazon.com/cn/campaigns/ftpromotion/?trk=80796997-152a-4a92-b22b-b90f68cc8da0&sc_channel=sm 
crproxy开源地址：https://github.com/DaoCloud/crproxy
# 05Docker实践支撑
| 序号  |                                  内容                                   | 介绍                                                                                                                                                                                       | 评价  |
| :-: | :-------------------------------------------------------------------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-: |
| 00  | [tech-srimp-Docker](https://github.com/tech-shrimp/docker_installer)  | 文本教程                                                                                                                                                                                     | ⭐⭐⭐ |
| 01  |  [Linux安装Docker](https://www.bilibili.com/video/BV1vm421T7Kw?t=1.7)   |                                                                                                                                                                                          |     |
| 02  | [Windows安装Docker](https://www.bilibili.com/video/BV1vm421T7Kw?t=58.3) |                                                                                                                                                                                          |     |
| 03  | [macOS安装Docker](https://www.bilibili.com/video/BV1vm421T7Kw?t=134.5)  |                                                                                                                                                                                          |     |
| 04  |    [拉取镜像方案1](https://www.bilibili.com/video/BV1vm421T7Kw?t=156.9)     | 国外镜像转存到阿里云私有库，[国外镜像私有库项目](https://github.com/tech-shrimp/docker_image_pusher)<br>支持任意类型的仓库，可以支持40GB的大型镜像<br>使用的是阿里云官方线路，速度快<br>[06视频链接](https://www.bilibili.com/video/BV1fS411A71Y)<br> |     |
| 05  |    [拉取镜像方案2](https://www.bilibili.com/video/BV1vm421T7Kw?t=187.9)     | 配置镜像站；<br>详细介绍了Linux/Windows/macOS配置镜像站的操作【**略**】                                                                                                                                        |     |
| 06  |    [镜像拉取方案3](https://www.bilibili.com/video/BV1vm421T7Kw?t=241.7)     | 使用Github Action下载Docker离线镜像<br>[Github地址-离线镜像源头下载](https://github.com/wukongdaily/DockerTarBuilder)                                                                                      |     |
| 07  |    [镜像拉取方案4](https://www.bilibili.com/video/BV1vm421T7Kw?t=254.2)     | 使用一键脚本；**具体操作见视频**<br>这个脚本可以自动地测试各个docker镜像源的可用性，选择个最优的进行下载                                                                                                                              |     |
| 08  |    [镜像拉取方案5](https://www.bilibili.com/video/BV1vm421T7Kw?t=275.9)     | 使用cloudflare work自建镜像加速<br>[Github地址-加速方案](https://github.com/cmliu/CF-Workers-docker.io)                                                                                                |     |
| 09  |      [镜像查找](https://www.bilibili.com/video/BV1vm421T7Kw?t=286.1)      | [web-镜像查找](https://docker.fxxk.dedyn.io/)<br>使用操作详见视频                                                                                                                                    |     |
### 09镜像查找
- 2025-11-16 20:23: 但是实际上无法搜索







