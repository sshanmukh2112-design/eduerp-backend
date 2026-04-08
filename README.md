EDUERP Backend ⚙️🔐

We built this backend for our Educational ERP platform to handle secure authentication, role-based access, and efficient data management using Spring Boot.

🏗️ Core Architecture & Modules
1. Authentication System (AuthController, AuthService) 🔐
Purpose: We designed this module to handle secure user login and registration.
Key Mechanics:
Exposes REST endpoints (/api/auth/login, /api/auth/signup).
Validates user credentials and ensures role-based access control.
Uses structured request/response DTOs for clean data transfer.
2. Security Configuration (Spring Security, JWT Filter) 🛡️
Purpose: We implemented this to secure APIs and protect routes.
Key Mechanics:
JWT-based authentication for stateless session handling.
Custom filters intercept requests and validate tokens.
Configured role-based authorization for different endpoints.
3. Controller Layer (StudentController, etc.) 🎯
Purpose: Handles incoming HTTP requests and routes them to services.
Key Mechanics:
RESTful APIs designed for frontend integration.
Uses annotations like @RestController, @RequestMapping.
Returns structured JSON responses.
4. Service Layer (Business Logic) ⚡
Purpose: Contains the core application logic.
Key Mechanics:
Processes data before sending to database or frontend.
Ensures separation of concerns between controller and data layer.
5. Repository Layer (JPA Repositories) 🗄️
Purpose: Manages database operations.
Key Mechanics:
Uses Spring Data JPA for CRUD operations.
Maps Java entities to database tables.
🛠️ Technology Stack
Backend Framework: Spring Boot
Security: Spring Security, JWT
Database: MySQL
ORM: Spring Data JPA
⚙️ Setup & Run
mvn clean install
mvn spring-boot:run
🔑 Configuration

Update application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/your_db
spring.datasource.username=your_username
spring.datasource.password=your_password

jwt.secret=your_secret_key

📌 Notes
Sensitive data like DB credentials and JWT secrets should not be committed.
Backend must run before frontend for full functionality.
