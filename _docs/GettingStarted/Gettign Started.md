---
title: Getting Started
category: Getting Started
order: 1
---

Here is how to get started with SFPowerscripts.

1. Sign into your Azure Pipelines Account. If you are not an Azure Pipelines customer, it is quite easy to get one going. Follow the links [here](https://azure.microsoft.com/en-au/services/devops/)

2. Install  the sfpowerscripts extension into your Azure Pipelines org from [here](https://marketplace.visualstudio.com/items?itemName=AzlamSalam.sfpowerscripts)

3. Once installed, import the sample pipelines or build your own using the tasks.

4. If there are multiple teams actively involved and you are following an unlocked package based development model, it is recommended to have a hosted agent per active team

5. Create a variable group per environment and attach this variable groups to the pipelines

![](/images/variable_group_for_envs.png){: width="812" height="440"}


Please note SFPowerscripts is only tested against Microsoft Hosted Agent running Ubuntu 16.04. If you would like to contribute to the extension to ensure it is cross platform, please contribute to the repo in Github.

It is recommended to have a variable group created per environment,such as in the figure and associate it with each stage of the pipeline

![](/images/variable_group_for_envs.png){: width="812" height="440"}