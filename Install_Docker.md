# install docker

官方文档 [https://www.docker.com/products/docker](https://www.docker.com/products/docker)

## windows

### windows 10或者之后的版本
下载并安装 [https://download.docker.com/win/beta/InstallDocker.msi](https://download.docker.com/win/beta/InstallDocker.msi)

1. 安装完毕后在右下角docker图标右键，选择`settings...`
2. 默认本地磁盘不可挂载到docker中，如有需要则在左侧选项卡点击`Shared Drives`,在右侧勾选上需要被挂载的磁盘，点击apply后等几分钟配置生效。
3. 默认docker端口不映射到本机端口，如果需要则在左侧选项卡选择`Network`，勾选上`Expose container ports on localhost`，点击apply后等几分钟配置生效。
4. 如果需要镜像加速，可以在左侧选项卡点击`Docker Daemon`，在的json中`registry-mirrors`节点中添加加速镜像的地址，点击apply后等几分钟配置生效。
5. 默认docker占用2核CPU，2G内存，如果需要调整则在左侧选项卡点击`Advanced`,在右侧调整CPU和memory，点击apply后等几分钟配置生效。


### 低于Windows 10
下载并安装 [https://github.com/docker/toolbox/releases/download/v1.11.1b/DockerToolbox-1.11.1b.exe](https://github.com/docker/toolbox/releases/download/v1.11.1b/DockerToolbox-1.11.1b.exe)

## mac

### Yosemite 10.10或者之后的版本
下载并安装 [https://download.docker.com/mac/beta/Docker.dmg](https://download.docker.com/mac/beta/Docker.dmg)

### 低于Yosemite 10.10版本
下载并安装 [https://github.com/docker/toolbox/releases/download/v1.10.3/DockerToolbox-1.10.3.pkg](https://github.com/docker/toolbox/releases/download/v1.10.3/DockerToolbox-1.10.3.pkg)

## centos

官方文档 [https://docs.docker.com/engine/installation/linux/centos/](https://docs.docker.com/engine/installation/linux/centos/)

	sudo yum -y update
	curl -fsSL https://get.docker.com/ | sh
	sudo service docker start

1. 用有sudo权限的用户登录或者使用root用户登录

2. 创建 `docker` 组

		sudo groupadd docker

3. 把你的用户添加到 `docker` 组

		sudo usermod -aG docker your_username

4. 登出并用你的用户名重新登录

	请确保使用正确的用户名登录

5. 验证你的用户名不使用sudo运行docker命令

		docker run hello-world

## ubuntu

官方文档 [https://docs.docker.com/engine/installation/linux/ubuntulinux/](https://docs.docker.com/engine/installation/linux/ubuntulinux/)
	
	sudo apt-get -y update
	sudo apt-get install -y linux-image-extra-$(uname -r)
	sudo apt-get install -y docker-engine
	sudo service docker start

1. 用有sudo权限的用户登录或者使用root用户登录

2. 创建 `docker` 组

		sudo groupadd docker

3. 把你的用户添加到 `docker` 组

		sudo usermod -aG docker your_username

4. 登出并用你的用户名重新登录

	请确保使用正确的用户名登录

5. 验证你的用户名不使用sudo运行docker命令

		docker run hello-world


# install docker-compose 

## windows

安装docker for windows 自带docker compose,无需另外安装



## mac os

	curl -L https://github.com/docker/compose/releases/download/1.8.0-rc1/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
	chmod +x /usr/local/bin/docker-compose

## centos

	rpm -iUvh http://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-7.noarch.rpm
	sudo yum -y update
	sudo yum install -y python-pip
	pip install docker-compose 

## ubuntu 

	sudo apt-get -y update
	sudo apt-get install -y python-pip
	pip install docker-compose 
