# Unit III: Microservices with Docker Compose

## 1. Microservices Architecture
*   **Need for microservices:** Complexity of monolithic applications.
*   **Monolithic vs Microservices:** Single deployment unit vs multiple small services.
*   **Advantages:** Scalability, fault isolation, agility.
*   **API Gateway:** A single entry point for all clients.

## 2. Docker Compose
*   **YAML Structure:** The format used for defining multi-container applications.
*   **Writing docker-compose.yml:** Defining services, networks, and volumes.
*   **Core Fields:** `version`, `services`, `volumes`, `networks`, `environment`.
*   **Secrets and configs:** Managing sensitive data.
*   **Build vs Image:** Building from a Dockerfile versus using a pre-existing image.
*   **Service Dependency:** Using `depends_on`.

## 3. Use Case Deployments
*   **Multi-container apps:** (e.g., Database + Backend + Frontend).
*   **WordPress + MySQL.**
*   **Node.js + MongoDB.**
*   **Java Spring Boot + PostgreSQL.**

---

## Unit III Practical Commands

### Using Docker Compose
```bash
# Start all services in the background
docker-compose up -d

# Stop services
docker-compose down

# Check service logs
docker-compose logs -f

# List running compose services
docker-compose ps
```

### Example `docker-compose.yml` (Node.js + MongoDB)
```yaml
version: '3.8'
services:
  web:
    build: .
    ports:
      - "3000:3000"
    depends_on:
      - db
  db:
    image: mongo:latest
    volumes:
      - mongo-data:/data/db

volumes:
  mongo-data:
```
