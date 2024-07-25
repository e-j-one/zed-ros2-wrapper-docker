# zed-ros2-wrapper-docker
Dockerfiles for zed-ros2-wrapper on Jetpack 6 (L4T R36.3)

- This image builds from [stereolabs/zed:4.1-tools-devel-l4t-r36.3](https://hub.docker.com/r/stereolabs/zed) and clones and builds [zed-ros2-wrapper](https://github.com/stereolabs/zed-ros2-wrapper).

## How to run
```bash
# Run docker container
docker run -it --rm --runtime nvidia --privileged -e DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix ejone/zed:4.1-runtime-l4t-r36.3
# Run zed node inside the container
ros2 launch zed_wrapper zed_camera.launch.py camera_model:=<camera model>
# ex
ros2 launch zed_wrapper zed_camera.launch.py camera_model:=zed2i
```