# SmartTrip Planner Backend

A comprehensive travel planning REST API built with Spring Boot that helps users plan their trips with features like weather forecasts, trip notifications, and location-based services.

## Tech Stack

- **Java 17**
- **Spring Boot 3.4.1**
- **MongoDB** - Database
- **Spring Security + JWT** - Authentication
- **Spring Mail** - Email notifications
- **Swagger/OpenAPI** - API Documentation
- **Maven** - Build tool

## Features

- **User Authentication** - Register, Login with JWT tokens
- **Trip Management** - Create, update, delete trips
- **Weather Integration** - Get weather forecasts for destinations
- **Location Services** - Search cities, countries with geocoding
- **Trip Notifications** - Email reminders for upcoming trips
- **User Profiles** - Profile management with photo upload
- **Category Management** - Organize trips by categories
- **Search** - Search destinations and trips

## API Endpoints

| Module | Endpoint | Description |
|--------|----------|-------------|
| Auth | `/api/auth/**` | Register, Login |
| Trips | `/api/trips/**` | Trip CRUD operations |
| Weather | `/api/weather/**` | Weather forecasts |
| Cities | `/api/cities/**` | City management |
| Countries | `/api/countries/**` | Country management |
| Categories | `/api/categories/**` | Category management |
| Profile | `/api/profile/**` | User profile management |
| Search | `/api/search/**` | Search functionality |
| Notifications | `/api/notifications/**` | Trip notifications |
| Maps | `/api/maps/**` | Map and directions |

## Prerequisites

- Java 17 or higher
- Maven 3.6+
- MongoDB Atlas account or local MongoDB instance

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/AnisaIdrees/smartTrip-Planner-backend.git
   cd smartTrip-Planner-backend/SmartPlanner
   ```

2. **Configure application.properties**

   Update `src/main/resources/application.properties` with your credentials:
   ```properties
   # MongoDB
   spring.data.mongodb.uri=your_mongodb_uri

   # JWT Secret (use a strong secret key)
   jwt.secret=your_secret_key

   # Email Configuration
   spring.mail.username=your_email
   spring.mail.password=your_app_password
   ```

3. **Build the project**
   ```bash
   ./mvnw clean install
   ```

4. **Run the application**
   ```bash
   ./mvnw spring-boot:run
   ```

The server will start at `http://localhost:8081`

## API Documentation

Once the application is running, access Swagger UI at:
```
http://localhost:8081/swagger-ui.html
```

## Project Structure

```
SmartPlanner/
├── src/main/java/com/SmartPlanner/SmartPlanner/
│   ├── config/          # Configuration classes
│   ├── controller/      # REST Controllers
│   ├── dto/             # Data Transfer Objects
│   ├── model/           # Entity models
│   ├── repository/      # MongoDB repositories
│   ├── scheduler/       # Scheduled tasks
│   ├── security/        # JWT & Security
│   └── service/         # Business logic
├── src/main/resources/
│   └── application.properties
└── pom.xml
```

## Environment Variables

For production, use environment variables instead of hardcoding credentials:

| Variable | Description |
|----------|-------------|
| `MONGODB_URI` | MongoDB connection string |
| `JWT_SECRET` | JWT signing secret key |
| `MAIL_USERNAME` | Email address for notifications |
| `MAIL_PASSWORD` | Email app password |

## Running Tests

```bash
./mvnw test
```

## Author

**Anisa Idrees**

## License

This project is licensed under the MIT License.
