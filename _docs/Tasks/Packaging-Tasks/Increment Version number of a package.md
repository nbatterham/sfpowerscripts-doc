---
title: Increment Version Number of a package
category: Packaging Tasks
order: 1
---

This task is used to increment the version number of the package version provided in sfdx-project.json for either an unlocked package or an org based deployment. Use the version number outputted by this task as input to the Create Package tasks, if you want the package number to be incremented during every package build pipeline trigger

**Task Snapshot**

&nbsp;

**![](/images/Increments Version Number of a package.png){: width="864" height="569"}**

**Task Version and Details**

id: sfpwowerscript-incrementversionnumber-task

version: 1.9.0

**Input Variables&nbsp; - Visual Designer Labels (Yaml variables)**

* **Increment which segment of the version(segment)**

  Select the segment of the version number that needs to be incremented, Possible values are BuildNumber, Patch, Minor, Major

* **Set the pipeline's build number to the the project's incremented version number" (set\_build\_number)**

Check this flag, if the pipeline's build number to be updated with the incremented version,so its easy to undertand the job in Azure Pipeliens

* **Create a commit of incremented sfdx-project.json" (commit\_changes)**

  Check this flag, if you need the incremented version in sfdx=project.json to be committed back to the repo. Please not this only does the commit it doesnt do the Push yet

* **Name of the package" (package)**

  The name of the package on which the version needs to be created, if ingored, the default package mentioned in sfdx-project.json will be utilized

* **SFDX Project directory that needs to be deployed (project\_directory)**

  Leave it blank if the sfdx-project.json is in the root of the repository, else provide the folder directory containing the sfdx-project.json

**Output Variables**

* **sfpowerscripts\_incremented\_project\_version**

The output version as a result of running this task

**Control Options**

None

**Gotcha's**

&nbsp;

**Changelog**

* 4\.0.0 Initial Version