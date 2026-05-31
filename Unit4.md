# Unit IV: Maven Build Automation

## 1. Why Build Tools Exist
To automate repetitive tasks like compilation, testing, and packaging.

## 2. Project Object Model (POM)
The `pom.xml` file is the heart of a Maven project.

## 3. Build Lifecycle Phases
`validate` -> `compile` -> `test` -> `package` -> `verify` -> `install` -> `deploy`.

## 4. Key Concepts
*   **Parent POM:** Managing common configurations across multiple projects.
*   **Dependency scope:** `compile`, `provided`, `runtime`, `test`, `system`.
*   **Transitive dependencies:** Dependencies of dependencies.
*   **Version conflicts & resolution:** How Maven chooses which version to use.
*   **Dependency Management:** Centralized version control.

## 5. Maven Plugins
*   `Compiler plugin`: Compiles Java code.
*   `Surefire plugin`: Runs unit tests.
*   `Shade plugin`: Creates a "fat" jar (uber jar).
*   **Maven wrapper (mvnw):** Ensures the same Maven version is used.

## 6. Maven and Docker Integration
*   `dockerfile-maven-plugin`: Automates image building during Maven build.
*   **Dockerizing Maven-based applications:** Best practices for Dockerfiles.
*   **Pushing artifacts:** Pushing images to registries.

---

## Unit IV Practical Commands

### Basic Maven Commands
```bash
# Compile and package
mvn package

# Run tests
mvn test

# Clean build
mvn clean install
```

### Dockerizing Maven App
```dockerfile
# Typical Dockerfile for a Maven project
FROM openjdk:11-jre-slim
COPY target/my-app.jar /app.jar
ENTRYPOINT ["java", "-jar", "/app.jar"]
```
