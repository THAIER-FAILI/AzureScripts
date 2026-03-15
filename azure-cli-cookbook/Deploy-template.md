# Deploy the template to Azure
# run this in vscode terminal where the azuredeploy.json exist
templateFile="azuredeploy.json"
today=$(date +"%d-%b-%Y")
DeploymentName="blanktemplate-"$today

az deployment group create --name $DeploymentName --template-file $templateFile

# OR in windows powershell with azure cli installed
az deployment group create \
  --resource-group Thair-RG \
  --template-file "C:\AzureScripts\vnet-2subnets\azuredeploy.json" \
  --parameters "@C:\AzureScripts\vnet-2subnets\azuredeploy.parameters.json"

# OR (run this in vscode terminal where the azuredeploy.json exist (with Parameters))
templateFile="azuredeploy.json"
today=$(date +"%d-%b-%Y")
DeploymentName="addnameparameter-"$today

az deployment group create --name $DeploymentName --template-file $templateFile --parameters storageName={your-unique-name}