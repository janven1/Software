---
date_create: 2025-11-15-星期六
type: Software
status: unstarted
source:
---
## 00目录
| 序号  |                                                                           课程                                                                            | 评价  |
| :-: | :-----------------------------------------------------------------------------------------------------------------------------------------------------: | :-: |
| 01  |                                                   [课程简介](https://www.bilibili.com/video/BV14s4y1i7Vf)                                                   |     |
| 02  |                        [02.Docker简介](https://www.bilibili.com/video/BV14s4y1i7Vf?vd_source=aef73766b941d8e52cb9a97d24ea42a2&p=2)                        |     |
| 03  |                     [03.Docker和虚拟机的区别](https://www.bilibili.com/video/BV14s4y1i7Vf?vd_source=aef73766b941d8e52cb9a97d24ea42a2&p=3)                      |     |
| 04  |     [04.基本原理和概念](https://www.bilibili.com/video/BV14s4y1i7Vf?vd_source=aef73766b941d8e52cb9a97d24ea42a2&spm_id_from=333.788.videopod.sections&p=4)      |     |
| 05  |       [05.安装配置](https://www.bilibili.com/video/BV14s4y1i7Vf?vd_source=aef73766b941d8e52cb9a97d24ea42a2&spm_id_from=333.788.videopod.sections&p=5)       |     |
| 06  |  [06.容器化和Dockerfile](https://www.bilibili.com/video/BV14s4y1i7Vf?vd_source=aef73766b941d8e52cb9a97d24ea42a2&spm_id_from=333.788.videopod.sections&p=6)  |     |
| 07  |       [07.实践环节](https://www.bilibili.com/video/BV14s4y1i7Vf?vd_source=aef73766b941d8e52cb9a97d24ea42a2&spm_id_from=333.788.videopod.sections&p=7)       |  ⏳  |
| 08  | [08.DockerDesktop的使用](https://www.bilibili.com/video/BV14s4y1i7Vf?vd_source=aef73766b941d8e52cb9a97d24ea42a2&spm_id_from=333.788.videopod.sections&p=8) |     |
| 09  | [09.DockerCompose简介](https://www.bilibili.com/video/BV14s4y1i7Vf?vd_source=aef73766b941d8e52cb9a97d24ea42a2&spm_id_from=333.788.videopod.sections&p=9)  |     |
|     |                                                                                                                                                         |     |
|     |                                                                                                                                                         |     |
## 01课程简介

| 序号  |                                                     文件                                                      | 介绍                                                    | 评价  |
| :-: | :---------------------------------------------------------------------------------------------------------: | ----------------------------------------------------- | :-: |
| 01  | [Docker针对问题](https://www.bilibili.com/video/BV14s4y1i7Vf/?t=0.0&vd_source=aef73766b941d8e52cb9a97d24ea42a2) | 1、应用程序的部署和环境配置复杂花费时间长<br>2、开发环境和测试以及生产环境应用不匹配         |     |
| 02  |                        [课程学习收获](https://www.bilibili.com/video/BV14s4y1i7Vf?t=41.8)                         | 基本概念；安装配置；常用命令；<br>构建镜像；运行容器；DockerCompose&Kubernetes |     |
## 02Docker简介

| 序号  |                                   文件                                    | 介绍                                                                                               | 评价  |
| :-: | :---------------------------------------------------------------------: | ------------------------------------------------------------------------------------------------ | :-: |
| 01  |    [Docker简介](https://www.bilibili.com/video/BV14s4y1i7Vf?t=4.1&p=2)    | Docker是一个用于构建build、运行run、传送share应用程序的平台；<br>将应用程序和它运行时所需要的各种依赖包、第三方软件库、配置文件等打包在一起，以便在任何环境中都能正常运行 |     |
| 02  | [为什么要使用Docker?](https://www.bilibili.com/video/BV14s4y1i7Vf?t=41.9&p=2) | 略                                                                                                |     |
## 03Docker和虚拟机的区别
| 序号  |                                   内容                                    | 介绍                                                                                                                                                                                                                                                                                                                               | 评价  |
| :-: | :---------------------------------------------------------------------: | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-: |
| 01  |      [虚拟机](https://www.bilibili.com/video/BV14s4y1i7Vf?t=11.6&p=3)      | 常见虚拟机软件：<br>vmware、Virtalbox、ParallelsDesktop、wsl和Hyper-V<br>虚拟化(Hypervisor)技术是一种将物理资源虚拟为多个逻辑资源的技术，它可以将一台物理服务器虚拟成多个逻辑服务器，每个逻辑服务器都有自己的操作系统、CPU、内存、硬盘和网络接口，完全隔离可以独立运行；<br>虚拟机在一定程度上实现了资源的整合，可以将一台服务器的计算/存储能力和网络资源分配给多个逻辑服务器，实现多台服务器的功能；<br>缺点是占用大量资源，启动速度慢（通常需要几分钟甚至几十分钟）<br>大部分情况下，我们一台服务器只需要运行一个主要对外提供服务的应用程序就可以了，并不需要操作系统提供所有功能 |     |
| 02  | [Docker和容器的区别](https://www.bilibili.com/video/BV14s4y1i7Vf?t=119.6&p=3) | Docker是容器的一种实现，是一个容器化的解决方案和平台；<br>而容器是一种虚拟化技术，和虚拟机类似，是一个独立的环境，能够运行应用程序；                                                                                                                                                                                                                                                          |     |
| 03  |  [容器和虚拟机的区别](https://www.bilibili.com/video/BV14s4y1i7Vf?t=140.4&p=3)   | 应用程序并不需要在容器中运行一个完整的操作系统，而是使用宿主机的操作系统；启动速度快，通常只需要几秒钟，资源使用少，一台服务器可以使用更多容器，减少资源的浪费                                                                                                                                                                                                                                                  |     |
|     |                                                                         |                                                                                                                                                                                                                                                                                                                                  |     |
## 04基本原理和概念
| 序号  |                                 内容                                  | 介绍                                                                                                                                                                 | 评价  |
| :-: | :-----------------------------------------------------------------: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :-: |
| 01  | [Docker重要概念](https://www.bilibili.com/video/BV14s4y1i7Vf?t=4.1&p=4) | 镜像、容器和仓库                                                                                                                                                           |     |
| 02  |   [镜像与容器](https://www.bilibili.com/video/BV14s4y1i7Vf?t=29.2&p=4)   | 镜像是一个只读的模板，它可以用来创建容器<br>容器是Docker的运行实例，它提供了一个独立的可移植的环境，可以在这个环境中运行应用程序<br>镜像与容器类似 类与实例之间的关系                                                                         |     |
| 03  |    [仓库](https://www.bilibili.com/video/BV14s4y1i7Vf?t=113.4&p=4)    | 镜像如何分享？<br>Docker仓库是用来存储Docker镜像的地方，<br>最流行和最常用的仓库就是Dockerhub，它是一个公共的Docker仓库，用来集中存储和管理Docker镜像，我们可以在这里下载各种镜像，也可以将自己的镜像上传到这里，这样就可以实现镜像的共享和复用，这也是Docker非常流行的一个重要原因。 |     |
## 05安装配置
| 序号  |                                         内容                                         | 介绍                                                                                                                                                                                                                                                                                                                                                                             | 评价  |
| :-: | :--------------------------------------------------------------------------------: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :-: |
| 01  |         [Docker的安装](https://www.bilibili.com/video/BV14s4y1i7Vf?t=4.0&p=5)         | [Docker官网](https://www.docker.com/)<br>安装完成后，需要启动Docker，否则后续操作无法进行<br>Docker启用之后可以在右上角菜单栏看见小鲸鱼图标                                                                                                                                                                                                                                                                               |     |
| 02  |   [Windows系统还需启用Hyper-V](https://www.bilibili.com/video/BV14s4y1i7Vf?t=42.8&p=5)   | 使用`win+R`输入`optionalfeatures`，启用`Hyper-V`后根据系统提示重启电脑                                                                                                                                                                                                                                                                                                                           |     |
| 03  |        [检查docker安装](https://www.bilibili.com/video/BV14s4y1i7Vf?t=60.7&p=5)        | `docker version`能够看到Docker版本信息就说明安装成功<br>如果只能看到Client就说明Docker没有启动                                                                                                                                                                                                                                                                                                             |     |
| 04  | [Docker的Client-Server架构模式](https://www.bilibili.com/video/BV14s4y1i7Vf?t=83.5&p=5) | Docker是使用Client-Server架构模式，Docker Client和Docker Daemon之间，通过Socket或者RESTful API进行通信；<br>**Docker Daemon**就是服务端的守护进程，他负责管理Docker的各种资源<br>**Docker Client**负责向Docker Daemon发送请求，Docker Daemon接收到请求之后进行处理，然后将结果返回给Docker Client；这里的Docker Daemon是一个后台进程，用来接收并处理来自Docker客户端的请求，然后将结果返回给客户端<br>所以我们在终端中输入的各种Dockert命令，实际上都是通过Docker客户端发送给Docker Daemon的，然后等待其处理后返回结果到客户端，然后再终端查看执行结果 |     |
## 06容器化和Dockerfile
| 序号  |                                   内容                                   | 介绍                                                                                                                                                                                                                                             | 评价  |
| :-: | :--------------------------------------------------------------------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-: |
| 01  |      [容器化](https://www.bilibili.com/video/BV14s4y1i7Vf?t=4.9&p=6)      | 容器化(containerization)顾名思义就是将应用程序打包成容器，<br>然后在容器中运行应用程序的过程                                                                                                                                                                                      |     |
| 02  |   [容器化具体过程](https://www.bilibili.com/video/BV14s4y1i7Vf?t=11.8&p=6)    | 1.创建一个Dockerfile，来告诉Docker构建应用程序镜像所需要的步骤和配置<br>2.使用Dockerfile来构建镜像<br>3.使用镜像创建和运行容器                                                                                                                                                            |     |
| 03  |  [Dockerfile](https://www.bilibili.com/video/BV14s4y1i7Vf?t=30.7&p=6)  | Dockerfile是一个文本文件，里面包含了一条条的指令，用来告诉Docker如何来构建镜像，这个镜像包括我们应用程序执行的所有命令，也就是各种依赖、配置环境和运行应用程序所需要的所有内容；<br>**一般说来包括以下内容**：<br>精简版的操作系统，比如Alpine<br>应用程序的运行时环境，比如NodeJS Java Python<br>应用程序，比如SpringBoot打包好的jar包<br>应用程序的第三方依赖库或者包<br>应用程序的配置文件、环境变量等等 |     |
| 04  | [Dockerfile规范](https://www.bilibili.com/video/BV14s4y1i7Vf?t=68.2&p=6) | 一般来说，我们会在项目的根目录下创建一个叫Dockerfilel的文件，第一个字母D大写其他都小写，在这个文件中写入构建镜像所需要的各种指令之后，Docker就会根据这个Dockerfile文件来构建一个镜像，有了镜像就可以创建容器从而运行程序                                                                                                                     |     |
## 07实践环节
| 序号  |                                      内容                                      | 介绍                                                                                                        | 评价  |
| :-: | :--------------------------------------------------------------------------: | --------------------------------------------------------------------------------------------------------- | :-: |
| 01  |        [实践内容](https://www.bilibili.com/video/BV14s4y1i7Vf?t=7.7&p=7)         | 实践包括：编写Dockerfile、创建镜像、启动容器                                                                               |     |
| 02  |   [创建问价夹并使用编辑器打开](https://www.bilibili.com/video/BV14s4y1i7Vf?t=14.8&p=7)    |                                                                                                           |     |
| 03  |    [创建index.js文件](https://www.bilibili.com/video/BV14s4y1i7Vf?t=47.7&p=7)    | 输入代码`console.log("string")`<br>这段代码会在控制台中输出括号里面的内容<br>终端执行输入 `node filename`                              |     |
| 04  |      [NodeJS介绍](https://www.bilibili.com/video/BV14s4y1i7Vf?t=80.6&p=7)      | NodeJs是一个运行时环境，它可以让我们在浏览器之外的地方，运行JavaScript的代码<br>NodeJS和JavaScript的关系，就像Java和JRE的关系一样，如果想运行Java程序需要安装JRE |     |
| 05  |   [另一个环境运用程序的步骤](https://www.bilibili.com/video/BV14s4y1i7Vf?t=105.0&p=7)    | 1.安装操作系统；2.安装代码运行环境；3.复制应用程序、依赖包、配置文件；4.执行启动命令运行程序；<br>将这些步骤写入Dockerfile中，交给Docker自动完成                    |     |
| 06  | [安装VSCode扩展-Docker](https://www.bilibili.com/video/BV14s4y1i7Vf?t=174.8&p=7) |                                                                                                           |     |
| 07  |  [操作-编写Dockerfile](https://www.bilibili.com/video/BV14s4y1i7Vf?t=188.0&p=7)  | 详情见下方                                                                                                     |     |
| 08  |      [命令-创建镜像](https://www.bilibili.com/video/BV14s4y1i7Vf?t=308.4&p=7)      |                                                                                                           |     |
| 09  |     [提问-镜像文件位置](https://www.bilibili.com/video/BV14s4y1i7Vf?t=336.3&p=7)     | Docker镜像的存储暂不展开                                                                                           |     |
| 10  |   [查看构建的Docker镜像](https://www.bilibili.com/video/BV14s4y1i7Vf?t=349.6&p=7)   | 使用到的Docker命令如下<br>并对显示的信息做出解释并补充命令细节                                                                      |     |
| 11  |      [命令-运行程序](https://www.bilibili.com/video/BV14s4y1i7Vf?t=377.2&p=7)      | `docker run <image_name>`                                                                                 |     |
| 12  |                                                                              |                                                                                                           |     |
| 13  |                                                                              |                                                                                                           |     |
| 14  |                                                                              |                                                                                                           |     |
|     |                                                                              |                                                                                                           |     |
### 07编写Dockerfile
镜像是按层次结构来构建的，每一层都是基于上一层的；
要先指定一个基础镜像，然后在这个镜像上添加我们的应用程序；

从一个最基础的Linux镜像开始，然后在这个镜像上安装NodeJS和我们的程序或者直接使用NodeJS的镜像

```dockerfile
FROM node:14-alpine 
# node后面的14表示NodeJS的版本
# "-alpine"表示这个镜像是基于lpine这个Linux发行版来构建的
# Alpine和其他我们经常听说的RedHat CentoS一样是Linux发行版，不过它非常轻量级体积非常小只有几十MB，下载部署非常快
```
配置完运行环境之后，还需要把我们的应用程序复制到镜像中，可以使用COPY命令来复制文件

```dockerfile
COPY index.js /index.js
```
 COPY命令后面可以加上两个参数，第一个参数表示源路径，第二个参数表示目标路径
这里的源路径是指相对于Dockerfile文件的路径，目标路径是相对于镜像的路径

然后我们需要在镜像中运行应用程序，可以使用CMD命令来运行应用程序
CMD命令后面可以加上一对方括号，
方括号的第一个参数表示可执行程序的名字，
第二个参数以后表示这个可执行程序接收到的参数

```dockerfile
CMD [ "node", "/index.js" ]
CMD node /index.js
```
两种格式，建议第一种；
### 08创建镜像
```docker
docker build -t <image_name> .
```
### 10查看已构建的Docker镜像
```docker
docker images
docker image ls
```
- 查看我们所有的镜像

| 序号  | 标题  | 介绍       |                               含义                                | 评价  |
| :-: | :-: | -------- | :-------------------------------------------------------------: | :-: |
| 01  | TAG | `Latest` | 镜像标签，也就是镜像版本，如果不指定版本，默认为`latest`<br>如果想要指定版本，就需要在镜像名字后面加上冒号和版本号 |     |












## 99其他知识
- [ ] 2025-11-15 19:01: NodeJS、npm、Vue、Redis、Nginx



