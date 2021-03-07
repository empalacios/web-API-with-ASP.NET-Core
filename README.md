# Tutorial: Create a web API with ASP.NET Core
Creation of the needed environment to follow and steps described in https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-5.0&tabs=visual-studio

## Testing Virtual Machine
Creation of the testing virtual machine, development platform, using Vagrant.

### .NET Core Installation
Steps followed from https://docs.microsoft.com/es-es/dotnet/core/install/linux-debian, these steps are embedded in the virtual machine creation.

### NuGet
Installation of NuGet package manager for .NET projects and update to latest version

## Tutorial Steps
### Web API Project Creation
Creation of the project in /vagrant in order to include the project folder in the repository.
```
dotnet new webapi -o /vagrant/TodoApi
cd /vagrant/TodoApi
dotnet add package Microsoft.EntityFrameworkCore.InMemory
```
