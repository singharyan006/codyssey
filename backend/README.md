# Codyssey Backend

Spring Boot (Java 21) API for code analysis and orchestration.

## Tech Stack

- Spring Boot (Java 21)
- Maven/Gradle build system
- Static Analysis Tools:
  - PMD for code smells and complexity
  - Checkstyle for style and naming conventions
  - SpotBugs for bug patterns
- PostgreSQL for data storage

## Key Features

- REST API for code submission and analysis
- Static analysis integration and result processing
- Code Quality Index (CQI) calculation
- Database persistence for submissions and results
- Communication with AI service for mentoring features

## Getting Started

1. Ensure you have Java 21 installed
2. Configure database connection in `application.properties`
3. Build the project:
   ```
   ./mvnw clean install
   ```
4. Run the application:
   ```
   ./mvnw spring-boot:run
   ```

## API Endpoints

- `POST /api/submissions` - Create submission, enqueue analysis
- `GET /api/submissions/{id}` - Get status/results
- `POST /api/analyze/sync` - Synchronous analysis (dev/demo mode)

See the API documentation in the `/docs` directory for complete details.
