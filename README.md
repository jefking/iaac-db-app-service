# Infrastructure as Code: App Service + SQL Database
The goal for these simple components is to onboard a new service as a secondary task to the underlying infrastructure. So what you see is global.json which deploys the control plain; and new-instance.json which subsiquently deploys a new Web App + Database onto the underlying infrastructure.

# Manual Deploy
## Global
az group deployment create --name global --resource-group dbappservice --template-file global.json --parameters global.params.json

## New Instance
az group deployment create --name new-instance --resource-group dbappservice --template-file new-instance.json --parameters new-instance.params.json

# Build Status
[![Build status](https://dev.azure.com/jefkin/oss/_apis/build/status/IaaC%20DB%20App%20Service)](https://dev.azure.com/jefkin/oss/_build/latest?definitionId=11)