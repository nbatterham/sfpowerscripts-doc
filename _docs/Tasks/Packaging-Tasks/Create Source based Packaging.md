---
title: Create Source based Package 
category: Packaging Tasks
order: 3
---

This task is used to create a build artifact for a source based repo (org deployment), which can then be associated with a release pipeline.

**Task Snapshot**

**![](/images/Create a new version of Source Package .png){: width="839" height="444"}**

**Task Version and Details**

id: sfpwowerscripts-createsourcepackage-task

version: 4.0.0

**Input Variables&nbsp; - Visual Designer Labels (Yaml variables)**

* **Name of the package(package)**

  Provide a name of the package

* **the version number of the package to be created" (version\_number)**

  The format is major.minor.patch.buildnumber . This will override the build number mentioned in the sfdx-project.json, Try considering the use of Increment Version Number task before this task

* **SFDX Project directory that needs to be deployed (project\_directory)**

  Leave it blank if the sfdx-project.json is in the root of the repository, else provide the folder directory containing the sfdx-project.json

**Output Variables**

None

**Control Options**

None

**Gotcha's**

&nbsp;

**Changelog**

* 4\.0.0 Initial Version