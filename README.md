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

- choose *use the classic editor*

- choose ASP.NET Core
<img src="/pictures/pipeline.png" title="pipeline"  width="900">
<img src="/pictures/pipeline1.png" title="pipeline"  width="900">

- enable continuous integration
<img src="/pictures/pipeline2.png" title="pipeline"  width="900">
```

## Create App Services

- choose .NET 6
<img src="/pictures/webapp.png" title="web app"  width="900">

## Create Release Pipeline

- choose **App Service Deployment**
<img src="/pictures/release.png" title="release pipeline"  width="900">

- add artifact
<img src="/pictures/release1.png" title="release pipeline"  width="900">

- deploy Dev
<img src="/pictures/release2.png" title="release pipeline"  width="900">
