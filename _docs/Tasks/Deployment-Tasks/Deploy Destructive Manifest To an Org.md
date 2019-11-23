---
title: Deploy Destructive Maifest to an org
category: Tasks
order: 13
---

This task is a thin wrapper over sfpowerkit:org:destruct ([link](https://github.com/Accenture/sfpowerkit)). Typically, destructive manifest are deployed as a seperate pipeline in Org based development model. This task helps one to build a pipeline

**Task Snapshot**

![](/uploads/deploy-destructive-manifest-to-org.PNG){: width="800" height="400"}

**Task Version and Details**

id: sfpwowerscript-deploydestructivemanifest-task

version: 1.4.0

**Input Variables&nbsp; - Visual Designer Labels (Yaml variables)**

* **Alias or username of the target org(target_org)**

  Provide the alias or username of the target org&nbsp; on which destructive manifest has to be udpdated

* **Method (method)**

  Choose the mode, if text (Text) is selected, please enter a multi line destructive changes in the next field, or alternatively select filePath (FilePath) to mention the path to where destructive changes should be deployed.
 
* **Enter the destructive manifest (destructive_manifest_text)**

If text is the preferred  method, please follow the instructions here (https://developer.salesforce.com/docs/atlas.en-us.daas.meta/daas/daas_destructive_changes.htm ) on how to create the file

* **The path to the destrucive manifest file (destructive_manifest_filepath")**

 If FilePath is the preferred mode, please provide the path to the file in the checkout code repository associated with the build


**Output Variables**

None

**Control Options**

None

**Gotcha's**

None

**Changelog**

* 1.4.0 Initial Version