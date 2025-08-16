# Kiron API (.NET 8) — Core Setup

This repository contains the Kiron assessment API built on **.NET 8** with Dapper, JWT auth, Swagger, and a generic caching layer.

> You are viewing the **core solution files**. Controllers, Services, Models, Data, Caching, and SQL scripts are provided in separate zip chunks. Extract **all chunks** into the same root folder to get a complete, buildable solution.

## Prerequisites
- Windows 11 + Visual Studio 2022 (17.9+)
- .NET 8 SDK
- SQL Server (Developer/Express) + SSMS

## First Run
1. Extract all zip chunks into a single folder named `Kiron` so that the structure looks like:
   ```
   Kiron/
   ├─ Kiron.sln
   └─ Kiron.Api/
      ├─ Kiron.Api.csproj
      ├─ Program.cs
      ├─ appsettings.json
      ├─ Controllers/
      ├─ Services/
      ├─ Models/
      ├─ Data/
      ├─ Caching/
      └─ SQLScripts/
   ```
2. Restore the `KironTest` database in SQL Server from the provided `.bak` (or run `SQLScripts`).
3. Open `Kiron.sln` in Visual Studio 2022.
4. Update `appsettings.json` connection string and `JwtSettings:Key`.
5. Build & Run. Swagger: `https://localhost:<port>/swagger`.

## Notes
- `Program.cs` is configured with JWT auth, Swagger (with JWT), CORS, and DI placeholders. The service registrations are uncommented in the complete full solution once all chunks are present.
- The `Kiron.Api.csproj` targets `net8.0` and includes packages: Dapper, Microsoft.Data.SqlClient, Swashbuckle, JwtBearer.

Happy coding!
