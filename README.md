# Finals_Q1 - Backend API

## Setup and Execution Instructions

### Prerequisites
- .NET 8.0 SDK or later
- Visual Studio 2022 or VS Code

### Running the Application
```bash
# Clone the repository
git clone https://github.com/RydnerObeal/Finals_Q1.git
cd Finals_Q1

# Restore dependencies
dotnet restore

# Run the application
dotnet run
```

The API will be available at `http://localhost:5000` or `https://localhost:5001`

### API Endpoints
- `GET /api/todo` - Get all todo items
- `GET /api/todo/{id}` - Get a specific todo item
- `POST /api/todo` - Create a new todo item
- `PUT /api/todo/{id}` - Update an existing todo item
- `DELETE /api/todo/{id}` - Delete a todo item

## Architectural Patterns Used

### 1. **Repository Pattern**
- Separates data access logic from business logic
- Makes the code easier to test and maintain
- Centralizes all database operations

### 2. **Dependency Injection**
- .NET's built-in dependency injection container
- Helps manage service dependencies automatically
- Makes components loosely coupled

### 3. **RESTful API Design**
- Uses standard HTTP methods (GET, POST, PUT, DELETE)
- Follows REST conventions for API endpoints
- Returns proper HTTP status codes

### 4. **Model-View-Controller (MVC)**
- Controllers handle HTTP requests
- Models represent data entities
- Clear separation of concerns

### 5. **Async/Await Pattern**
- Non-blocking database operations
- Better performance and scalability
- Prevents application freezing

## Evidence of Fixing Technical Debt Items

### 1. **Error Handling**
- **Before**: Basic try-catch blocks with generic error messages
- **After**: Global exception handling middleware with structured error responses
- **Impact**: Consistent error responses and better debugging experience

### 2. **Input Validation**
- **Before**: No validation on API inputs
- **After**: Data annotations and model validation attributes
- **Impact**: Prevents invalid data from entering the system

### 3. **Logging**
- **Before**: No logging mechanism
- **After**: Structured logging with Serilog
- **Impact**: Better monitoring and troubleshooting capabilities

### 4. **API Documentation**
- **Before**: No API documentation
- **After**: Swagger/OpenAPI integration
- **Impact**: Self-documenting API with interactive testing interface

### 5. **Configuration Management**
- **Before**: Hardcoded values in code
- **After**: Environment-specific configuration files
- **Impact**: Better deployment flexibility and security

### 6. **Code Organization**
- **Before**: All logic in controllers
- **After**: Separated services and repositories
- **Impact**: Improved maintainability and testability

### 7. **Database Performance**
- **Before**: Inefficient database queries
- **After**: Optimized queries with async operations
- **Impact**: Faster response times and better resource usage

## Technologies Used
- **.NET 8.0** - Main framework
- **Entity Framework Core** - Database ORM
- **ASP.NET Core Web API** - API framework
- **Serilog** - Structured logging
- **Swagger** - API documentation
- **xUnit** - Testing framework
