# 🐳 Docker Practices & DevOps Syllabus

This repository contains practical exercises and commands based on the Docker and DevOps infrastructure syllabus.

---

## 📁 Unit Wise Index
1. [Unit I: Basics of DevOps Infrastructure](Unit1.md)
2. [Unit II: Image Building & Container Management](Unit2.md)
3. [Unit III: Microservices with Docker Compose](Unit3.md)
4. [Unit IV: Maven Build Automation](Unit4.md)
5. [Unit V: Continuous Integration (CI) with GitHub Actions](Unit5.md)

---

## 🖥️ Terminal Outputs & Practical Execution

### Unit I: Docker Basics
**Command:** `docker version`
```text
Client: Docker Engine - Community
 Version:           24.0.7
 API version:       1.43
 Go version:        go1.20.10
 Git commit:        afdd53b
 Built:             Thu Oct 26 09:08:01 2023
 OS/Arch:           linux/amd64
 Context:           default
```

**Command:** `docker run hello-world`
```text
Hello from Docker!
This message shows that your installation appears to be working correctly.
...
```

---

### Unit II: Image & Network Management
**Command:** `docker build -t my-app:v1 .`
```text
[+] Building 1.2s (7/7) FINISHED
 => [internal] load build definition from Dockerfile
 => => transferring dockerfile: 154B
 => [internal] load .dockerignore
 => [internal] load metadata for docker.io/library/node:14
 => [1/3] FROM docker.io/library/node:14
 => [2/3] COPY . /app
 => [3/3] RUN npm install
 => exporting to image
 => => writing image sha256:d3f...
 => => naming to docker.io/library/my-app:v1
```

**Command:** `docker network ls`
```text
NETWORK ID     NAME      DRIVER    SCOPE
06a1b2c3d4e5   bridge    bridge    local
f1e2d3c4b5a6   host      host      local
9z8y7x6w5v4u   none      null      local
```

---

### Unit III: Docker Compose
**Command:** `docker-compose up -d`
```text
[+] Running 2/2
 ⠿ Container db    Started
 ⠿ Container web   Started
```

---

### Unit IV: Maven Build
**Command:** `mvn package`
```text
[INFO] Scanning for projects...
[INFO] Building my-app 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] --- maven-compiler-plugin:3.8.1:compile (default-compile) @ my-app ---
[INFO] --- maven-surefire-plugin:2.22.2:test (default-test) @ my-app ---
[INFO] --- maven-jar-plugin:3.2.0:package (default-package) @ my-app ---
[INFO] BUILD SUCCESS
```

---

### Unit V: GitHub Actions
**Command:** `gh workflow run main.yml`
```text
✓ Created workflow dispatch event for main.yml at main
```

---
*Note: Terminal outputs are simulated based on standard Docker/Maven behavior as the local daemon was unreachable in this environment.*


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
