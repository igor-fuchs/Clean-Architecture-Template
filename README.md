# Clean Architecture Template

A minimal, ready-to-use **.NET 10** solution template following **Clean Architecture** principles. Clone it, rename it, and start building.

## Project Structure

```
src/
├── Domain/            → Core entities and business rules (no dependencies)
├── Application/       → Use cases and application logic (depends on Domain)
├── Infrastructure/    → External concerns: databases, APIs, etc. (depends on Application & Domain)
└── Presentation/      → ASP.NET Core Web API entry point
```

## Features

- **.NET 10.0** targeting
- **Nullable reference types** enabled
- **Implicit usings** enabled
- **Treat warnings as errors** for strict compilation
- **Central Package Management** via `Directory.Packages.Props`
- **Artifacts output** consolidated in a single `artifacts/` folder
- Clean dependency flow: `Presentation → Infrastructure → Application → Domain`

## Getting Started

1. **Clone or download** this repository.

2. **Rename the template** to match your project name.  
   Use your editor's global search & replace to find all occurrences of `CleanArchitectureTemplate` and replace them with your desired project name (e.g. `MyApp`).

   Files that will be affected:
   - `CleanArchitectureTemplate.slnx` (filename and contents)
   - `src/Domain/Domain.csproj` (`RootNamespace`)
   - `src/Application/Application.csproj` (`RootNamespace`)
   - `src/Infrastructure/Infrastructure.csproj` (`RootNamespace`)
   - `src/Presentation/Presentation.csproj` (`RootNamespace`)

3. **Restore & run**:
   ```bash
   dotnet restore
   dotnet run --project src/Presentation
   ```

## License

This project is licensed under the [MIT License](LICENSE).

