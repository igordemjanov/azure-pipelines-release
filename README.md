# Release Pipelines
## Description 
This repository contains Release templates, often referred as 'Continuous Delivery/Deployment' (CD) pipelines, and these templates are defined in YAML format. Description about each job template is listed below with its input parameters and tasks.

## Templates
### Azure App Service
#### Tasks included
- Azure App Service Deploy

#### Parameters
| Parameter | Description |
|--|--|
| name | Internal name of the job |
| display_name | Display name of the job |
| pool | Name of the Agent (more info [here](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/pools-queues?view=azure-devops&tabs=yaml)) |
| project_title | Title of the project |
| environment | Name of the Environment in Azure Devops to perform a release |
| azure_service_connection | Name of the Azure Service connection |
| app_name | Name of the Azure App Service |
| app_type | Type of the Azure App Service |
| artifact_name | Name of the Artifact to be used for release |
| depends_on | Applicable if current job has a dependency on another job in the same pipeline. Provide Internal name of the job. |

### ARM Template
#### Tasks included
- Extract Files
- Azure Resource Group Deployment

#### Parameters
| Parameter | Description |
|--|--|
| name | Internal name of the job |
| display_name | Display name of the job |
| pool | Name of the Agent (more info [here](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/pools-queues?view=azure-devops&tabs=yaml)) |
| project_title | Title of the project |
| environment | Name of the Environment in Azure Devops to perform a release |
| azure_service_connection | Name of the Azure Service connection |
| resource_group | Name of the Azure Resource Group |
| resource_group_location | Location of the Azure Resource Group |
| template | Name of the ARM template file |
| template_parameters | Name of the ARM parameters file |
| artifact_name | Name of the Artifact to be used for release |
| depends_on | Applicable if current job has a dependency on another job in the same pipeline. Provide Internal name of the job. |
