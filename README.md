# buster_camera

## Using buster with desktop as host os.

Add permission to container

https://raspberrypi.stackexchange.com/questions/101462/camera-access-in-docker-container-is-generating-errors-locking

while a process is using camera module, other process seems not to use camera.

To delete RPi_Cam_Web_Interface process,

sudo pkill -U www-data

