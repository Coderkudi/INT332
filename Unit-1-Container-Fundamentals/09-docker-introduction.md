# Docker Hub introduction

- Centralized repository for docker images
- Features:-
  Public and private repo
  official images
  automated builds
  importance in devops

# docker architecture

- Docker client
- Docker Daemon
- Docker images
- Containers
- Docker Registry (Docker Hub)

# Docker life cycle

- Build: Create an image
- Ship: share images via docker hub
- Run: Start containers

* Container States:
  - created
  - running
  - paused
  - stopped

docker pull ubuntu
docker images
docker run ubuntu
docker run -it ubuntu /bin/bash
docker stop<conatier_id>
docker rm <constainerid>
docker system prune -a
docker system prune -d volumes
