# 安装
```
brew cask install docker
Docker->Perferences...->Daemon->Registry mirrors->http://hub-mirror.c.163.com # 设置代理
docker info # 查看代理是否设置成功
```
# 常用命令
```Bash
docker images # 查看本地镜像
docker search $name # 搜索镜像
docker pull $repo[:$tag] # 下载镜像
docker commit -m="$desc" -a="$auther" $conId $name:$tag # 创建新镜像
docker tag $imageId $name:$tag # 添加新标签
docker run -it $name[:$tag] $cmd(/bin/bash) # 创建并运行容器
    # -i 保持标准输入打开
    # -t 分配一个伪终端
    # -P 通过NAT机制将容器标记暴露的端口自动映射到本地主机的临时端口
    # -p [127.0.0.1:]$port:5000[/tcp] 指定端口映射
docker ps # 查看运行中的容器
    # -a 查看所有容器
```
