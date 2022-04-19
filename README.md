# yocto-builder-u
基于docker ubuntu 20.04版本的 yocto 构建环境

## 1. 构建docker image
在当前目录执行：

> **./scripts/build.sh**

会创建名称为 **$USERNAME/yocto-u:latest** 的docker image  
例如：用户alice创建的默认image名称为 alice/yocto-u:latest

## 2. 安装脚本

构建完毕后，在当前目录执行：

> **FUNC_ALIAS=yocto ./scripts/install.sh [TargetPath]**

**TargetPath** 的默认值为： `${HOME}/.local`  
如不作修改，则生成的脚本为：`${HOME}/.local/docker_env/yocto_yocto-u_env`  

## 3. 使用方法
对于用户alice, 参考安装脚本提示：

<pre>First, exec:
    source /home/alice/.local/docker_env/yocto_yocto-u_env
Then, use:
    docker_yocto [arg1]...</pre>

执行完毕后，进入一个容器内的shell，可以开展yocto项目的构建工作

如需永久生效，可将
>source /home/alice/.local/docker_env/yocto_yocto-u_env

添加到${HOME}/.bashrc
