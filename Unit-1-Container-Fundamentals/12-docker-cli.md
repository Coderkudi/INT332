# docker container interaction commands

    docker exec -it <container_id> bash
    docker logs <container_id>
    docker inspect <container_id>
    docker run -dit --name myubuntu ubuntu
    docker start myubuntu

# volume commands

    docker volume create myvolume (creates a persistent storage volume)
    docker volume ls (lists all volumes)
    docker volume inspect myvolume (shows volume details)
    docker volume rm myvolume (removes the volume)

# network commands
