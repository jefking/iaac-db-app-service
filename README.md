# iaac-db-app-service

# Manual Deploy
## Global
az group deployment create --name global --resource-group everything --template-file global.json --parameters global.params.json

## New Instance
az group deployment create --name new-instance --resource-group everything --template-file new-instance.json --parameters new-instance.params.json

# Build Status
[![Build status](https://dev.azure.com/jefkin/oss/_apis/build/status/IaaC%20DB%20App%20Service)](https://dev.azure.com/jefkin/oss/_build/latest?definitionId=11)