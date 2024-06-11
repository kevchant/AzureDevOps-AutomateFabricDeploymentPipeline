# AzureDevOps-AutomateFabricDeploymentPipelineAll

Contains a template that you can use to automate your Microsoft Fabric Deployment Pipeline deployments using YAML Pipelines in Azure DevOps. Based on a blog post I wrote called '[Update Fabric Deployment Pipeline stages with DeploymentPipelines-DeployAll and YAML Pipelines](https://www.kevinrchant.com/2024/06/11/update-fabric-deployment-pipeline-stages-with-deploymentpipelines-deployall-and-yaml-pipelines/)'.

It can be used to automate the deployments to different stages within a deployment pipeline.

It uses a YAML pipeline, which you can find in the root of this repository. It utilizes a PowerShell script which you can find in the scripts folder.

In order to use it in Azure Pipelines you can either import or fork this repository into another GitHub repository or into Azure Repos.

You need to create the below variables somewhere, ideally in the variable groups specified

- agentpool - The name of the agent pool you ant to use for the deployment
- servicePrincipalKey - The secret value for the service principal key used
- servicePrincipalId - The service principal id
- tenantId - The tenant id that Microsoft fabric is hosted on
- deploymentPipelineName - The name of the deployment pipeline in Microsoft Fabric
- DevStageName - The name of the Development stage in the Microsoft Fabric deployment pipeline
- TestStageName - The name of the Test stage in the Microsoft Fabric deployment pipeline
- ProdStageName - The name of the Production stage in the Microsoft Fabric deployment pipeline
- deploymentNote - Any additional deployment note that you wish to add

 
Afterwards, you can select the YAML file in Azure Pipelines and tailor the pipeline to suit your needs.

This repository is provided "as is" based on the [MIT license](https://opensource.org/licenses/MIT). Basically, I am not responsible for your use of it.
