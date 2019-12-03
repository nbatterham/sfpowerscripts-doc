---
title: Install SFDX CLI and SFPowerkit
category: Tasks
subcategory: Utility Tasks
order: 1
---

This task is usually the first task of any pipeline you build using sfpowerscripts. It installs the SFDX CLI along with the open source extension '[sfpowerkit](https://github.com/Accenture/sfpowerkit)'.&nbsp;

Please note this task is only supported only in Linux agents

**Please note an earlier version of this task with the exact functionality is now deprecated at 1.3.0. Please utilize a newer version of this task with updated id for the same functionality. The task name is "Install SFDX CLI with SFPowerkit"**

**Task Snapshot**

![](/images/Install SFDX CLI Task.PNG){: width="930" height="374"}

**Task Version and Details**

id: sfpwowerscript-installsfdx-task

version: 3.2.1

**Input Variables \[Visual Designer Labels / Yaml variables\]**

* **SFDX CLI Version (sfdx\_cli\_version)**

  By default, the latest SFDX CLI version will be installed. You can override this by providing the version number found in [Salesforce CLI Release Notes](https://developer.salesforce.com/media/salesforce-cli/releasenotes.html)

* **SFPowerkit Version (sfpowerkit\_version)**

  By default, the latest SFPowerkit version will be installed. You can override this by providing the version number found in [SFPowerkit Release Notes](https://github.com/Accenture/sfpowerkit/releases)

**Output Variables**

None

**Control Options**

None

**Gotcha's**

**Changelog**

* 3.2.1 Updated with Telemetry
* 2.0.0 Task updated with new id
* 1.3.0 Deprecated the task&nbsp;
* 1.2.0 Initial Version