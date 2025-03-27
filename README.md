# Spring Boot Auth0 Demo

This is a simple Spring Boot application demonstrating Auth0 authentication with a secured hello world endpoint.

## Prerequisites

- Java 17 or higher
- Gradle
- Auth0 account and application credentials

## Configuration

The application is configured to use Auth0 for authentication. The configuration is in `src/main/resources/application.properties`.

You need to set your Auth0 client secret as an environment variable when running the application:

```bash
export AUTH0_CLIENT_SECRET="your-client-secret"
```

## Running the Application

You can run the application in two ways:

1. Using Gradle:
```bash
AUTH0_CLIENT_SECRET="your-client-secret" ./gradlew bootRun
```

2. Using the executable JAR:
```bash
# First, build the JAR
./gradlew bootJar

# Then run it
AUTH0_CLIENT_SECRET="your-client-secret" java -jar build/libs/spring-boot-okta-demo-0.0.1-SNAPSHOT.jar
```

The application will start on http://localhost:8080

## Endpoints

- `/hello` - A secured endpoint that returns a personalized greeting for the authenticated user

## Security

This application uses Auth0 for authentication and authorization. Users must authenticate through Auth0 to access the endpoints.
