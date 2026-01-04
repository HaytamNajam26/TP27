# Microservices Book Application

## Description
This project demonstrates a microservices architecture using Spring Boot and Docker. It consists of a Book Service (running in multiple instances) and a Pricing Service, communicating with a MySQL database.



## Architecture
The application is composed of the following services defined in `docker-compose.yml`:

- **MySQL**: Database service for storing book data.
- **Pricing Service**: Handles pricing logic.
- **Book Service**: Manages book information. Deployed as 3 separate instances for scalability:
  - Instance 1: Port `8081`
  - Instance 2: Port `8083` (mapped to internal `8081`)
  - Instance 3: Port `8084` (mapped to internal `8081`)

## Getting Started

### Prerequisites
- Docker and Docker Compose installed.
- Java JDK 17+ (for local development).

### Running the Application
To build and run the entire system using Docker Compose:

```bash
docker-compose up --build
```

## API Endpoints

| Service | Port | Description |
|---------|------|-------------|
| **Pricing Service** | `8082` | Core pricing logic |
| **Book Service 1** | `8081` | First instance of Book Service |
| **Book Service 2** | `8083` | Second instance of Book Service |
| **Book Service 3** | `8084` | Third instance of Book Service |
| **MySQL** | `3306` | Database access |

## Technologies
- **Java / Spring Boot**
- **Docker / Docker Compose**
- **MySQL**
## Screenshots
<!-- Place your screenshots below -->


---