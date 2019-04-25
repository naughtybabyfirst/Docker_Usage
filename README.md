# Docker_Usage

## show images docker里的镜像

docker images

## load local images 加载本地镜像到docker

docker load --input local_image.tar

## change images tag 修改镜像的仓库名

docker image tag image_id new_repository_name：tag

## run image 运行镜像

docker run -i -t new_repository_name /bin/bash

## cp 复制文件

sudo nvidia-docker cp tag_id:src_path des_path

sudo nvidia-docker cp src_path tag_id:des_path

## 修改镜像后保存

nvidia-docker commit tag_id new_nam
