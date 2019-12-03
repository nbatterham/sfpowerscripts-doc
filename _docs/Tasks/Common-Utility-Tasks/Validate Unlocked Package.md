---
title: Validate Unlocked Package for Metadata Coverage
category: Tasks
order: 4
---

This task is used to validate the metadata coverage of components that are part of the unlocked package you are building. Typically there are components in normal development that are not covered by unlocked packaging such as settings. Having this metadata in your project directory results either these metadata to be skipped or results in an error during the time of packaging. This task checks whether the source directory has any such issues.

**Prerequisites**

Please note [Install SFDX with Sfpowerkit](/Tasks/Common-Utility-Tasks/Install%20SFDX%20CLI/) task is added to the pipeline before utilizing this task

**Task Options**

**Input Variables**

**Output Variables**

**Control Options**

**Gotcha's**

**Changelog**

* 2\.0.1 Updated with Telemetry
* 1\.0.0 Updated for inclusion of bypass option from sfpowerkit