---
title: Install an Unlocked Package to an org
category: Deployment Tasks
subcategory: Deployment Tasks
order: 14
---

This task is a thin wrapper over sfdx force:package:install [command](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference_force_package.htm) with a helpful function to directly apply a build artifact built using Create SFDX Unlocked Package Task. This task is meant to be used in Release Pipeline

**Prerequisites**

Please note [Install SFDX with Sfpowerkit](/Tasks/Common-Utility-Tasks/Install%20SFDX%20CLI/) task is added to the pipeline before utilizing this task


**Task Snapshot**

**![](/images/Install Unlocked Package.png){: width="853" height="726"}**

**Task Version and Details**

id: sfpwowerscript-installunlockedpackage-task

version: 5.0.1

**Input Variables&nbsp; - Visual Designer Labels (Yaml variables)**

* **Alias or username of the target org(envname)**

  Provide the alias or username of the target org&nbsp; on which the unlocked package is to be deployed

* **Name of the package to be installed (package)**

  Name of the package to be installed

* **Package to be installed From (packageinstalledfrom)**

This task has two options, BuildArtifact or using a custom. If you specify BuildArtifact, specify the attached build artifact in the Artifact input parameter. If it is the custom option pass in the package id

* **Package Version Id (package\_version\_id)**

  Only enabled if the above option (Package to be installed from is Custom), pass the version id of the package

* **Name of the artifact that is attached to this release pipeline (artifact)**

The name of the artifact that is attached to this release pipeline. Please note it will only take artifact generated by Create SFDX Unlocked Package

* **Installation Key (installationkey)**

  Installation key for the package version to be installed

* **Compile Apex from only the package" (apexcompileonlypackage)**

  For unlocked packages only, specifies whether to compile all Apex in the org and package, or only the Apex in the package.

* **Security access type for the installed package" (security\_type)**

  Security access type for the installed package, Permissible values are: AllUsers, AdminsOnly

* **Upgrade type for the installed package" (upgrade\_type)**

  Upgrade type for the package to be installed, Permissible values are: Mixed, DeprecateOnly,Delete

* **Wait Time" (wait\_type)**

  Wait time for the command to finish in minutes

* **Publish Wait Time" (publish\_wait\_type)**

  Wait time for the command to wait for the created package to be available in the org, before it can be installed

**Output Variables**

None

**Control Options**

None

**Gotcha's**

None

**Changelog**

* 5.0.1 Updated with Telemetry
* 4.1.0 Initial Version