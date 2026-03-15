#Create and set the default resource group
az group create --name <resource-group-name> --location <location>
az configure --defaults group="<resource-group-name>"