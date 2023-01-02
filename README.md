# helloWorld
Push the Sample Application to Repo
1. DevOps Portal → Create a Project (HelloWorldApp)
2. Project → Repo → Files → Copy Clone URL to Clipboard
3. D:\DevOpsDemos>git clone <Paste the URL>
4. D:\DevOpsDemos>dotnet new sln -o HelloWorldApp
5. D:\DevOpsDemos> cd HelloWorldApp
6. D:\DevOpsDemos\HelloWorldApp> dotnet new mvc -n HelloWorldApp.Web
7. D:\DevOpsDemos\HelloWorldApp> dotnet sln HelloWorldApp.sln add
HelloWorldApp.Web\HelloWorldApp.Web.csproj
8. git add .
9. git commit -m "Initial Commit"
10. git push origin master
11. Switch back to the web portal and View the Committed Files.
Create a Pipeline
1. Pipeline → New Pipeline → Use the classic editor
2. Select your Source Code Repository and Branch → Continue
3. Select a Template: Select ASP.NET Core → Apply
4. This generates all the Tasks in a Job.
5. Click on Save and queue.
Enable Continuous Integration
Pipelines → Select Build Pipeline → Edit → Tab Triggers → Continuous integration → Enable continuous
integration
Continous Deployment
Step1: Create an Azure App Service with Slots
1. Create an App Service = DssDemoApp-Dev
2. Create an App Service = DssDemoApp-QA
3. Create an App Service = DssDemoApp / Slot = Staging
Step2: Add Release Stage (QA)
1. Pipelines → Releases → +New → New release pipeline → Select Template Azure App Service
Deployment → Apply
2. Change Stage name = Dev Stage
3. View Stage tasks: Click on 1 job, task, Select Azure Subscription = <Subscription created before>, App type
= Web App on Linux, App service name = Dssdemoapp
4. Check Deploy to App Service, App Service Name = Dev


Thankyou
