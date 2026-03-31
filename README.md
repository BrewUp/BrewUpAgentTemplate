# BrewUpAgentTemplate - .NET Modular API Template

An advanced template for building .NET APIs based on modular architecture and Domain-Driven Design (DDD) principles.

## 🎯 Goal

This project provides a solid foundation for rapid development of .NET APIs that follow:
- **Modular architecture** with separated Bounded Contexts
- **Domain-Driven Design (DDD)** patterns and best practices
- **Clean Architecture** with a clear separation of layers
- **Standardized and scalable structure** and scalable

## 🏗️ Architecture

The template implements a modular architecture where each module represents a domain Bounded Context:

```
src/
├── {ProjectName}.Rest/                             # API Layer & Composition Root
├── {ProjectName}.Infrastructure/                   # Shared Infrastructure
├── {ProjectName}.Shared/                           # Shared Kernel
└── {ModuleName}/                                   # Bounded Context Module
    ├── {ProjectName}.{ModuleName}.Domain/          # Domain Layer
    ├── {ProjectName}.{ModuleName}.Facade/          # Presentation Layer
    ├── {ProjectName}.{ModuleName}.Infrastructure/  # Infrastructure Layer
    ├── {ProjectName}.{ModuleName}.ReadModel/       # Query Models
    ├── {ProjectName}.{ModuleName}.SharedKernel/    # Module Contracts
    └── {ProjectName}.{ModuleName}.Tests/           # Unit Tests
```

## 🚀 How to Use

### 1. Generate the Skeleton

Edit the `.github/prompts/rest-api.prompt.md` file to define:
- Project name
- Required modules (Bounded Contexts)
- Basic API structure

Then, ask your AI assistant to generate the skeleton using this prompt.

### 2. Implement the Modules

For each created module, use the dedicated prompts to develop business logic:
- `.github/prompts/purchases-module.prompt.md` - Module for managing purchases
- `.github/prompts/warehouse-module.prompt.md` - Module for warehouse management
- `.github/prompts/domain-driven-design.prompt.md` - DDD guidelines

### 3. Customization

Adapt the prompts to your specific needs by modifying:
- Domain and module names
- Specific business logic
- Required external integrations

## 📁 Prompt Structure

Prompts are organized under `.github/prompts/` and include:

| Prompt | Purpose |
|--------|--------|
| `rest-api.prompt.md` | Generates the API skeleton |
| `domain-driven-design.prompt.md` | Guidelines for applying DDD patterns |
| `purchases-module.prompt.md` | Implementation of the Purchases module |
| `warehouse-module.prompt.md` | Implementation of the Warehouse module |

## 🛠️ Technologies

- **.NET 9** - Main framework
- **ASP.NET Core** - Web API framework
- **FluentValidation** - Model validation
- **Serilog** - Structured logging

## 🎨 Pattern Implementati

### Domain-Driven Design
- **Bounded Context** - Logical separation of domains
- **Aggregates** - Data consistency boundaries
- **Domain Events** - Asynchronous communication
- **Repository Pattern** - Persistence abstraction
- **Value Objects** - Immutable, identity-free objects

### Clean Architecture
- **Domain Layer** - Pure business rules
- **Application Layer** - Use cases and orchestration
- **Infrastructure Layer** - Concrete implementations
- **Presentation Layer** - API endpoints and presentation

### CQRS
- **Commands** - Write operations
- **Queries** - Read operations
- **Handlers** - Separate processing for commands and queries

## 📖 Usage Example

1. **Clone the template**
2. **Edit** `rest-api.prompt.md` with your requirements:
   ```markdown
   # Project name: RistoranteManager
   # Modules: Purchases, Sales, Warehouse
   ```
3. **Generate the skeleton** using the AI assistant
4. **Implement modules** using the dedicated prompts
5. **Customize** the business logic

## 🤝 Contributing

To contribute to the template:
1. Improve existing prompts
2. Add new prompts for other domains
3. Propose architectural improvements
4. Share usage examples

## 📄 License

This project is released under the MIT license. See the LICENSE file for details..

---

**Nota**: This is a template designed to accelerate modular API development. Adapt it to your specific needs and refine the prompts based on your experience.