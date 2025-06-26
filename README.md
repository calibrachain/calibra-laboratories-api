# Calibra Laboratories API

## Overview

The Calibra Laboratories API is a comprehensive system for managing calibration laboratories and their calibration type capabilities. This API enables users to create, read, update, and delete laboratory records, as well as manage the types of calibrations each laboratory can perform.

## Features

- Complete CRUD operations for laboratories
- Management of calibration types
- Laboratory status tracking
- Search and filtering capabilities
- OpenAPI documentation with Swagger UI

## API Documentation

The complete API documentation is available in production at:
[https://laboratories.onrender.com/swagger-ui/index.html#](https://laboratories.onrender.com/swagger-ui/index.html#)

The Swagger UI provides an interactive interface to explore and test all available endpoints.

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven 3.6+
- Spring Boot 3.x

### Installation and Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/calibra-laboratories-api.git
   cd calibra-laboratories-api
   ```

2. Build the project:

   ```bash
   mvn clean package
   ```

3. Run the application:

   ```bash
   java -jar target/*.jar
   ```

Alternatively, you can use the Spring Boot Maven plugin:

```bash
mvn spring-boot:run
```

## API Endpoints

### Laboratories

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | /api/v1/laboratories | Get all laboratories |
| GET    | /api/v1/laboratories/{accreditationNumber}/status | Get laboratory status |
| POST   | /api/v1/laboratories | Create a new laboratory |
| PATCH  | /api/v1/laboratories/{accreditationNumber}/status/{status} | Update laboratory status |
| DELETE | /api/v1/laboratories/{accreditationNumber} | Delete a laboratory |

### Calibration Types

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | /api/v1/calibration-types | Get all calibration types |
| POST   | /api/v1/calibration-types | Create a new calibration type |

## Data Models

### Laboratory

```json

{
  "name": "string",
  "accreditationNumber": "string",
  "status": "string",
  "state": "string",
  "calibrationType": {
    "description": "string"
  }
}
```

### Calibration Type

```json
{
  "description": "string"
}
```

## Configuration

The application can be configured through the `application.properties` file. Key configuration options include:

- Server port
- Database connection details
- Logging levels
- API versioning

## Development

### Running Tests

```bash
mvn test
```

## License

This project is licensed under the terms of the license included in the repository.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

For support, please open an issue in the repository or contact the development team.
