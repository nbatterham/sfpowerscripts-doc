---
title: Deploy Source to Org
category: Tasks
order: 3
---

This task is used to deploy/validate metadata which is in source format (newer format) to any org, be it a scratch org, sandbox or production. The task does the following things.

1. Converts the source directory to metadata using source:convert command
2. Use mdapi:deploy to deploy/validate the converted metadata to an org
3. Run any associated test runs supported along with the mdapi:deploy command

You can read about mdapi:deploy command [here](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference_force_mdapi.htm) and understand the various options


**Task Snapshot**

![](/images/Deploy Source To Org.png){: width="951" height="629"}


**Task Version and Details**

id: sfpowerscript-deploysourcetoorg-task

version: 2.8.0

**Input Variables [Visual Designer Labels / Yaml variables]**


- **Authentication Method(method)**

   The method to authenticate this org. Available methods are either using JWT or using Credentials (Username/Password/Security Token)


- **Secure File(jwt_key_file)**

   Secure file containing the private key, used only if the authentication method is JWT based. Instructions to store the private key as a secure file are avaiable [here](https://docs.microsoft.com/en-us/azure/devops/pipelines/library/secure-files?view=azure-devops)

- **Username(username)**

   Username for the authenticated user (available in both JWT and Credentials based authentication mode)


- **clientid(clientid)**

  OAuth client ID (sometimes called the consumer key) (available only in  JWT  based authentication mode)

- **Password(password)**

   Password for the authenticated user (available only in Credentials based authentication mode)

- **Security Token(securitytoken)**

   Security Token for this particular user, Security Token requirement can be removed by ensuring the particular user  is allowed to connect to Salesforce from whitelisted IP ranges that include the IP ranges where Azure hosted agents will be executed. (available only in Credentials based authentication mode)

- **Alias(alias)**

   Alias of the org to be used in subsequent tasks (available in both JWT and Credentials based authentication mode)


- **Authenticate this org as a DevHub(isdevhub)**

  Enable this variable, if the org is to be authenticated as a DevHub, this is required incase this org is used in subsequent task to create a scratch org or to create an unlocked package (available in both JWT and Credentials based authentication mode)




**Output Variables**

None

**Control Options**

None

**Gotcha's**

JWT based authentication is the preferred approach and it is intendended for CI/CD based non human authentication

**Changelog**

- 3.0.0  Initial Version 

