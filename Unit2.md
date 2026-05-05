# Unit 2 Docker Commands

## Basic
| Command | Purpose |
|---|---|
| `docker version` | Show Docker client and server versions |
| `docker info` | Show detailed Docker system information |
| `docker help` | Display Docker help |

## Containers
| Command | Purpose |
|---|---|
| `docker run nginx` | Run an Nginx container |
| `docker run -it ubuntu bash` | Start an interactive Ubuntu shell |
| `docker run -d nginx` | Run a container in detached mode |
| `docker run -p 8080:80 nginx` | Map host port 8080 to container port 80 |
| `docker run --name mycontainer nginx` | Run a container with a custom name |
| `docker run -m 512m nginx` | Limit container memory to 512 MB |
| `docker run --cpus="1.5" nginx` | Limit container CPU usage |
| `docker ps` | List running containers |
| `docker ps -a` | List all containers |
| `docker stop <container_id>` | Stop a running container |
| `docker start <container_id>` | Start a stopped container |
| `docker restart <container_id>` | Restart a container |
| `docker kill <container_id>` | Force stop a container |
| `docker rm <container_id>` | Remove a container |
| `docker exec -it <container_id> bash` | Open a shell inside a running container |
| `docker logs <container_id>` | View container logs |

## Images
| Command | Purpose |
|---|---|
| `docker images` | List local images |
| `docker pull nginx` | Download the Nginx image |
| `docker push username/image` | Upload an image to a registry |
| `docker rmi <image_id>` | Remove a local image |
| `docker build -t myapp:1.0 .` | Build an image from the current directory |
| `docker tag myapp:1.0 myapp:latest` | Add a new tag to an image |
| `docker inspect <image_id>` | View detailed image information |
| `docker history <image_name>` | View image layer history |
| `docker build -t myimage .` | Build an image from a Dockerfile |

## Networking
| Command | Purpose |
|---|---|
| `docker network ls` | List Docker networks |
| `docker network create mynet` | Create a network named mynet |
| `docker network inspect mynet` | Show network details |
| `docker network rm mynet` | Remove a network |
| `docker run -d --network=mynet nginx` | Run a container on a custom network |
| `docker run --network host nginx` | Use the host network stack |
| `docker run -p 8080:80 nginx` | Publish container port 80 on host port 8080 |

## Volumes and Storage
| Command | Purpose |
|---|---|
| `docker volume ls` | List volumes |
| `docker volume create myvol` | Create a named volume |
| `docker volume inspect myvol` | Show volume details |
| `docker volume rm myvol` | Remove a volume |
| `docker run -v myvol:/data nginx` | Mount a named volume into a container |
| `docker run -v /host/path:/container/path nginx` | Mount a host directory into a container |

## Registry
| Command | Purpose |
|---|---|
| `docker login` | Sign in to a registry |
| `docker logout` | Sign out from a registry |
| `docker pull nginx` | Download an image from a registry |
| `docker push username/image` | Upload an image to a registry |

## Daemon and Service
| Command | Purpose |
|---|---|
| `systemctl start docker` | Start the Docker service on Linux |
| `systemctl stop docker` | Stop the Docker service on Linux |
| `systemctl restart docker` | Restart the Docker service on Linux |
| `systemctl status docker` | Check Docker service status on Linux |
