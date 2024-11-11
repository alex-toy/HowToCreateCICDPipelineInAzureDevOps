# How to Create a CI/CD Pipeline in Azure DevOps

## Run Local

- build
```
dotnet restore
dotnet build --no-restore --configuration release
```

- publish : publishes the application and its dependencies to a folder for deployment to a hosting system.
```
dotnet publish --no-build --configuration release
```

- run local
```
cd HelloWorldApp\HelloWorldApp
dotnet bin\Debug\net6.0\HelloWorldApp.dll
```

## Create Pipeline

- choose : use the classic editor

- choose ASP.NET Core
<img src="/pictures/pipeline.png" title="pipeline"  width="900">