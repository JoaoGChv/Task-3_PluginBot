# Dockerfile para TurtleBot4 Simulation
FROM osrf/ros:humble-desktop-full

ENV DEBIAN_FRONTEND=noninteractive
ENV ROS_DISTRO=humble

# Instalação dos pacotes de simulação do TurtleBot4 e Ignition Gazebo
RUN apt-get update && apt-get install -y \
    ros-humble-turtlebot4-simulator \
    ros-humble-turtlebot4-desktop \
    ros-humble-irobot-create-nodes \
    wget \
    git \
    nano \
    && rm -rf /var/lib/apt/lists/*

# Configuração do ambiente
RUN echo "source /opt/ros/humble/setup.bash" >> /root/.bashrc

# Workspace setup
WORKDIR /root/workspace

CMD ["/bin/bash"]
