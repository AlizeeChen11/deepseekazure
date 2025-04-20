# deepseekazure

Prerequisites:
Donwload and install .net 8.0 SDK:
https://builds.dotnet.microsoft.com/dotnet/Sdk/8.0.408/dotnet-sdk-8.0.408-win-x64.exe

Install Azure app service extension in VS code

Deploy an Azure app service with .net 8.0 as runtime.

###
Run project https://github.com/your-account/DeepSeekAzure.git
```
dotnet restore DeepSeekAzure.sln
dotnet run --project DeepSeekAzureApi.csproj
```
### Deploy the project to Azure App Service
Enter the Endpoint and Key into the appsettings.json file of the DeepSeekAzureApi project.

Deploy the project to Azure App Service.
```
dotnet publish DeepSeekAzure.sln -c Release -o ./publish

az webapp deploy --resource-group elsa-vmrg --name azuredeepseek --src-path "C:\temp\DeepSeekAzure\publish" --type static
enountered error:
Initiating deployment
Deploying from local path: C:\temp\DeepSeekAzure\publish
Either 'C:\temp\DeepSeekAzure\publish' is not a valid local file path or you do not have permissions to access it
```
