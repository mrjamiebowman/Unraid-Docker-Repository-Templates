# Unraid Docker Repository Templates
A collection of useful developer containers for Unraid.   

# WIP: UNDER CONSTRUCTION (02/17/2023)
Work In Progress.. hoping to get this done ASAP

## Containers Included
* Azure Build Agent (.NET 7, Terraform, Ansible, Packer)  
* NuGet Server
* Parrot OS
* Kafka (Confluent / Landoop)
* Debezium
* kSqlDb
* Microservice Toolbox (MBOX)

## Unraid Useage

`/usr/local/emhttp/plugins/dynamix.docker.manager/scripts/docker create --name='AzureDevOpsAgent' --net='bridge' -e TZ="America/Chicago" -e HOST_OS="Unraid" -e 'AZP_URL'='https://dev.azure.com/your-org-name' -e 'AZP_TOKEN'='' -e 'AZP_AGENT_NAME'='dockeragent-01' -e 'AZP_POOL'='Unraid' 'mrjamiebowman/azure-build-agent'`   

Firstly you need to be running unRAID ver 6.0.0 or later, once installed follow the instructions below:-

1. Navigate to "Docker" tab and then the "Docker Repositories" sub-tab in the unRAID webui
2. Enter in a URL of `https://github.com/mrjamiebowman/docker-templates` in the "Template repositories" field
3. Click on the "Save" button
4. Click back to "Docker" tab and then click on the "Add Container" button
5. Click on the "Template" dropdown menu and select the desired Docker image
6. Click the "Advanced View" toggle on the top right and fill in required fields e.g. volume data, environment variables etc
7. Click on the "Create" button at the bottom of the window to begin pulling down the Docker image
8. Once the image is downloaded you should see it appear in the "Docker Containers" sub-tab


## Starting Debezium
Debezium requires an instance of Kafka, and ZooKeeper running in order to operate. This can be tricky and ports must be mapped to different host ports for easy compatibility and access.   