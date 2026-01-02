FROM osrf/ros:humble-desktop-full

ENV DEBIAN_FRONTEND=noninteractive
ENV ROS_DISTRO=humble

RUN apt-get update && apt-get install -y \
    nano \
    vim \
    git \
    curl \
    wget \
    build-essential \
    python3-pip \
    ros-humble-turtlesim \
    ros-humble-rviz2 \
    ros-humble-gazebo-ros \
    gazebo \
    xauth && \
    rm -rf /var/lib/apt/lists/*

RUN echo "source /opt/ros/humble/setup.bash" >> /root/.bashrc

WORKDIR /root/workspace

CMD ["/bin/bash"]
