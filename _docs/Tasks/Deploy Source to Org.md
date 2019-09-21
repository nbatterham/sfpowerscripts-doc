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

**Input Variables&nbsp; - Visual Designer Labels (Yaml variables)**

* **Alias or username of the target org(target\_org)**

  Provide the alias or username of the target org&nbsp; on which the source directory is to be deployed

* **SFDX Project directory that needs to be deployed (project\_directory)**

  Leave it blank if the sfdx-project.json is in the root of the repository, else provide the folder directory containing the sfdx-project.json

* **Source Directory to be deployed (source\_directory)**

  mention the source directory in your project directory that needs to be deployed

* **Validate Deployment, do not deploy (checkonly)&nbsp;**

  Enable this for doing a validate only. Utilise this mechanism for Pull Request against Sandbox to validate the metadata

  * Once enabling this the following action will be enabled, where a file such as .validationignore can be specified that can be used to ignore certain metadata during a validate only deployment.<br>This is needed to overcome certain salesforce quirks, where during a validate only deployment, it raise unwanted errors if your source contains say a metadata such as ApexTestSuite

  * ![](/uploads/deploy-source-to-org-validate-only-deployment.png){: width="800" height="147"}

* **Wait Time (wait\_time)**

  Time to wait for this execution to complete,after this set wait time&nbsp; the next task in the pipeline will be executed. It is recommended to provide sufficient wait time so that the command can be made into a synchronous execution

* **Test Level (testlevel)**

  Security Token for this particular user, Security Token requirement can be removed by ensuring the particular user is allowed to connect to Salesforce from whitelisted IP ranges that include the IP ranges where Azure hosted agents will be executed. (available only in Credentials based authentication mode)

**Output Variables**

* **sfpowerkit\_deploysource\_id**

This variable holds the id of the deployment, you can use the deployment id to pull reports or do any further action on subsequent tasks

**Control Options**

None

**Gotcha's**

&nbsp;

**Changelog**

* 2\.8.0 Initial Version