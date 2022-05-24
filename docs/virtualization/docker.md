# Docker
* add user to `docker` group so it does not ask for sudo: `sudo usermod -aG docker $USER`
* build image: `docker build -t <image_name> .`
* tag image: `docker tag example_image:latest gauravvv/example_image:latest`
* push image: `docker push gauravvv/example_image:latest`
* check docker disk space usage: `docker system df`