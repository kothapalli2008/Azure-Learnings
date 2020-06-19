**Overview for Azure Cloud Foundation Templates:**
============================

***This Master template creates the following resources:***
============================

 -2 Virtual Network

Connect-AzAccount -tenant "a697981c-c242-4f40-bf3c-1eb4412918f0" -Subscription "bccffc32-27d2-4348-b7b6-4897ed061b0d" -verbose

New-AzResourceGroup -Name azure-learnings-eus-rg -Location eastus -verbose

New-AzResourceGroupDeployment -TemplateFile .\Infrastructure\01-VirtualNetworks\azuredeploy.json -TemplateParameterFile .\Infrastructure\01-VirtualNetworks\azuredeploy.parameters.json -ResourceGroupName azure-learnings-eus-rg -verbose
