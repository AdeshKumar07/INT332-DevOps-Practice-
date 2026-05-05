# Unit I Docker Commands

## General
| Command | Purpose |
|---|---|
| `docker --help` | Show Docker help and command list |
| `docker version` | Display Docker client and server versions |
| `docker info` | Show detailed Docker system information |

## Authentication and Registry
| Command | Purpose |
|---|---|
| `docker login [registry]` | Sign in to a Docker registry |
| `docker logout [registry]` | Sign out from a Docker registry |
| `docker search <term>` | Search for images in a registry |
| `docker pull <image>[:tag]` | Download an image from a registry |
| `docker push <image>[:tag]` | Upload an image to a registry |

## Images
| Command | Purpose |
|---|---|
| `docker images` | List local images |
| `docker image ls` | List local images |
| `docker image inspect <image>` | Show detailed image metadata |
| `docker image history <image>` | Show image layer history |
| `docker build -t <name>:<tag> <path>` | Build an image from a Dockerfile |
| `docker image tag <source> <target>` | Add a new tag to an image |
| `docker image rm <image>` | Remove a local image |
| `docker image prune` | Remove unused image layers |
| `docker save -o <file.tar> <image>` | Save an image as a tar archive |
| `docker load -i <file.tar>` | Load an image from a tar archive |

## Containers
| Command | Purpose |
|---|---|
| `docker ps` | List running containers |
| `docker ps -a` | List all containers |
| `docker run [options] <image> [command]` | Create and start a container |
| `docker start <container>` | Start a stopped container |
| `docker stop <container>` | Stop a running container |
| `docker restart <container>` | Restart a container |
| `docker kill <container>` | Force stop a container |
| `docker rm <container>` | Remove a container |
| `docker exec -it <container> <command>` | Run a command inside a running container |
| `docker logs <container>` | View container logs |
| `docker attach <container>` | Attach to a running container |
| `docker inspect <container>` | Show detailed container metadata |
| `docker stats` | View live container resource usage |
| `docker top <container>` | View processes running inside a container |
| `docker wait <container>` | Wait until a container stops |
| `docker pause <container>` | Pause container processes |
| `docker unpause <container>` | Resume a paused container |
| `docker rename <old> <new>` | Rename a container |
| `docker cp <container>:<path> <host_path>` | Copy files from container to host |
| `docker cp <host_path> <container>:<path>` | Copy files from host to container |
| `docker commit <container> <image>:<tag>` | Create an image from a container |
| `docker update --cpus <n> --memory <size> <container>` | Update container resource limits |
| `docker export -o <file.tar> <container>` | Export container filesystem to tar |
| `docker import <file.tar> <image>:<tag>` | Import a tar archive as an image |

## Networking
| Command | Purpose |
|---|---|
| `docker network ls` | List Docker networks |
| `docker network create <network>` | Create a network |
| `docker network inspect <network>` | Show network details |
| `docker network connect <network> <container>` | Connect a container to a network |
| `docker network disconnect <network> <container>` | Disconnect a container from a network |
| `docker network rm <network>` | Remove a network |
| `docker network prune` | Remove unused networks |

## Volumes and Storage
| Command | Purpose |
|---|---|
| `docker volume ls` | List Docker volumes |
| `docker volume create <volume>` | Create a volume |
| `docker volume inspect <volume>` | Show volume details |
| `docker volume rm <volume>` | Remove a volume |
| `docker volume prune` | Remove unused volumes |
| `docker run -v <volume>:/container/path <image>` | Mount a named volume into a container |
| `docker run -v /host/path:/container/path <image>` | Mount a host folder into a container |

## System and Cleanup
| Command | Purpose |
|---|---|
| `docker system df` | Show Docker disk usage |
| `docker system prune` | Remove unused Docker objects |
| `docker system events` | Show Docker events in real time |

## Common Examples
| Command | Purpose |
|---|---|
| `docker run --name web -p 8080:80 nginx:latest` | Run Nginx and expose port 80 on host port 8080 |
| `docker run -it --rm alpine:latest sh` | Start a temporary interactive Alpine shell |
| `docker run -d --name api --cpus 1 --memory 512m myapp:1.0` | Run an app in detached mode with resource limits |
