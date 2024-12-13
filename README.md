## Spring REST API Project με File Upload, Logging, DB Initialization, Specifications, Filtering.

# Documentation still under construction.

Spring-REST-API-Project is a Spring Boot-based REST API application that supports various features, including:

- File Upload
- Logging
- Database Initialization
- Specifications and Filtering

## Features

- **File Upload**: Supports uploading files via REST endpoints with validation and error handling.
- **Logging**: Comprehensive logging for all requests and key application processes.
- **Database Initialization**: Automatic seeding of the database with initial data on startup.
- **Specifications and Filtering**: Advanced querying capabilities using JPA Specifications, supporting dynamic filtering of data.

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Java 17 or higher
- Gradle 7.6+
- MySQL database

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/Spring-REST-API-Project.git
   cd Spring-REST-API-Project
   ```

2. Build the project:

   ```bash
   ./gradlew build
   ```

3. Configure the database in `application.properties` or `application.yml`:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/your_database
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   spring.jpa.hibernate.ddl-auto=update
   ```

4. Run the application:

   ```bash
   ./gradlew bootRun
   ```

### API Endpoints

#### File Upload

- **POST** `/api/files/upload`
  - Upload a file.
  - Request: Multipart form data.
  - Response: File details (name, size, upload timestamp).

#### Filtering and Querying

- **GET** `/api/items`
  - Retrieve items based on dynamic filters.
  - Parameters:
    - `field` (e.g., `name`)
    - `operation` (e.g., `equals`, `contains`)
    - `value` (e.g., `example`)

#### Logging

Logs all requests and responses in a structured format for debugging and analytics.

## Database Initialization

The application seeds initial data into the database during startup. Customize the data in `data.sql` or similar configuration files.

## Technologies Used

- **Spring Boot**: Framework for building the REST API.
- **Spring Data JPA**: For database operations and JPA Specifications.
- **Lombok**: To reduce boilerplate code.
- **MySQL**: Relational database for data persistence.
- **Logback**: Logging framework for structured logs.
- **Gradle**: Build automation tool.
