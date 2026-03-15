#Deploy the template to Azure
templateFile="azuredeploy.json"
today=$(date +"%d-%b-%Y")
DeploymentName="blanktemplate-"$today

az deployment group create --name $DeploymentName --template-file $templateFile

#OR
az deployment group create \
  --resource-group Thair-RG \
  --template-file "C:\AzureScripts\vnet-2subnets\azuredeploy.json" \
  --parameters "@C:\AzureScripts\vnet-2subnets\azuredeploy.parameters.json"