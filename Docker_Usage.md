# Docker_Usage



## 1.show images in docker 展示docker里的镜像

```bash
nvidia-docker images
```



## 2.load local images 加载本地镜像到docker

```bash
nvidia-docker load --input [local_image.tar]
```



## 3.change images tag 修改镜像的仓库名

```bash
nvidia-docker image tag [image_id] [new_repository_name]：[tag]
```



## 4.run image 运行镜像

```bash
nvidia-docker run -i -t [new_repository_name] /bin/bash
```



## 5.load path in host 运行时做路径文件夹挂载

```bash
nvidia-docker run -it --shm-size 12G -v [host_folder_path]:[docker_folder_path]  image_name /bin/bash

-v

[host_folder_path]:宿主机的文件夹绝对路径

[docker_folder_path]:docker里的文件夹绝度路径
```



## 6.copy files 复制文件

```bash
sudo nvidia-docker cp [tag_id]:[src_path] [des_path]

sudo nvidia-docker cp [src_path] [tag_id]:[des_path]
```



## 7.将修改镜像后保存

```bash
nvidia-docker commit [tag_id] [new_name]:[tag]

[tag] 不写 即为latest
```



## 8.save image to local 保存镜像到本地

```bash
nvidia-docker save -o [file_name.tar] [image_name]

[file_name.tar]:保存的文件名 以tar格式结尾

[image_name]:要保存的镜像名
```

