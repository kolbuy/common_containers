# Run Common Containers
需要安装有docker，如本机没有安装请转到[https://github.com/kolbuy/common_containers/blob/master/Install_Docker.md](https://github.com/kolbuy/common_containers/blob/master/Install_Docker.md)

	git clone https://github.com/kolbuy/common_containers.git
	cd common_containers
	docker-compose up -d

## start containers

	cd common_containers
	docker-compose up -d

## stop containers

	cd common_containers
	docker-compose stop


## remove containers

	cd common_containers
	docker-compose down

# access common containers

如是Windows10，需要在settings中`Network`选项卡，勾选上`Expose container ports on localhost`，并应用生效。否则端口不会映射到本机。

## mysql

default port : `3306`

default user : `root`

devault password : `Aa123456`

## rabbitmq

url: [http://127.0.0.1:15672/](http://127.0.0.1:15672/)

default user : `dev`

devault password : `Aa123456`

## redis

default port : `6379`