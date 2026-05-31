# Unit II: Image Building & Container Management

## 1. Dockerfile Core Concepts
*   **Image layering:** Each instruction adds a new layer.
*   **Build context & .dockerignore:** Files sent to the daemon during build.
*   **Dockerfile writing:** Best practices for writing efficient Dockerfiles.

## 2. Basic Instructions
*   `FROM`: Base image.
*   `RUN`: Execute commands in a new layer.
*   `COPY`: Copy files from host to container.
*   `ADD`: Like COPY, but can handle remote URLs and tar extraction.
*   `CMD`: Default command for the container.
*   `ENTRYPOINT`: Configures a container that will run as an executable.
*   `WORKDIR`: Sets the working directory.
*   `ENV`: Sets environment variables.
*   `EXPOSE`: Informs Docker that the container listens on specified network ports.
*   `VOLUME`: Creates a mount point for persistent storage.

## 3. Image Creation in Detail
*   `docker build`: The process of building an image from a Dockerfile.
*   **Tagging/Versioning:** `docker tag <image> <name>:<version>`.
*   **Inspecting Images:** `docker image inspect`, `docker history`.

## 4. Docker Networking
*   **Bridge network:** Default network for containers.
*   **Host network:** Containers share the host's networking namespace.
*   **Overlay network:** Connects multiple Docker daemons (used in Swarm).
*   **DNS inside Docker:** Automatic service discovery.
*   **Linking containers:** The legacy way (now use networks).
*   **Port mapping:** `-p <host_port>:<container_port>`.

## 5. Docker Storage
*   **Volumes:** Managed by Docker (best for persistence).
*   **Bind mounts:** Use host filesystem paths.
*   **Copy-on-write:** How Docker manages file changes across layers.

---

## Unit II Practical Commands

### Building and Managing Images
```bash
# Build an image
docker build -t my-app:v1 .

# Tag an image
docker tag my-app:v1 my-repo/my-app:latest

# View history
docker history my-app:v1
```

### Networking & Storage
```bash
# Create a bridge network
docker network create my-bridge

# Run with port mapping and volume
docker run -d -p 8080:80 -v my-vol:/app/data --name my-container nginx

# Inspect network
docker network inspect my-bridge
```

