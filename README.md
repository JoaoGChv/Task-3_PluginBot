# Repositório de Capacitação em Robótica e Docker
df
Este repositório contém os ambientes de desenvolvimento Docker para simulação dos robôs TurtleBot3 e TurtleBot4, desenvolvidos durante a capacitação de robótica.

## Estrutura
- `/turtlebot3`: Contém Dockerfile e Compose para rodar o TB3 no Gazebo Clássico.
- `/turtlebot4`: Contém Dockerfile para rodar o TB4.

## Como Executar

### 1. TurtleBot3 (Task Anterior)
Para rodar o ambiente do TurtleBot3:

```bash
cd turtlebot3
# Permitir gráfico
xhost +local:root
# Subir o container
docker compose up -d --build
# Entrar no container
docker exec -it ros2_humble_dev bash
# Rodar simulação (dentro do container)
export TURTLEBOT3_MODEL=burger
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
