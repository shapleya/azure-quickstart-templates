# Provide High Availability to RD Gateway and RD Web Access servers in RDS deployment

<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-deployment-ha-gateway/PublicLastTestDate.svg" />&nbsp;
<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-deployment-ha-gateway/PublicDeployment.svg" />&nbsp;

<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-deployment-ha-gateway/FairfaxLastTestDate.svg" />&nbsp;
<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-deployment-ha-gateway/FairfaxDeployment.svg" />&nbsp;

<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-deployment-ha-gateway/BestPracticeResult.svg" />&nbsp;
<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-deployment-ha-gateway/CredScanResult.svg" />&nbsp;

This template deploys the following resources:

* a number of RD Gateway/RD Web Access VMs (number defined by 'numberOfWebGwInstances' parameter)

The template will

* Join all new VMs to the domain
* Deploy RDS roles in the deployment
* Join new VM's to the existing web and Gateway farm of basic RDS deployment
* Post configurations for web/Gateway VM's such as defining the Machine keys for IIS modules

### Prerequisites

Current Template is an extension to the Basic RDS Deployment Template, and it is mandatory to deploy any one of the template as prerequisite:

* Basic RDS deployment template  
  https://github.com/Azure/azure-quickstart-templates/tree/master/rds-deployment 

* RDS deployment from custom RDSH image  
  https://github.com/Azure/azure-quickstart-templates/tree/master/rds-deployment-custom-image-rdsh

* RDS deployment on pre-existing VNET and AD  
  https://github.com/Azure/azure-quickstart-templates/tree/master/rds-deployment-existing-ad

This template expects the same names of resources from RDS deployment, if resource names are changed in your deployment then please edit the parameters and resources accordingly, example of such resources are below:
<ul>
<li>publicIpRef: Resource must be exact same to existing RDS deployment.</li>
<li>availabilitySets: Resource must be exact same to existing RDS deployment.</li>
<li>Load-balancer: Load balancer name, Backend pool, LB-rules, Nat-Rule and NIC.</li>
<li>VM’s – VM name classification which is using copy index function.</li>
<li>NIC – NIC naming convention.</li>
</ul>


Click the button below to deploy

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fshapleya%2Fazure-quickstart-templates%2Fmaster%2Frds-deployment-ha-gateway%2Fazuredeploy.json" target="_blank">
    <img src="https://raw.githubusercontent.com/shapleya/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fshapleya%2Fazure-quickstart-templates%2Fmaster%2Frds-deployment-ha-gateway%2Fazuredeploy.json" target="_blank">
    <img src="https://raw.githubusercontent.com/shapleya/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.png"/>
</a>

