**Overview for Azure Virtual Network Templates:**
============================

***This Master template creates the following resources:***
============================

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)]((https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fkothapalli2008%2FAzure-Learnings%2Fmaster%2FFoundation%2FActiveDirectory%2Fazuredeploy.json) )

 -2 Virtual Network

Connect-AzAccount -tenant "a697981c-c242-4f40-bf3c-1eb4412918f0" -Subscription "bccffc32-27d2-4348-b7b6-4897ed061b0d" -verbose

New-AzResourceGroup -Name azure-learnings-eus-rg -Location eastus -verbose

New-AzResourceGroupDeployment -TemplateFile .\Infrastructure\01-VirtualNetworks\azuredeploy.json -TemplateParameterFile .\Infrastructure\01-VirtualNetworks\azuredeploy.parameters.json -ResourceGroupName azure-learnings-eus-rg -verbose
