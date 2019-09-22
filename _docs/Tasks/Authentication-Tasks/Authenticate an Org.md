---
title: Authenticate an Org
category: Authentication-Tasks
order: 1
---

This task is used to authenticate against a salesforce org to do the required further actions. The task supports authentication to org using JWT (recommended) or using username/password/security. The org can then further accessed by utilizing the provided alias. It is higly recommended to create a service user while using this task.

To read more about JWT based authentication and to generate the private key files, please follow the instruction&nbsp;[here](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_auth_jwt_flow.htm).

&nbsp;

**Task Snapshot**

![](/images/Authenticate a Salesforce Org.png){: width="951" height="629"}
![](/images/Authenticate a Salesforce Org using JWT.png){: width="951" height="629"}
![](/images/Authenticate a Salesforce Org using Credentials.png){: width="951" height="629"}

**Task Version and Details**

id: sfpower-authenticateorg

version: 3.0.0

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

