Task Management API – Machine Test

Tech Stack
- .NET 8
- ASP.NET Core Web API
- Entity Framework Core (SQLite)
- Clean Architecture (Domain, Application, Infrastructure, API)

How to Run
1. Open the solution in Visual Studio 2022
2. Set TaskManagement.Api as startup project
3. Press F5
4. Swagger will open automatically

Features Implemented
- CRUD Task API endpoints
- Repository pattern with dependency injection
- Background service (TaskNotificationService) running every 30 seconds
  Logs overdue tasks to the console
- External API integration using Open-Meteo (no API key)
  Demonstrates HttpClient usage and error handling

Endpoints
- GET    /api/tasks
- GET    /api/tasks/{id}
- POST   /api/tasks
- PUT    /api/tasks/{id}
- PATCH  /api/tasks/{id}/complete
- DELETE /api/tasks/{id}
- GET    /api/external/weather

Notes
- SQLite database is created automatically on first run
- Background service uses scoped repository via IServiceScopeFactory
