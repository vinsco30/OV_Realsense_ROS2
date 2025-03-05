# Docker for OpenVins with Realsense and ROS2

Docker configuration with ROS2 Humble for OpenVins implementation with Realsense cameras. 

## Details

- **Auto-deletion: Temporary Suspended** After its execution, the Docker container is automatically deleted. This helps in maintaining a clean environment by freeing up resources on the host machine.

- **`ros2_ws-src` folder:** This folder should contain the source code for the ROS2 workspace. The Docker container comes pre-loaded with a custom version of `realsense-ros` package where the QoS of the output topics are already set as `BEST_EFFORT`.

- **`ROS_DOMAIN_ID`:** it is set by default as 69, you can change it in the dockerfile before building the image.

### Installing

A step by step series of git clone https://github.com/Prisma-Drone-Team/ov_republisher.gitexamples that tell you how to get a development environment running:

1. Clone the repository to your local machine.
2. Build the docker imagege with `cd docker && docker build -t ov-rs-ros2 -f ov_humble_rs_dockerfile.txt .`
3. Run the container with `./run_cnt.sh` (Auto-deletion removed temporary).

## OpenVins Republisher
Clone it in `ros2_ws-src/pkg/` from outside the container

    $ git clone https://github.com/Prisma-Drone-Team/ov_republisher.git $

### TODO: complete implementation

