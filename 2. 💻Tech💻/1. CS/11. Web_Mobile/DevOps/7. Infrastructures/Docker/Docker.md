# Images/Container
- docker images -a (show all images)
- docker images -q (only shows id)
- docker rmi id/name (remove image)
- docker run [OPTIONS] IMAGE [COMMAND] 
- dokcer ps (list running container)
- start/restart/stop/kill
- docker rm id/name


# DockerFile
FROM
	基础镜像，当前镜像是基于那个镜像
MAINTAINER
	镜像维护者的姓名和邮箱地址
RUN
	镜像构建时需要运行的命令
WORKDIR
	容器创建后，默认在那个目录
EXPOSE
	当前容器对外暴露的接口
ENV
	用来构建镜像时设置环境变量
ADD
	将宿主机目录下的文件copy到镜像且ADD命令会自动解压压缩包
COPY
VOLUME
	容器数据卷，用来保存和持久化
CMD
	指定容器启动时需要运行的命令
	多条CMD命令，只有最后一条生效
	CMD命令会被docker run之后的参数替换
ENTRYPOINT
	指定容器启动过程中需要运行的命令
	把docker run命令的参数追加到后面
ONBUILD