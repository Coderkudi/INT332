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

    docker network ls (lists available docker networks)
    docker network inspect
    docker network rm <network_name>
    docker

# cleanup commands

    docker stop $(docker ps -aq) (stops all containers)
    docker rm $(docker ps -aq) (removes all containers)
    docker rmi $(docker images -q) (deletes all images)
    docker system prune -a (cleans unused containers, networks, images)

# run commands

    docker run httpd echo "Hello"
    docker run --name my-container httpd echo "Hello, World"

# setting env variables

    docker run -e MY_VAR=value httpd env  (it will open the container and you can check the env variable inside it as:- Echo $MY_NAME)

# setting multiple env variables

    docker run -e APP_ENV= production -e APP_Version=1.0 nginx
