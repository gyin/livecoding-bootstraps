# C# .NET Bootstrap (Console + xUnit)

This folder contains a minimal C# .NET 8.0 solution for live coding, technical interviews, and coding dojos. It includes a console application and an xUnit test project, following best practices for .NET development.

## Project Structure
- `Bootstrap.sln` — Solution file
- `src/App/` — Console application (`App.csproj`)
- `tests/App.Tests/` — xUnit test project (`App.Tests.csproj`)

## How It Was Created
```
dotnet new sln -n Bootstrap
dotnet new console -n App -o src/App --framework net8.0
dotnet new xunit -n App.Tests -o tests/App.Tests --framework net8.0
dotnet sln add src/App/App.csproj
dotnet sln add tests/App.Tests/App.Tests.csproj
dotnet add tests/App.Tests/App.Tests.csproj reference src/App/App.csproj
```

## Prerequisites
- [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) installed

## Running in GitHub Codespaces
You can use this project directly in GitHub Codespaces for interviews or coding dojos. No local installation is required.

1. Fork this repository into your own account.
2. Create a new Codespace from your fork.
3. Open the `csharp-xunit` folder in Codespaces.
4. Use the integrated terminal to run the setup and commands below.

## First-Time Setup
Restore dependencies before running or testing:
```pwsh
dotnet restore
```

## Running the Console App
Run the app by specifying the project file:
```pwsh
dotnet run --project src/App/App.csproj
```

## Running the Tests
```pwsh
dotnet test
```

## Notes
- The test project references the console app, allowing you to test its code directly.
- This structure is ideal for quick prototyping, interviews, and coding practice.

## Troubleshooting
- If you encounter missing dependencies, run `dotnet restore` in the solution root.
- For more info, see the [Microsoft .NET docs](https://docs.microsoft.com/dotnet/core/).
