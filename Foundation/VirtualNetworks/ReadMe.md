**Overview for Azure Virtual Network Templates:**
============================

***This Master template creates the following resources:***
============================

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fkothapalli2008%2FAzure-Learnings%2Fmaster%2FFoundation%2FActiveDirectory%2Fazuredeploy.json)

 -2 Virtual Network

Connect-AzAccount -tenant "78efe786-1610-49d8-97ab-c710be9ac898" -Subscription "bccffc32-27d2-4348-b7b6-4897ed061b0d" -verbose

New-AzResourceGroup -Name azure-learnings-eus-rg -Location eastus -Tags @{"Owner"="Krish Kothapalli"; "Project"="Azure Foundation"; "Cost Center"="Learning-01"; "Department"="Training"; "Created By"="Krish Kothapalli"; "Environment"="Production"}

 New-AzResourceGroupDeployment -TemplateFile .\VirtualNetworks\vnet_build.json -TemplateParameterFile .\VirtualNetworks\vnet_build.parameters.json -ResourceGroupName azure-learnings-eus-rg -verbose