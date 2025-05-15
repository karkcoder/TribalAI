# TribalAI - .NET Aspire Project

This is a .NET Aspire project created with the Aspire empty template.

## Project Structure

- **TribalAI.AppHost**: The orchestrator for the distributed application.
- **TribalAI.ServiceDefaults**: Default configuration for services in the application.

## Getting Started

To run the application:

1. Ensure you have .NET SDK 9.0+ installed
2. Open the solution in Visual Studio 2022 or later (or your preferred IDE)
3. Set the AppHost project as the startup project
4. Press F5 to run the application

## Adding Services

To add a new service to your Aspire application:

1. Create a new project in the solution
2. Reference it from the AppHost project
3. Register the service in the AppHost's Program.cs file

Example:

```csharp
var builder = DistributedApplication.CreateBuilder(args);
builder.AddProject<Projects.MyNewService>("my-service");
builder.Build().Run();
```
