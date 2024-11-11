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

### Dev Stage

- choose **App Service Deployment**
<img src="/pictures/release.png" title="release pipeline"  width="900">

- add artifact
<img src="/pictures/release1.png" title="release pipeline"  width="900">

- deploy Dev
<img src="/pictures/release2.png" title="release pipeline"  width="900">

- enable continuous deploy
<img src="/pictures/release3.png" title="release pipeline"  width="900">

- release pipeline should trigger automatically
<img src="/pictures/release4.png" title="release pipeline"  width="900">
<img src="/pictures/release41.png" title="release pipeline"  width="900">

- site should be deployed on dev environment
<img src="/pictures/release42.png" title="release pipeline"  width="900">

### Qa Stage

- add qa stage
<img src="/pictures/release5.png" title="release pipeline"  width="900">
<img src="/pictures/release51.png" title="release pipeline"  width="900">

- add predeployment approval
<img src="/pictures/release52.png" title="release pipeline"  width="900">

### Production Stage

- add staging slot
<img src="/pictures/release6.png" title="release pipeline"  width="900">

- add predeployment approval
<img src="/pictures/release66.png" title="release pipeline"  width="900">

- add production stage
<img src="/pictures/release61.png" title="release pipeline"  width="900">
<img src="/pictures/release62.png" title="release pipeline"  width="900">

- deploy to staging first
<img src="/pictures/release63.png" title="release pipeline"  width="900">

- add swap slots
<img src="/pictures/release64.png" title="release pipeline"  width="900">
<img src="/pictures/release65.png" title="release pipeline"  width="900">

### General Workflow

- make a modification to the code and push. Pipelines should automatically trigger
<img src="/pictures/release7.png" title="release pipeline"  width="900">

- give approval for QA stage
<img src="/pictures/release71.png" title="release pipeline"  width="900">
<img src="/pictures/release72.png" title="release pipeline"  width="900">

- give approval for prod stage
<img src="/pictures/release73.png" title="release pipeline"  width="900">
