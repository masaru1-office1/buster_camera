# buster_camera

## This project uses buster with desktop as host os and buster as container image.

1. Add permission to container

https://raspberrypi.stackexchange.com/questions/101462/camera-access-in-docker-container-is-generating-errors-locking

2. While a process is using camera module, other process seems not to use camera.

   To delete RPi_Cam_Web_Interface process,
```
sudo pkill -U www-data
```

Necessary Commands

copy this project into /home/pi/ by
```
git clone https://github.com/masaru1-office1/buster_camera.git
```
Then start docker
```
docker-compose up -d --build
docker exec -it containerID bash
```
In the container in RPi_Cam_Web_Interface folder
```
./install.sh
```
access to localhost:8080 on browser
