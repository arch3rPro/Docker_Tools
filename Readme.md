# VulDocker -- Vulnerable Dockers For Study Pentest and Network Security

采用Dock的形式，搭建漏洞环境，用于记录分享渗透测试学习和代码审计

- 本项目有借鉴优秀项目Vulhub和VulAPP的地方，侵删~
- **容器中可能包含漏洞，强烈建议不要部署在生产环境**

Docker Hub链接[https://hub.docker.com/u/vuldocker/](https://hub.docker.com/u/vuldocker/)

## 使用文档

### Pull镜像

```
docker pull  vuldocker/xxxx
```
- xxxx 为需要pull的镜像名

**每个环境对应的详细使用方法我会写在该环境目录的Readme中**

###  启动容器

```
docker run -d -p 8080:80 --name abc  vuldocker/xxxx
```
-  -d   后台启动 ， -p 指定映射的端口   abc为指定容器名 
-  如果需要容器开机自启，可以加上 --restart always 选项
-  如果pull速度较慢，推荐使用 [中科大 Docker Mirrors](https://lug.ustc.edu.cn/wiki/mirrors/help/docker) 或者使用 [阿里云 Mirrors(加速器)](https://cr.console.aliyun.com/#/accelerator)

### 访问目标

访问 `http://a.b.c.d:8080/` 即可访问目标地址，开始学习相关漏洞了~
