# Unit I: Basics of DevOps Infrastructure

## 1. Introduction to Containers
*   **Origin of containers:** Early isolation methods like `chroot` (1979).
*   **Emergence of Modern Containerization:** Solaris Zones, FreeBSD Jails, and eventually LXC (LinuX Containers).
*   **Integration into DevOps:** How containers bridge the "it works on my machine" gap.

## 2. Container Runtime
The component that runs containers (e.g., `containerd`, `CRI-O`, `Docker Engine`).

## 3. Process Isolation & Namespaces
Linux kernel features that provide isolation:
*   `pid`: Process IDs
*   `net`: Network stack
*   `mnt`: Mount points
*   `uts`: Hostname and NIS domain name
*   `ipc`: Interprocess communication
*   `user`: User and Group IDs

## 4. Control Groups (cgroups)
Used for limiting and monitoring resources (CPU, Memory, I/O).

## 5. Container Images & Layers
Images are read-only templates. Layers are formed by each instruction in a Dockerfile.

## 6. Image Registries & Distribution
Places to store and share images (e.g., Docker Hub, Amazon ECR).

## 7. Introduction to Docker
Docker is a platform for developing, shipping, and running applications in containers.

## 8. Docker Architecture
Client-Server architecture. The Docker Client talks to the Docker Daemon (`dockerd`).

## 9. Docker Daemon
The background process that manages Docker objects.

## 10. Docker CLI
The command-line interface for interacting with the Docker Daemon.

## 11. Docker Registry & Hub
Docker Hub is the default public registry.

## 12. Object Types
*   **Container:** A runnable instance of an image.
*   **Image:** Read-only template for creating containers.
*   **Network:** Provides connectivity between containers.
*   **Volume:** Persistent data storage.

## 13. Docker Layering & Filesystem
Uses Union File System (UnionFS) to stack layers.

---

## Unit I Practical Commands

### Checking Docker Status
```bash
# Check version
docker version

# System info
docker info
```

### Basic Imagery & Container Operations
```bash
# Pull an image
docker pull alpine

# List images
docker images

# Run a container
docker run -it alpine /bin/sh

# List running containers
docker ps

# Inspect an image
docker image inspect alpine
```

