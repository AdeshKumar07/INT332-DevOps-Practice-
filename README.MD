# 🐳 Docker Commands Cheat Sheet (Unit 1 + Unit 2)

## 🔹 Basic Commands

```bash
docker version
docker info
docker help
```

---

## 🔹 Container Commands

```bash
docker run nginx
docker run -it ubuntu bash
docker run -d nginx
docker run -p 8080:80 nginx
docker run --name mycontainer nginx
docker run -m 512m nginx
docker run --cpus="1.5" nginx
```

```bash
docker ps
docker ps -a
docker stop <container_id>
docker start <container_id>
docker restart <container_id>
docker kill <container_id>
docker rm <container_id>
docker exec -it <container_id> bash
docker logs <container_id>
```

---

## 🔹 Image Commands

```bash
docker images
docker pull nginx
docker push username/image
docker rmi <image_id>
docker build -t myapp:1.0 .
docker tag myapp:1.0 myapp:latest
docker inspect <image_id>
docker history <image_name>
```

---

## 🔹 Dockerfile Related

```bash
docker build -t myimage .
```

---

## 🔹 Networking Commands

```bash
docker network ls
docker network create mynet
docker network inspect mynet
docker network rm mynet
```

```bash
docker run -d --network=mynet nginx
docker run --network host nginx
docker run -p 8080:80 nginx
```

---

## 🔹 Volume & Storage

```bash
docker volume ls
docker volume create myvol
docker volume inspect myvol
docker volume rm myvol
```

```bash
docker run -v myvol:/data nginx
docker run -v /host/path:/container/path nginx
```

---

## 🔹 Registry Commands

```bash
docker login
docker logout
docker pull nginx
docker push username/image
```

---

## 🔹 Daemon Commands (Linux)

```bash
systemctl start docker
systemctl stop docker
systemctl restart docker
systemctl status docker
```

```bash
docker run
docker build
docker pull
docker push
docker ps
docker stop
docker rm
docker images
docker network ls
docker volume ls
```
