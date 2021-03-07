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

To run the application in Development (refer to [ASP.NET Tutorial | Hello World in 10 minutes](https://dotnet.microsoft.com/learn/aspnet/hello-world-tutorial/intro)):
```
cd /vagrant/TodoApi
dotnet watch run
```

### Update lauchUrl and applicationUrl
Update the launchUrl from `swagger` to `api/TodoItems` and applicationUrl from `localhost` to `0.0.0.0` in order to listen from external connections in all IP addresses of the development virtual machine.
