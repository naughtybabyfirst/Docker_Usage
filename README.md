# Docker_Usage

## load local images

docker load --input local_image.tar

## change images tag

docker image tag image_id new_repository_name

## run image

docker run -i -t new_repository_name /bin/bash

## cp

sudo nvidia-docker cp tag_id:src_path des_path

sudo nvidia-docker cp src_path tag_id:des_path


