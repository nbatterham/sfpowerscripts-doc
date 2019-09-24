---
title: Create/Delete a Scratch Org
category: Common/Utility Tasks
order: 6
---

This task is used to create and delete a scratch org and mostly used in a Pull Request validation pipeline. The task is an exact wrapper over the sfdx force:org:create command.

**Task Snapshot**

**![](/images/Create or Delete a scratchorg.png){: width="832" height="519"}**

**Task Version and Details**

id: sfpower-managescratchorg

version: 2.1.0

**Input Variables**

* **Action(action)** Select the action that this task should do, either create or delete an existting scratch org. Possible values are Create and Delete

* **Config File Path(config\_file\_path)**

The path to the file containing the configurations of the scratch org to be created. This field is only visible when Create mode is selected.

* **Alias(alias)**

Provide the alias for the scratch org, that is to be created. This field is visible only when create is activated

* **Alias or username of the target org(alias)**

Provide the alias for the scratch org, that is to be created. This field is visible only when create is activated

* **Alias/username of the DevHub (devhub\_alias)**

rovide the alias of the devhub previously authenticated, default value is HubOrg if using the Authenticate Org task

* **Working directory to be installed(working\_directory)**

The root directory that contains the sfdx-project.json. In build pipelines you can craete this blank, however when used in release pipelines mention the repo directory

**Output Variables**

* **sfpowerscripts\_scratch\_org\_url**

 The url of the scratch org that was created

* **sfpowerscripts\_scratch\_org\_username**

 The username of the scratch org that was created

**Control Options**

**Gotcha's**

Provide the repo path for the working directory in a releaase pipeline


**Changelog**

* 2.1.0 Initial Version