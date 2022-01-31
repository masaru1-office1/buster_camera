# buster_camera

## This project uses buster with desktop as host os and buster as container image.

Enable camera module by Raspberry Pi Configuration

docker install
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker pi
sudo pip3 install docker-compose
```

copy this project into /home/pi/ by
```
git clone --recursive https://github.com/masaru1-office1/buster_camera.git
```
Then start docker in buster_camera folder
```
docker-compose up -d --build
docker exec -it containerID bash
```
in RPi_Cam_Web_Interface folder in the container
```
./install.sh
```
access to http://localhost:8080 on browser


## If the web camera doesn't work

1. Add permission to container

https://raspberrypi.stackexchange.com/questions/101462/camera-access-in-docker-container-is-generating-errors-locking

2. While a process is using camera module, other process seems not to be able to use camera.

   if host OS is using RPi_Cam_Web_Interface process, delete the processes by
```
sudo pkill -U www-data
```
