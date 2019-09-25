---
title: Install SFDX CLI and SFPowerkit
category: Tasks
order: 1
---

This task is usually the first task of any pipeline you build using sfpowerscripts. It installs the SFDX CLI along with the open source extension '[sfpowerkit](https://github.com/Accenture/sfpowerkit)'.&nbsp;

Please note this task is only supported only in Linux agents

**Task Snapshot**

![](/images/Install SFDX CLI Task.PNG){: width="930" height="374"}

**Task Version and Details**

id: sfpwowerkit-installsfdx-task

version: 1.2.0

**Input Variables [Visual Designer Labels / Yaml variables]**

- **SFDX CLI Version (sfdx_cli_version)** 
    
     By default, the latest SFDX CLI version will be installed. You can override this by providing the version number found in [Salesforce CLI Release Notes](https://developer.salesforce.com/media/salesforce-cli/releasenotes.html)

- **SFPowerkit Version (sfpowerkit_version)** 
    
    By default, the latest SFPowerkit version will be installed. You can override this by providing the version number found in [SFPowerkit Release Notes](https://github.com/Accenture/sfpowerkit/releases)


**Output Variables**

None

**Control Options**

None

**Gotcha's**


**Changelog**

- 1.2.0  Initial Version 
