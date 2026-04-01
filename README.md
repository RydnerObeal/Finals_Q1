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
- Improves testability and maintainability
- Centralizes data operations

### 2. **Dependency Injection**
- Built-in .NET DI container for service registration
- Loose coupling between components
- Easier unit testing

### 3. **RESTful API Design**
- Standard HTTP methods (GET, POST, PUT, DELETE)
- Resource-based URLs
- Proper HTTP status codes

### 4. **Model-View-Controller (MVC)**
- Controllers handle HTTP requests and responses
- Models represent data entities
- Clear separation of concerns

### 5. **Async/Await Pattern**
- Non-blocking operations for better performance
- Improved scalability
- Proper resource management

## Evidence of Technical Debt Fixes

### 1. **Error Handling Improvements**
- **Before**: Basic try-catch blocks
- **After**: Global exception handling middleware
- **Impact**: Consistent error responses and better debugging

### 2. **Input Validation**
- **Before**: No validation on API inputs
- **After**: Data annotations and model validation
- **Impact**: Prevents invalid data and improves data integrity

### 3. **Logging Implementation**
- **Before**: No logging mechanism
- **After**: Structured logging with Serilog
- **Impact**: Better monitoring and debugging capabilities

### 4. **API Documentation**
- **Before**: No API documentation
- **After**: Swagger/OpenAPI integration
- **Impact**: Self-documenting API with interactive testing

### 5. **Environment Configuration**
- **Before**: Hardcoded configuration values
- **After**: Environment-specific configuration files
- **Impact**: Better deployment flexibility and security

### 6. **Code Organization**
- **Before**: Monolithic controller structure
- **After**: Separated concerns with services and repositories
- **Impact**: Improved maintainability and testability

### 7. **Database Context Optimization**
- **Before**: Inefficient database queries
- **After**: Optimized queries with proper async operations
- **Impact**: Better performance and reduced resource usage

## Bonus Challenge Features

### 1. **Advanced Error Handling**
- Custom exception middleware
- Detailed error logging
- User-friendly error responses

### 2. **Performance Monitoring**
- Request timing middleware
- Performance metrics collection
- Health check endpoints

### 3. **Security Enhancements**
- Input sanitization
- CORS configuration
- Rate limiting preparation

### 4. **Testing Infrastructure**
- Unit test project setup
- Integration test examples
- Mock data providers

## Technologies Used
- **.NET 8.0**
- **Entity Framework Core**
- **ASP.NET Core Web API**
- **Serilog** for logging
- **Swagger** for API documentation
- **xUnit** for testing
