---
title: Trigger Apex Test
category: Tasks
order: 13
---

This task is used to trigger apex tests in an org

**Prerequisites**

Please note [Install SFDX with Sfpowerkit](/Tasks/Common-Utility-Tasks/Install%20SFDX%20CLI/)task is added to the pipeline before utilizing this task


**Task Snapshot**

**![](/uploads/trigger-apex-tests.PNG){: width="800" height="448"}**

**Task Version and Details**

id: sfpwowerscript-triggerapextest-task

version: 2.0.1

**Input Variables&nbsp; - Visual Designer Labels (Yaml variables)**

* **Alias or username of the target org(target\_org)**<br><br>Provide the alias or username of the target org&nbsp; on which destructive manifest has to be udpdated
* **Test Level(testlevel)**<br><br>Select the testlevel for this task from the possible list of values, The values include the following<br>&nbsp; - RunSpecifiedTests (Run only specified tests)<br>&nbsp; - RunApexTestSuite (Run an apex test suite)<br>&nbsp; - &nbsp;RunLocalTests (Run Local Tests)<br>&nbsp; - &nbsp;RunAllTestsInOrg (Run All Tests in the org)

* **Tests to be executed(specified\_tests)**<br><br>This field will be visible only if the Test Level is RunSpecifiedTests, Provide a coma seperated list of apex test classes that is to be executed

* **Apex Test Suite(apextestsuite)**<br><br>This field will be visible only if the Test Level is RunApexTestSuite, Provide&nbsp; the name of the apex test suite that should be executed with this task.

* **Wait Time (wait\_time)**<br><br>The time this task should wait for the result to be generated. The default wait time is 60 minutes.

**Output Variables**

None

**Control Options**

None

**Gotcha's**

None

**Changelog**

* 2.0.1 Updated with Telemetry
* 1.1.0 Initial Version